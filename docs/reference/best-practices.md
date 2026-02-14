# Best Practices

Writing effective Markdown requires more than just knowing the syntax. Follow these best practices to create clean, readable, and maintainable documentation.

## General Guidelines

### 1. Be Consistent

Choose a style and stick with it throughout your document:

- Use either `*` or `_` for emphasis (not both)
- Use either `-` or `*` for unordered lists (not both)
- Be consistent with heading styles
- Use consistent indentation (2 or 4 spaces)

### 2. Use Blank Lines

Add blank lines between different elements for better readability:

```markdown
# Heading

This is a paragraph.

This is another paragraph.

- List item 1
- List item 2
```

### 3. Keep Lines Reasonably Short

While Markdown doesn't enforce line length, keeping lines around 80-100 characters improves readability in plain text:

```markdown
This is a very long line that should probably be broken up into multiple 
lines to make it easier to read in plain text editors and version control 
systems.
```

## Headings

### Use Hierarchical Structure

Organize your content with a clear hierarchy:

```markdown
# Main Title (H1) - Use once per document

## Major Section (H2)

### Subsection (H3)

#### Minor Section (H4)
```

### Don't Skip Heading Levels

❌ **Bad:**
```markdown
# Heading 1
### Heading 3
```

✅ **Good:**
```markdown
# Heading 1
## Heading 2
### Heading 3
```

## Lists

### Use Proper Indentation

Indent nested lists by 2 or 4 spaces:

```markdown
- Main item
  - Nested item
    - Deeply nested item
```

### Add Blank Lines for Multi-Paragraph Items

```markdown
1. First item with a long description that spans
   multiple lines.

   This is a second paragraph for the first item.

2. Second item
```

## Links and Images

### Use Descriptive Link Text

❌ **Bad:**
```markdown
Click [here](https://example.com) for more information.
```

✅ **Good:**
```markdown
Read the [documentation](https://example.com) for more information.
```

### Always Add Alt Text for Images

```markdown
![Screenshot of the main dashboard showing user statistics](dashboard.png)
```

### Use Reference-Style Links for Repeated URLs

```markdown
Check out [GitHub][gh] and [GitHub Pages][gh-pages].

[gh]: https://github.com
[gh-pages]: https://pages.github.com
```

## Code

### Specify the Language for Code Blocks

````markdown
```python
def hello():
    print("Hello, World!")
```
````

### Use Inline Code for Technical Terms

Use inline code for:
- Function names: `print()`
- File names: `config.yml`
- Commands: `git commit`
- Code snippets: `const x = 5`

## Tables

### Align Table Columns in Source

While not required, aligning columns makes tables easier to read in plain text:

```markdown
| Name       | Age | Location     |
| ---------- | --- | ------------ |
| Alice      | 30  | New York     |
| Bob        | 25  | Los Angeles  |
| Charlie    | 35  | Chicago      |
```

## Compatibility

### Test with Your Target Platform

Different Markdown processors support different features:

- GitHub Flavored Markdown (GFM)
- CommonMark
- Markdown Extra
- MultiMarkdown

### Avoid Over-Reliance on HTML

While many processors allow HTML, it reduces portability:

❌ **Avoid:**
```html
<div align="center"><strong>Title</strong></div>
```

✅ **Prefer:**
```markdown
**Title**
```

## File Organization

### Use Meaningful File Names

- Use lowercase
- Use hyphens for spaces
- Be descriptive: `installation-guide.md` not `guide.md`

### Create a Logical Directory Structure

```
docs/
├── getting-started/
│   ├── installation.md
│   └── quick-start.md
├── guides/
│   ├── configuration.md
│   └── deployment.md
└── reference/
    └── api.md
```

## Accessibility

### Provide Meaningful Alt Text

```markdown
![Bar chart showing 40% increase in user engagement](chart.png)
```

### Use Semantic Headings

Don't use headings just for styling. Use them to create document structure.

### Ensure Link Text is Descriptive

Screen readers often jump between links. Make sure each link's purpose is clear from its text alone.

## Version Control

### Make Atomic Commits

Each commit should contain a single logical change to your documentation.

### Write Clear Commit Messages

```
docs: Add section on table formatting

Added examples and best practices for creating and formatting
tables in Markdown documents.
```

### Review Diffs Before Committing

Markdown diffs should be readable. If they're not, consider restructuring your changes.

## Maintenance

### Keep Documentation Current

- Review and update regularly
- Remove outdated information
- Add deprecation notices when needed

### Use Comments Sparingly

HTML comments can be used in Markdown but aren't visible in the rendered output:

```markdown
<!-- TODO: Add more examples here -->
```

### Lint Your Markdown

Use tools like markdownlint to maintain consistency:

```bash
markdownlint **/*.md
```

## Performance

### Optimize Images

- Compress images before adding them
- Use appropriate formats (PNG for screenshots, JPEG for photos)
- Consider image size and load time

### Limit Large Files

- Don't commit large binary files to documentation repositories
- Use external hosting for videos and large assets

## Summary

Following these best practices will help you create:

- **Readable** documentation in both source and rendered forms
- **Maintainable** content that's easy to update
- **Portable** documents that work across different platforms
- **Accessible** content for all users
- **Professional** documentation that follows industry standards

Remember: The goal is to communicate effectively. Let clarity and consistency guide your choices.
