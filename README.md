# Python Copier Template for Data Science

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border-orange.json)](https://github.com/copier-org/copier)

This is a template to generate a data science focused python project built with [Copier](https://github.com/copier-org/copier). It is based on the template created by Felix G. Williams, which you can find at [https://github.com/felixgwilliams/python-copier-template-ds/tree/main](https://github.com/felixgwilliams/python-copier-template-ds/tree/main). It removes the linting, pre-commit, and rumdl features, and alters the template to bring it into alignment with the CookieCutter template. It also removes the data folder to keep github repositories lean while the data is stored elsewhere (e.g. Kaggle).

Get started with the following command:

```shell
copier copy gh:DragonBishop/python-copier-template-ds path/to/destination
```

## Project Type

Two questions shape the generated project:

- **`project_type`** — `data_science` adds `features/` and `models/` (plus a top-level `models/` folder for trained artifacts) alongside `data/` and `visualization/`; `data_analysis` keeps just `data/` and `visualization/`.
- **`include_module`** — whether any of the above lives in an installable package under `src/{{module_name}}/`, or as plain unpackaged folders under `src/` for standalone scripts. With no module, the project does not require build steps — just notebooks, reports, and scripts.

## Features

### Project structure

It is assumed that most of the work will be done in Jupyter Notebooks.
The template also includes a `src/` layout for functions and scripts shared across notebooks, whether or not that's an installable package.
The repository is set up to use [Pytest](https://docs.pytest.org/en/stable/) for unit testing.

### [just](https://github.com/casey/just)

`just` is a command runner that allows you to easily to run project-specific commands.
In fact, you can use `just` to run all the setup commands listed below:

```shell
just setup
```

### [uv](https://github.com/astral-sh/uv)

The repository is set up to use [uv](https://github.com/astral-sh/uv) for package or project management.
You may set up your python environment with

```shell
uv sync --all-groups --all-extras
```

### [nbwipers](https://github.com/felixgwilliams/nbwipers)

`nbwipers` is a tool written in rust to ensure Jupyter notebooks are clean.
Committing notebooks that are not clean makes diffs more confusing, can degrade performance and increases the risk of leaking sensitive information.
Set it up as a git filter with the following command.

```shell
uv run nbwipers install local
```

### [pytest](https://docs.pytest.org/en/stable/)

The repository comes configured to use `pytest` for unit testing. If there's no module (`include_module: false`), tests run without coverage, since there's no package to measure.

### Github Actions

You may optionally add a github workflow file which runs unit tests and checks coverage.

Test with [Copier](https://github.com/copier-org/copier) and [copier-template-tester](https://github.com/KyleKing/copier-template-tester).
