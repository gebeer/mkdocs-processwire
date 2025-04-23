# ProcessWire API Documentation Markdown

This repository contains a MkDocs setup for testing and previewing ProcessWire API documentation in Markdown format. The actual Markdown documentation is provided by a separate repository.

## Current State

- Basic MkDocs configuration with Material theme
- Minimal placeholder documentation in the `docs/` directory
- Python 3.11.9 virtual environment with MkDocs and required dependencies
- Dark mode enabled by default

The project is currently set up as follows:
- `.venv/`: Python virtual environment with MkDocs and dependencies
- `docs/`: Contains placeholder Markdown files for testing
  - `index.md`: Main landing page
  - `classes/`: Directory for class documentation
    - `cache/`: Example class documentation
- `mkdocs.yml`: MkDocs configuration file

## Switching to uv for Python Package Management

[uv](https://github.com/astral-sh/uv) is a fast Python package manager and installer written in Rust. It offers significant performance improvements over traditional tools like pip. Here's how to use uv for this project:

### Installation

```bash
# Install uv
curl -sSf https://astral.sh/uv/install.sh | sh
```

### Project Initialization with uv

```bash
# Initialize a new project (creates pyproject.toml and virtual environment)
uv init
```

This will create a `pyproject.toml` file to manage dependencies and automatically set up a virtual environment.

### Managing Dependencies with uv

```bash
# Add dependencies
uv add mkdocs mkdocs-material pymdown-extensions ghp-import

# Remove a dependency
uv remove <package-name>

# Update dependencies and sync environment
uv sync
```

### Running MkDocs with uv

```bash
# Start the development server
uv run -- mkdocs serve

# Build the static site
uv run -- mkdocs build

# Deploy to GitHub Pages
uv run -- mkdocs gh-deploy
```

The `uv run` command ensures that all dependencies are up-to-date before executing the command.

## Usage

1. Clone this repository
2. Initialize the project with `uv init`
3. Add required dependencies with `uv add mkdocs mkdocs-material`
4. Place your ProcessWire API Markdown documentation in the `docs/` directory
5. Run `uv run -- mkdocs serve` to preview the documentation
6. Run `uv run -- mkdocs build` to build the static site

## License

This project is for testing purposes only. The ProcessWire API documentation is subject to its own licensing terms.
