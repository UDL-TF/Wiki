# Rocket Classes

:material-rocket-launch: **Understanding TFDB Rocket Types**

---

## Overview

In TF2 Dodgeball, rockets are defined by **classes** in the server configuration. Each class specifies how a rocket behaves—its speed, turn rate, damage, appearance, sounds, and special effects. Server operators can create custom rocket types with unique characteristics.

The two most common rocket classes are:

- **Common** (Homing Rocket) - The standard rocket used in most gameplay
- **Nuke** - A special rocket with devastating effects

---

## Rocket Class Parameters

Each rocket class can configure numerous parameters:

### Basic Parameters

| Parameter     | Description                                                   | Example                    |
| ------------- | ------------------------------------------------------------- | -------------------------- |
| `name`        | Display name of the rocket                                    | `"Homing Rocket"`          |
| `behaviour`   | Tracking type: `homing` (smooth) or `legacy homing` (classic) | `"homing"`                 |
| `model`       | Custom model path (optional)                                  | `"models/custom/nuke.mdl"` |
| `is animated` | Whether the model has animations                              | `0` or `1`                 |

### Sound Parameters

| Parameter          | Description               | Default              |
| ------------------ | ------------------------- | -------------------- |
| `play spawn sound` | Emit sound when spawning  | Sentry rocket sound  |
| `play beep sound`  | Emit beeping while flying | Sentry search sound  |
| `play alert sound` | Alert target player       | Sentry spotted sound |
| `beep interval`    | Time between beeps        | `0.5` seconds        |

### Movement Parameters

| Parameter             | Description                                       |
| --------------------- | ------------------------------------------------- |
| `speed`               | Base speed (HU/s)                                 |
| `speed increment`     | Speed added per deflection                        |
| `speed limit`         | Maximum speed cap (0 = no limit)                  |
| `turn rate`           | Base turning rate per tick                        |
| `turn rate increment` | Turn rate added per deflection                    |
| `turn rate limit`     | Maximum turn rate cap                             |
| `elevation rate`      | Vertical elevation rate on deflect                |
| `elevation limit`     | Maximum elevation angle                           |
| `control delay`       | Delay before rocket starts homing after deflect   |
| `drag pause duration` | How long rocket flies straight before reading aim |

### Damage Parameters

| Parameter          | Description                                    |
| ------------------ | ---------------------------------------------- |
| `damage`           | Base damage dealt                              |
| `damage increment` | Damage added per deflection                    |
| `critical chance`  | Percentage chance for critical hit (3x damage) |

### Behaviour Modifiers

| Parameter            | Description                               |
| -------------------- | ----------------------------------------- |
| `elevate on deflect` | Rocket gains elevation after each deflect |
| `neutral rocket`     | No team-based targeting                   |
| `keep direction`     | Maintains direction after surface bounce  |
| `teamless deflects`  | Any player can deflect (not just enemies) |
| `reset bounces`      | Reset bounce counter on deflect           |
| `no bounce drags`    | Disable dragging after surface contact    |
| `can be stolen`      | Allow stealing rocket from current target |
| `max bounces`        | Maximum surface bounces allowed           |
| `bounce scale`       | Bounce force multiplier                   |

### Target Selection

| Parameter                    | Description                                      |
| ---------------------------- | ------------------------------------------------ |
| `direction to target weight` | Weight modifier for target selection algorithm   |
| `no. players modifier`       | Speed modifier based on player count             |
| `no. rockets modifier`       | Speed modifier based on rockets fired this round |

---

## Common Rocket (Default)

The standard homing rocket used in most Dodgeball gameplay.

```yaml
"common"
{
    "name"                        "Homing Rocket"
    "behaviour"                   "homing"
    "play spawn sound"            "1"
    "play beep sound"             "1"
    "play alert sound"            "1"
    
    "damage"                      "50"
    "damage increment"            "25"
    "speed"                       "875"
    "speed increment"             "160"
    "turn rate"                   "0.260"
    "turn rate increment"         "0.0180"
    "max bounces"                 "1000"
    "drag pause duration"         "0.1"
    "critical chance"             "100"
    "direction to target weight"  "100"
}
```

### Key Characteristics

- **Base Speed**: 875 HU/s
- **Speed per Deflect**: +160 HU/s
- **Turn Rate**: 0.260 (increases by 0.018 per deflect)
- **Drag Window**: 0.1 seconds (100ms)
- **Bounces**: Up to 1000 surface bounces

---

## Nuke Rocket

A special rocket with devastating explosion effects.

```yaml
"nuke"
{
    "name"                        "Nuke!"
    "behaviour"                   "homing"
    "model"                       "models/custom/dodgeball/nuke/nuke.mdl"
    "is animated"                 "1"
    "beep interval"               "0.2"
    
    "damage"                      "200"
    "damage increment"            "200"
    "speed"                       "550"
    "speed increment"             "100"
    "turn rate"                   "0.233"
    "turn rate increment"         "0.0275"
    "elevation rate"              "0.1237"
    "elevation limit"             "0.1237"
    "max bounces"                 "0"
    "direction to target weight"  "25"
    
    "on explode"                  "tf_dodgeball_explosion @dead ; tf_dodgeball_shockwave @dead 200 1000 1000 600"
}
```

### Key Characteristics

- **Base Speed**: 550 HU/s (slower than common)
- **Damage**: 200 base (+200 per deflect)
- **Turn Rate**: 0.233 (tighter turning)
- **No Bounces**: Cannot bounce off surfaces
- **Explosion Effects**: Creates shockwave on kill
- **Lower Target Weight**: 25 (more random target selection)

---

## Wave Rockets

!!! info "Custom Rocket Type"
    Wave rockets are a custom rocket class that creates oscillating trajectories. Not all servers have wave rockets configured.

Wave rockets modify the standard homing behaviour to create unpredictable, wavelike flight paths. This is achieved through special configuration values, **not** through player technique.

If a server has wave rockets enabled, they will appear in the spawn rotation alongside common and nuke rockets.

---

## Spawner Configuration

Rockets spawn from team-specific spawners with configurable chances:

```yaml
"spawners"
{
    "red"
    {
        "max rockets"    "1"
        "interval"       "2.0"
        "common%"        "90"
        "nuke%"          "10"
    }
}
```

This means:
- Maximum 1 rocket at a time
- 2 second spawn interval
- 90% chance of common rocket
- 10% chance of nuke rocket

---

## Event System

Rockets can trigger commands on specific events:

| Event          | When It Fires                  |
| -------------- | ------------------------------ |
| `on spawn`     | Rocket spawns                  |
| `on deflect`   | Player deflects rocket         |
| `on kill`      | Rocket kills a player          |
| `on explode`   | Same as kill (triggers once)   |
| `on no target` | Rocket has no valid target     |
| `on destroyed` | Rocket expires without killing |

### Event Parameters

Events can use these parameters in commands:

| Parameter      | Type    | Description                |
| -------------- | ------- | -------------------------- |
| `@name`        | String  | Rocket type name           |
| `@rocket`      | Integer | Rocket entity index        |
| `@owner`       | Integer | Deflector's client index   |
| `@target`      | Integer | Target's client index      |
| `@dead`        | Integer | Dead player's client index |
| `@deflections` | Integer | Total deflection count     |
| `@speed`       | Float   | Current speed (with limit) |
| `@mphspeed`    | Integer | Speed in MPH (no limit)    |

---

## Server Commands

TFDB provides special commands for events:

```
tf_dodgeball_explosion <client>
```
Shows a large explosion at the client's location.

```
tf_dodgeball_shockwave <client> <damage> <force> <radius> <falloff>
```
Applies a shockwave from the client's location.

---

## See Also

- [General Concept](../getting-started/general-concept.md) - How rockets select targets
- [Dragging](../techniques/dragging.md) - Influencing target selection through aim
