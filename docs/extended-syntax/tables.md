# Tables

Tables aren't part of the core Markdown specification, but many Markdown processors support them. They're a great way to organize information.

## Creating Tables

To create a table, use three or more hyphens (---) to create each column's header, and use pipes (|) to separate each column.

```markdown
| Header 1 | Header 2 | Header 3 |
| -------- | -------- | -------- |
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |
| Row 3    | Data     | Data     |
```

**Output**:

| Header 1 | Header 2 | Header 3 |
| -------- | -------- | -------- |
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |
| Row 3    | Data     | Data     |

## Alignment

You can align text in the columns to the left, right, or center by adding a colon (:) to the left, right, or on both sides of the hyphens within the header row.

```markdown
| Left Aligned | Center Aligned | Right Aligned |
| :----------- | :------------: | ------------: |
| Left         | Center         | Right         |
| Left         | Center         | Right         |
```

**Output**:

| Left Aligned | Center Aligned | Right Aligned |
| :----------- | :------------: | ------------: |
| Left         | Center         | Right         |
| Left         | Center         | Right         |

## Formatting Text in Tables

You can format text within tables using standard Markdown formatting.

```markdown
| Syntax      | Description |
| ----------- | ----------- |
| **Bold**    | Bold text   |
| *Italic*    | Italic text |
| `Code`      | Code text   |
| [Link](#)   | Link text   |
```

**Output**:

| Syntax      | Description |
| ----------- | ----------- |
| **Bold**    | Bold text   |
| *Italic*    | Italic text |
| `Code`      | Code text   |
| [Link](#)   | Link text   |

## Tips for Creating Tables

- You don't need to make the columns line up perfectly in the raw Markdown
- You can include leading and trailing pipes
- Cell widths can vary
- You can escape pipe characters using a backslash (\\|)

## Example: Complex Table

```markdown
| Feature        | Support | Notes                    |
| :------------- | :-----: | :----------------------- |
| Headers        | ✓       | Required                 |
| Alignment      | ✓       | Optional                 |
| Formatting     | ✓       | Most Markdown supported  |
| Multiple lines | ✗       | Not widely supported     |
```

**Output**:

| Feature        | Support | Notes                    |
| :------------- | :-----: | :----------------------- |
| Headers        | ✓       | Required                 |
| Alignment      | ✓       | Optional                 |
| Formatting     | ✓       | Most Markdown supported  |
| Multiple lines | ✗       | Not widely supported     |
