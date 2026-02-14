# Markdown Cheat Sheet

A quick reference guide for the most commonly used Markdown syntax.

## Basic Syntax

### Headings

```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

### Emphasis

```markdown
*italic* or _italic_
**bold** or __bold__
***bold and italic***
~~strikethrough~~
```

### Lists

**Unordered:**
```markdown
- Item 1
- Item 2
  - Nested item
```

**Ordered:**
```markdown
1. First item
2. Second item
3. Third item
```

### Links

```markdown
[Link text](https://example.com)
[Link with title](https://example.com "Title")
<https://example.com>
```

### Images

```markdown
![Alt text](image.jpg)
![Alt text](image.jpg "Image title")
```

### Code

**Inline:** `` `code` ``

**Block:**
````markdown
```language
code block
```
````

### Blockquotes

```markdown
> Blockquote
>> Nested blockquote
```

### Horizontal Rule

```markdown
---
***
___
```

## Extended Syntax

### Tables

```markdown
| Header 1 | Header 2 |
| -------- | -------- |
| Cell 1   | Cell 2   |
```

**With alignment:**
```markdown
| Left | Center | Right |
| :--- | :----: | ----: |
| Text | Text   | Text  |
```

### Task Lists

```markdown
- [x] Completed task
- [ ] Incomplete task
```

### Footnotes

```markdown
Here's a sentence with a footnote.[^1]

[^1]: This is the footnote.
```

### Definition Lists

```markdown
Term
: Definition
```

### Strikethrough

```markdown
~~Strikethrough text~~
```

### Highlight

```markdown
==Highlighted text==
```

### Subscript and Superscript

```markdown
H~2~O (subscript)
X^2^ (superscript)
```

## Code Syntax Highlighting

Common language identifiers:

- `bash` or `shell`
- `c`, `cpp`, `csharp`
- `css`, `html`, `xml`
- `go`, `java`, `javascript`, `js`
- `json`, `yaml`, `toml`
- `markdown`, `md`
- `python`, `py`
- `ruby`, `rust`
- `sql`, `typescript`, `ts`

## Escaping Characters

Use backslash (\\) to escape special characters:

```markdown
\* \_ \{ \} \[ \] \( \) \# \+ \- \. \! \|
```

## HTML in Markdown

Most Markdown processors allow HTML:

```html
<div align="center">
  <strong>Bold text using HTML</strong>
</div>
```

## Emoji (GitHub Flavored Markdown)

```markdown
:smile: :heart: :thumbsup:
```

## Tips

1. Leave blank lines between different elements
2. Use consistent indentation (2 or 4 spaces)
3. Preview your Markdown before publishing
4. Check which features your Markdown processor supports
5. Use a linter to maintain consistent formatting

## Quick Reference Links

- [Basic Syntax Guide](../getting-started/basic-syntax.md)
- [Tables](../extended-syntax/tables.md)
- [Code Blocks](../extended-syntax/code-blocks.md)
- [Task Lists](../extended-syntax/task-lists.md)
