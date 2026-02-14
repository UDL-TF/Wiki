# Basic Syntax

This guide covers the basic Markdown syntax elements that are supported in nearly all Markdown applications.

## Headings

To create a heading, add number signs (#) in front of a word or phrase. The number of number signs corresponds to the heading level.

```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

### Output:

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

## Paragraphs

To create paragraphs, use a blank line to separate one or more lines of text.

```markdown
This is the first paragraph.

This is the second paragraph.
```

## Line Breaks

To create a line break, end a line with two or more spaces, then type return.

```markdown
This is the first line.  
And this is the second line.
```

## Emphasis

### Bold

To bold text, add two asterisks or underscores before and after a word or phrase.

```markdown
**bold text**
__bold text__
```

**Output**: **bold text**

### Italic

To italicize text, add one asterisk or underscore before and after a word or phrase.

```markdown
*italic text*
_italic text_
```

**Output**: *italic text*

### Bold and Italic

To emphasize text with bold and italics at the same time, add three asterisks or underscores.

```markdown
***bold and italic***
___bold and italic___
```

**Output**: ***bold and italic***

## Blockquotes

To create a blockquote, add a > in front of a paragraph.

```markdown
> This is a blockquote.
```

**Output**:

> This is a blockquote.

### Nested Blockquotes

Blockquotes can be nested by adding additional > symbols.

```markdown
> This is a blockquote.
>
>> This is a nested blockquote.
```

**Output**:

> This is a blockquote.
>
>> This is a nested blockquote.

## Lists

### Ordered Lists

To create an ordered list, add line items with numbers followed by periods.

```markdown
1. First item
2. Second item
3. Third item
```

**Output**:

1. First item
2. Second item
3. Third item

### Unordered Lists

To create an unordered list, add dashes (-), asterisks (*), or plus signs (+) in front of line items.

```markdown
- First item
- Second item
- Third item
```

**Output**:

- First item
- Second item
- Third item

### Nested Lists

You can create nested lists by indenting items.

```markdown
- First item
  - Nested item
  - Nested item
- Second item
```

**Output**:

- First item
  - Nested item
  - Nested item
- Second item

## Code

### Inline Code

To denote a word or phrase as code, enclose it in backticks (`).

```markdown
Use the `printf()` function.
```

**Output**: Use the `printf()` function.

### Code Blocks

To create code blocks, indent every line of the block by at least four spaces or one tab, or use triple backticks (```).

````markdown
```
{
  "name": "example",
  "version": "1.0.0"
}
```
````

**Output**:

```
{
  "name": "example",
  "version": "1.0.0"
}
```

## Horizontal Rules

To create a horizontal rule, use three or more asterisks (***), dashes (---), or underscores (___).

```markdown
---
```

**Output**:

---

## Links

To create a link, enclose the link text in brackets and then follow it immediately with the URL in parentheses.

```markdown
[Markdown Guide](https://wiki.udl.tf)
```

**Output**: [Markdown Guide](https://wiki.udl.tf)

### URLs and Email Addresses

To quickly turn a URL or email address into a link, enclose it in angle brackets.

```markdown
<https://wiki.udl.tf>
<email@example.com>
```

## Images

To add an image, add an exclamation mark (!), followed by alt text in brackets, and the path or URL to the image in parentheses.

```markdown
![Alt text](image.jpg)
```

### Images with Links

To add a link to an image, enclose the Markdown for the image in brackets, and then add the link in parentheses.

```markdown
[![Alt text](image.jpg)](https://example.com)
```

## Escaping Characters

To display a literal character that would otherwise be used to format text in a Markdown document, add a backslash (\\) in front of the character.

```markdown
\* Without the backslash, this would be a bullet point.
```

**Output**: \* Without the backslash, this would be a bullet point.

## Next Steps

Now that you've learned the basics, explore our [Extended Syntax](../extended-syntax/tables.md) guides to learn about more advanced features.
