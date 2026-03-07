# Contributing to the TFDB Wiki

![UDL Logo](../assets/logo.png){ align=right width="100" }

Thank you for your interest in contributing to the TFDB Wiki! This guide explains how you can help improve this community resource.

---

## Ways to Contribute

### 1. Request Changes

Don't have a GitHub account or not sure how to edit? No problem!

:material-arrow-right: **[Request Changes](request-changes.md)** - Submit suggestions for corrections or new content.

### 2. Direct Editing

For those comfortable with Git and Markdown:

1. **Fork** the [Wiki repository](https://github.com/UDL-TF/Wiki)
2. **Edit** files in the `docs/` folder
3. **Submit** a Pull Request

### 3. Join the Discussion

Connect with the community to discuss wiki content:

- :fontawesome-brands-discord: [UDL Discord](https://udl.tf) - Chat with the community
- :fontawesome-brands-github: [GitHub Issues](https://github.com/UDL-TF/Wiki/issues) - Report issues or suggest features
- :fontawesome-brands-github: [GitHub Discussions](https://github.com/UDL-TF/Wiki/discussions) - Long-form discussions

---

## Contribution Guidelines

### Content Standards

All contributions should follow these guidelines:

| Guideline      | Description                                |
| -------------- | ------------------------------------------ |
| **Accuracy**   | Information must be correct and verifiable |
| **Clarity**    | Write clearly for all skill levels         |
| **Neutrality** | Present techniques objectively             |
| **Formatting** | Follow existing page structure             |
| **Links**      | Link to related pages when relevant        |

### Writing Style

- Use **clear, concise language**
- Explain jargon on first use
- Include **practical examples**
- Use tables and lists for readability
- Add diagrams where helpful

### What We're Looking For

!!! tip "High-Priority Contributions"
    
    - Technique details marked as "TBD"
    - Video examples and demonstrations
    - Map-specific strategies
    - Server configuration guides
    - Translations

---

## How to Edit Pages

### Using GitHub's Web Editor

1. Click the :material-pencil: **Edit** button on any page
2. Make your changes in the editor
3. Write a clear commit message
4. Submit a Pull Request

### Using Local Development

```bash
# Clone the repository
git clone https://github.com/UDL-TF/Wiki.git
cd Wiki

# Create a branch
git checkout -b my-contribution

# Install dependencies
pip install -r requirements.txt

# Start local server
mkdocs serve

# Make your changes, then commit
git add .
git commit -m "Description of changes"
git push origin my-contribution
```

Then open a Pull Request on GitHub.

---

## Page Structure

Follow this general structure for technique pages:

```markdown
# Technique Name

:material-star: **Difficulty**: Level

---

## Overview
Brief introduction to the technique.

## How It Works
Detailed explanation.

## Execution
Step-by-step instructions.

## When to Use
Strategic applications.

## Common Mistakes
What to avoid.

## Practice Tips
How to improve.

## Related Techniques
Links to related content.
```

---

## Markdown Reference

This wiki uses [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/). Key features:

### Admonitions

```markdown
!!! tip "Title"
    Content here
```

### Tables

```markdown
| Header 1 | Header 2 |
| -------- | -------- |
| Cell 1   | Cell 2   |
```

### Links

```markdown
[Link Text](relative/path.md)
[External](https://example.com)
```

### Images

```markdown
![Alt text](../assets/image.png){ width="200" }
```

---

## Review Process

1. **Submit** - Create a Pull Request
2. **Review** - Community members review changes
3. **Feedback** - Make requested changes if needed
4. **Merge** - Changes go live on the wiki

Reviews typically take 1-3 days.

---

## Code of Conduct

- Be respectful and constructive
- Focus on improving content
- Accept feedback gracefully
- Help other contributors

---

## Questions?

Need help contributing?

- Join the [UDL Discord](https://udl.tf) and ask in the wiki channel
- Open an [issue on GitHub](https://github.com/UDL-TF/Wiki/issues)
- Contact a wiki maintainer

---

<div style="text-align: center; margin-top: 2rem;">
    <small>Every contribution helps make this wiki better for the entire community!</small>
</div>
