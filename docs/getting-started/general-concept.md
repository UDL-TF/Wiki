# General Concept

## What is Dodgeball?

**Dodgeball** (commonly abbreviated as **TFDB** or **DB**) is a community-created game mode for Team Fortress 2 that transforms the game into a fast-paced arena of reflexes and precision. The core concept is simple yet compelling: two teams of Pyros face off, reflecting homing rockets back and forth until one team fails to deflect.

---

## The Core Mechanics

### Homing Rockets

Unlike standard TF2 rockets, Dodgeball rockets are **homing projectiles** that track their target. When a rocket is reflected, the plugin selects a new target based on **positioning logic** - typically the furthest player in the direction of the reflect.

Key characteristics:

- Rockets **gain speed** with each reflection
- Rockets **lock onto a new target** after being reflected (based on positioning, not random)
- Maximum speed can reach extreme levels in extended rallies
- Rocket speed resets when a new round begins

### Target Selection

The rocket's target is determined by the **SelectTarget** algorithm in the TFDB plugin:

1. Each potential target receives a **base random weight** (0-100)
2. A **directional bonus** is added based on alignment with your aim direction
3. The bonus uses the **dot product** of your aim direction and the vector to each player
4. Players more aligned with your crosshair get higher weight
5. The player with the **highest combined score** becomes the target

The `RocketClassTargetWeight` server config determines how much aim direction matters versus randomness.

!!! tip "Dragging"
    **Dragging** is a technique where you manipulate your aim during the airblast to influence targeting. Aiming **toward** a player increases their selection weight; aiming **away** decreases it. While not 100% deterministic (there's still a random component), skilled dragging significantly improves your odds of hitting your intended target. See [Dragging](../techniques/dragging.md) for details.

### The Airblast

The **airblast** (secondary fire for Pyro) is your only tool for survival. When timed correctly, an airblast will:

1. Deflect the incoming rocket
2. Change its target to an enemy player
3. Increase its speed slightly
4. Reset your airblast cooldown (on most servers)

!!! warning "Timing is Everything"
    Airblast too early, and the rocket will pass through. Airblast too late, and... well, you know what happens.

---

## Server Plugins

Dodgeball servers run specialized **SourceMod plugins** that modify game behavior.

---

## The Skill Ceiling

What makes Dodgeball unique is its **deceptively high skill ceiling**. While the concept is simple, mastery involves:

<div class="technique-highlight" markdown>

- **Reaction time**: Responding to rockets at extreme speeds
- **Prediction**: Anticipating where rockets will go
- **Positioning**: Being in the optimal location to reflect
- **Technique execution**: Performing advanced moves like [orbits](../techniques/orbiting.md), [spikes](../techniques/downspike.md), and [dragging](../techniques/dragging.md)
- **Mind games**: Outplaying opponents psychologically

</div>

---

## Why Play Dodgeball?

:material-check-circle: **Simple to learn** - Only one mechanic to master  
:material-check-circle: **Deep gameplay** - Endless room for improvement  
:material-check-circle: **Active community** - Dedicated players and servers  
:material-check-circle: **Competitive scene** - Organized leagues and tournaments  
:material-check-circle: **Satisfying gameplay** - Nothing beats a perfectly timed reflect  

---

## Next Steps

Ready to dive in? Continue to the [Gameplay](gameplay.md) guide to learn the rules and objectives of a Dodgeball match.
