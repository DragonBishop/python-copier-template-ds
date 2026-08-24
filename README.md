# Python Copier Template for Data Science

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border-orange.json)](https://github.com/copier-org/copier)

This is a template to generate a data science focused python project built with [Copier](https://github.com/copier-org/copier). It is based on the template created by Felix G. Williams, which you can find at [https://github.com/felixgwilliams/python-copier-template-ds/tree/main](https://github.com/felixgwilliams/python-copier-template-ds/tree/main). It borrows the report and notebook scaffolding of the Cookiecutter Data Science template, trims it down, and swaps its `pip`/`make`-based workflow for `uv` and `just`, so the generated project's structure stays flexible: notebooks, reports, an installable module, and a `src/` layout are each opt-in per project rather than assumed. It also removes the data folder to keep github repositories lean while the data is stored elsewhere (e.g. Kaggle).

Get started with the following command:

```shell
copier copy gh:DragonBishop/python-copier-template-ds path/to/destination
```

## Project Type

Several questions shape the generated project's structure:

- **`project_type`** — `data_science` adds `features/` and `models/` (plus a top-level `models/` folder for trained artifacts) alongside `data/` and `visualization/`; `data_analysis` keeps just `data/` and `visualization/`.
- **`include_module`** — whether any of the above lives in an installable package under `src/{{module_name}}/`, or as plain unpackaged folders under `src/` for standalone scripts. With no module, the project does not require build steps — just notebooks, reports, and scripts.
- **`include_notebooks`** — whether a `notebooks/` folder with starter notebooks is scaffolded.
- **`include_reports`** — whether a `reports/` folder (write-up, cleaning log, bibliography) is scaffolded.

`notebooks/`, `reports/`, and `src/` are one-time scaffolding: `copier update` won't re-create or overwrite them once they exist, so you're free to restructure or remove them afterward.

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

### [prek](https://github.com/j178/prek) and [pre-commit](https://github.com/pre-commit/pre-commit)

`prek` and `pre-commit` run checks on your files before you commit them with git, catching lint and formatting issues before they land. `prek` is a Rust reimplementation of `pre-commit`: a single binary with no Python dependency, faster, and fully compatible with the same `.pre-commit-config.yaml` format.

Depending on your answer to `use_prek`, set it up with one of

```shell
prek install --prepare-hooks
```

```shell
pre-commit install --install-hooks
```

The configuration for either is stored in `.pre-commit-config.yaml`, and includes basic file hygiene, `ruff` check/format, and a markdown linter — [rumdl](https://github.com/rvben/rumdl) by default, or [markdownlint-cli2](https://github.com/DavidAnson/markdownlint-cli2) if you answer `use_rumdl: false`.

### Github Actions

You may optionally add a github workflow file with a `lint` job (`ruff check` / `ruff format --check`) and a `tests` job (`pytest` with coverage). `.yaml` issue templates are included for use on github.

Test with [Copier](https://github.com/copier-org/copier) and [copier-template-tester](https://github.com/KyleKing/copier-template-tester).
