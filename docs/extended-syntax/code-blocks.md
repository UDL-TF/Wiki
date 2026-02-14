# Code Blocks

Code blocks are essential for documenting code, displaying examples, and sharing snippets. While basic code blocks are part of the core Markdown syntax, many processors offer extended features.

## Fenced Code Blocks

The basic way to create a code block is with triple backticks (```).

````markdown
```
def hello_world():
    print("Hello, World!")
```
````

**Output**:

```
def hello_world():
    print("Hello, World!")
```

## Syntax Highlighting

You can add syntax highlighting by specifying a language after the opening backticks.

````markdown
```python
def hello_world():
    print("Hello, World!")
```
````

**Output**:

```python
def hello_world():
    print("Hello, World!")
```

## Supported Languages

Most Markdown processors support syntax highlighting for many languages:

- **Python**: `python` or `py`
- **JavaScript**: `javascript` or `js`
- **Java**: `java`
- **C/C++**: `c`, `cpp`
- **HTML**: `html`
- **CSS**: `css`
- **Bash**: `bash` or `shell`
- **JSON**: `json`
- **YAML**: `yaml`
- **SQL**: `sql`
- And many more...

## Examples by Language

### JavaScript

````markdown
```javascript
function greet(name) {
    return `Hello, ${name}!`;
}

console.log(greet("World"));
```
````

**Output**:

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}

console.log(greet("World"));
```

### Python

````markdown
```python
class Greeter:
    def __init__(self, name):
        self.name = name
    
    def greet(self):
        return f"Hello, {self.name}!"

greeter = Greeter("World")
print(greeter.greet())
```
````

**Output**:

```python
class Greeter:
    def __init__(self, name):
        self.name = name
    
    def greet(self):
        return f"Hello, {self.name}!"

greeter = Greeter("World")
print(greeter.greet())
```

### JSON

````markdown
```json
{
    "name": "Markdown Guide",
    "version": "1.0.0",
    "features": [
        "Syntax highlighting",
        "Code blocks",
        "Tables"
    ]
}
```
````

**Output**:

```json
{
    "name": "Markdown Guide",
    "version": "1.0.0",
    "features": [
        "Syntax highlighting",
        "Code blocks",
        "Tables"
    ]
}
```

### Bash

````markdown
```bash
#!/bin/bash

echo "Hello, World!"

for i in {1..5}; do
    echo "Count: $i"
done
```
````

**Output**:

```bash
#!/bin/bash

echo "Hello, World!"

for i in {1..5}; do
    echo "Count: $i"
done
```

## Indented Code Blocks

The traditional way to create a code block is to indent every line by at least four spaces or one tab.

```
    def hello_world():
        print("Hello, World!")
```

This creates:

    def hello_world():
        print("Hello, World!")

!!! note
    Indented code blocks don't support syntax highlighting. Use fenced code blocks for that feature.

## Inline Code

For inline code, use single backticks.

```markdown
Use the `print()` function to output text.
```

**Output**: Use the `print()` function to output text.

## Escaping Backticks

If you need to show backticks inside inline code, use double backticks.

```markdown
``Use `backticks` for code``
```

**Output**: ``Use `backticks` for code``

## Best Practices

1. **Always specify the language** for syntax highlighting
2. **Use descriptive variable names** in examples
3. **Keep code examples concise** and focused
4. **Test your code** before including it in documentation
5. **Add comments** to explain complex code
