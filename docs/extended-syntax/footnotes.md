# Footnotes

Footnotes allow you to add notes and references without cluttering the body of your document. When you create a footnote, a superscript number with a link appears where you added the footnote reference. Readers can click the link to jump to the content of the footnote at the bottom of the page.

## Creating Footnotes

To create a footnote reference, add a caret and an identifier inside brackets ([^1]). Identifiers can be numbers or words, but they can't contain spaces or tabs.

```markdown
Here's a sentence with a footnote.[^1]

[^1]: This is the footnote content.
```

**Output**:

Here's a sentence with a footnote.[^1]

[^1]: This is the footnote content.

## Multiple Footnotes

You can add multiple footnotes in a document.

```markdown
This is the first reference.[^first]
This is the second reference.[^second]

[^first]: This is the first footnote.
[^second]: This is the second footnote.
```

**Output**:

This is the first reference.[^first]
This is the second reference.[^second]

[^first]: This is the first footnote.
[^second]: This is the second footnote.

## Footnote Content

Footnotes can contain multiple paragraphs or code blocks. Indent subsequent paragraphs by 4 spaces or 1 tab.

```markdown
Here's a footnote with multiple paragraphs.[^multipara]

[^multipara]: This is the first paragraph.

    This is the second paragraph.
    
    This is a third paragraph with more content.
```

## Inline Footnotes

Some Markdown processors support inline footnotes, where the footnote content is placed directly in the brackets.

```markdown
Here's an inline footnote.^[This is the inline footnote content.]
```

!!! note
    Inline footnotes are not supported in all Markdown processors.

## Best Practices

1. **Use descriptive identifiers**: Instead of `[^1]`, use `[^note-about-topic]`
2. **Place footnote definitions** at the end of your document or section
3. **Keep footnotes concise**: They should supplement, not replace, your main content
4. **Be consistent**: Use the same footnote style throughout your document

## Common Use Cases

### Academic Writing

```markdown
According to recent studies, Markdown is widely used.[^study2024]

[^study2024]: Smith, J. (2024). The Rise of Markdown in Technical Writing.
```

### Technical Documentation

```markdown
The API supports multiple authentication methods.[^auth]

[^auth]: OAuth 2.0, API keys, and JWT tokens are supported.
```

### Additional Information

```markdown
The software is available under the MIT License.[^license]

[^license]: See LICENSE.md for full terms and conditions.
```

## Limitations

- Some Markdown processors don't support footnotes
- Footnote formatting may vary between different processors
- Not all platforms support multi-paragraph footnotes

!!! tip
    If your Markdown processor doesn't support footnotes, consider using parenthetical citations or links instead.
