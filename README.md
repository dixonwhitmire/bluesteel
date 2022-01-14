# Bluesteel
Bluesteel generates data models for standard healthcare protocols

## Overview
Coming soon!

## QuickStart

### Pre-requisites
The LinuxForHealth bluesteel development environment relies on the following software packages:

- [git](https://git-scm.com) for project version control
- [Python 3.8 or higher](https://www.python.org/downloads/) for runtime/coding support

### Project Setup and Validation
```shell
pip install --upgrade pip setuptools

git clone https://github.com/LinuxForHealth/bluesteel
cd bluesteel

python3 -m venv venv && source venv/bin/activate && pip install --upgrade pip setuptools 
pip install -e .[dev]
pytest
```


### Code Formatting

LinuxForHealth bluesteel adheres to the [Black Code Style and Convention](https://black.readthedocs.io/en/stable/index.html)

The following command executes the black formatter with default options

```shell
user@mbp bluesteel % source venv/bin/activate
(venv) user@mbp bluesteel % black ./src
```

Use the `--help` flag to view all available options for the black code formatter

```shell
(venv) user@mbp bluesteel % black --help
```

## Building The Project
LinuxForHealth bluesteel is aligned, to a degree, with the PEP-517 standard. `setup.cfg` stores build metadata/configuration.
`pyproject.toml` contains the build toolchain specification and black formatter configurations.

The commands below creates a source and wheel distribution within a clean build environment.

```shell
python3 -m venv build-venv && source build-venv/bin/activate && pip install --upgrade pip setuptools build wheel twine
python3 -m build --no-isolation
```
