# copier_template_example

A simple Python project template using Copier. This template creates a basic Python project structure with src/, test/, configuration files, and GitHub Actions.

## Features

- **Python Package Structure**: Organized with `src/` and `test/` directories
- **Build Configuration**: Modern `pyproject.toml` setup
- **Docker Support**: Dockerfile included for containerization
- **GitHub Actions**: Pre-configured workflow that greets your project
- **Testing**: pytest configuration ready to use
- **Type Hints**: Python code includes type annotations

## Prerequisites

Install Copier:

```bash
pip install copier
```

## Usage

Create a new project from this template:

```bash
copier copy gh:kdrivas/copier_template_example my-new-project
```

Or if you have the template locally:

```bash
copier copy /path/to/copier_template_example my-new-project
```

You'll be prompted to answer a few questions:
- **project_name**: The name of your Python package (e.g., `my_project`)
- **project_description**: A short description of your project
- **author_name**: Your name
- **author_email**: Your email address
- **python_version**: Python version to use (3.9, 3.10, 3.11, or 3.12)

## Generated Project Structure

```
my_project/
├── .github/
│   └── workflows/
│       └── hello.yml          # GitHub Actions workflow
├── src/
│   └── my_project/
│       ├── __init__.py
│       └── main.py            # Main module with sample code
├── test/
│   ├── __init__.py
│   └── test_main.py           # Sample tests
├── .gitignore
├── Dockerfile                  # Docker configuration
├── pyproject.toml             # Project configuration
└── README.md                   # Project documentation
```

## What's Included

### Source Code
The template includes a simple Python module with:
- A `greet()` function with type hints
- A `main()` entry point
- Proper docstrings

### Tests
Basic pytest tests are included to validate the generated code.

### Configuration
- **pyproject.toml**: Modern Python packaging configuration with setuptools
- **pytest configuration**: Ready to run tests
- **Docker**: Simple Dockerfile to containerize your application

### GitHub Actions
A simple workflow that prints "hello {project_name}" on push/pull request.

## Using the Generated Project

After creating a project from this template:

1. **Install the package**:
   ```bash
   cd my-new-project
   pip install -e ".[dev]"
   ```

2. **Run tests**:
   ```bash
   pytest
   ```

3. **Run the application**:
   ```bash
   python -m my_project.main
   # Or use the console script:
   my_project
   ```

4. **Build Docker image**:
   ```bash
   docker build -t my_project .
   docker run my_project
   ```

## Updating a Project

To update an existing project created from this template:

```bash
cd my-new-project
copier update
```

## Contributing

Feel free to submit issues or pull requests to improve this template.

## License

This template is provided as-is for use in creating new projects.