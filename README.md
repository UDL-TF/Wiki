# Markdown Guide

A comprehensive guide to Markdown syntax and usage, published at [wiki.udl.tf](https://wiki.udl.tf).

## About

This repository contains a complete Markdown guide built with [MkDocs](https://www.mkdocs.org/) and the [Material theme](https://squidfunk.github.io/mkdocs-material/). The guide covers everything from basic syntax to extended features and best practices.

## Features

- 📚 Complete Markdown syntax reference
- 🎨 Modern, responsive design with dark/light mode
- 🔍 Built-in search functionality
- 📱 Mobile-friendly layout
- 🚀 Automatically deployed to wiki.udl.tf

## Content

The guide includes:

- **Getting Started**: Introduction and basic syntax
- **Extended Syntax**: Tables, code blocks, footnotes, and task lists
- **Reference**: Cheat sheet and best practices

## Local Development

### Prerequisites

- Python 3.x
- pip

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/UDL-TF/Wiki.git
   cd Wiki
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Serve the site locally:
   ```bash
   mkdocs serve
   ```

4. Open your browser to `http://127.0.0.1:8000`

### Building

To build the static site:

```bash
mkdocs build
```

The built site will be in the `site/` directory.

## Deployment

The site is automatically deployed to GitHub Pages (wiki.udl.tf) when changes are pushed to the `main` branch using GitHub Actions.

## Contributing

Contributions are welcome! Feel free to:

- Report issues
- Suggest improvements
- Submit pull requests

## License

This project is licensed under the terms specified in the LICENSE file.
