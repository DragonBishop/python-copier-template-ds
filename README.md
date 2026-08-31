# Python Copier Template for Data Science

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border-orange.json)](https://github.com/copier-org/copier)

This is a template to generate a data science focused python project built with [Copier](https://github.com/copier-org/copier). It is based on the template created by Felix G. Williams, which you can find at [https://github.com/felixgwilliams/python-copier-template-ds/tree/main](https://github.com/felixgwilliams/python-copier-template-ds/tree/main). It borrows the report and notebook scaffolding of the Cookiecutter Data Science template, trims it down, and swaps its `pip`/`make`-based workflow for `uv` and `just`, so the generated project's structure stays flexible: notebooks, reports, an installable module, and a `src/` layout are each opt-in per project rather than assumed. It also removes the data folder to keep github repositories lean while the data is stored elsewhere, e.g. Kaggle.

Get started with the following command:

```shell
copier copy gh:DragonBishop/python-copier-template-ds path/to/destination
```

## Table of Contents

* [Template Options](#template-options)
* [Features](#features)
  * [Project Structure](#project-structure)
  * [just](#just)
  * [uv](#uv)
  * [nbwipers](#nbwipers)
  * [pytest](#pytest)
  * [prek](#prek)
  * [Github Actions](#github-actions)
* [Development](#development)
* [Repository Structure](#repository-structure)
  * [File Descriptions](#file-descriptions)

---

## Template Options

These `copier.yml` questions shape the generated project's structure:

| Question | Type | Default | Effect |
| --- | --- | --- | --- |
| `project_name` | `str` | none | Project name. `module_name` defaults to this value, slugified. |
| `project_type` | choice | `data_analysis` | `data_science` adds `features/` and `models/` alongside `data/` and `visualization/`, plus a top-level `models/` folder for trained artifacts. `data_analysis` keeps just `data/` and `visualization/`. |
| `include_module` | `bool` | `true` | Whether the above lives in an installable package under `src/{{module_name}}/`, or as plain unpackaged folders under `src/` for standalone scripts. With no module, the project does not require build steps. |
| `module_name` | `str` | slugified `project_name` | Python module name; only asked when `include_module` is true. |
| `include_notebooks` | `bool` | `true` | Scaffolds a `notebooks/` folder with starter notebooks. |
| `include_reports` | `bool` | `true` | Scaffolds a `reports/` folder for a write-up, cleaning log, and bibliography. |
| `python_version` | `str` | `3.14.7` | Pinned in `.python-version` and `pyproject.toml`'s `requires-python`. |
| `github_actions` | `bool` | `true` | Adds `lint`/`tests` workflows, plus release-please + git-cliff versioning and changelog automation. |
| `use_rumdl` | `bool` | `true` | Include markdown linting with [rumdl](https://github.com/rvben/rumdl). |

`notebooks/`, `reports/`, and `src/` are one-time scaffolding: `copier update` won't re-create or overwrite them once they exist, so you're free to restructure or remove them afterward.

---

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

### [prek](https://github.com/j178/prek)

`prek` runs checks on your files before you commit them with git, catching lint and formatting issues before they land. It's a Rust reimplementation of [pre-commit](https://github.com/pre-commit/pre-commit): a single binary with no Python dependency, faster, and fully compatible with the same `.pre-commit-config.yaml` format. Set it up with

```shell
prek install --prepare-hooks
```

The configuration is stored in `.pre-commit-config.yaml`, and includes basic file hygiene and `ruff` check/format. When `use_rumdl` is true, it also includes markdown linting with [rumdl](https://github.com/rvben/rumdl).

### Github Actions

You may optionally add github workflows: a `lint` job that runs `ruff check` and `ruff format --check`, a `tests` job that runs `pytest` with coverage, and a `release` workflow that automates versioning with [release-please](https://github.com/googleapis/release-please) and regenerates `CHANGELOG.md` with [git-cliff](https://github.com/orhun/git-cliff) whenever a release is cut. `.yaml` issue templates are included for use on github.

---

## Development

This repository's own dev tooling lives at the root, not under `template/`. Set it up with

```shell
uv sync --group dev
```

which installs [Copier](https://github.com/copier-org/copier), [copier-template-tester](https://github.com/KyleKing/copier-template-tester) (`ctt`), [rumdl](https://github.com/rvben/rumdl), [yamllint](https://github.com/adrienverge/yamllint), and [j2lint](https://github.com/aristanetworks/j2lint).

* `uv run ctt` renders the template variants configured in `ctt.toml` into `.ctt/` and reports pass/fail.
* `uv run rumdl check .` lints this repository's own markdown.
* `uv run yamllint .` lints this repository's own YAML: workflows, issue templates, and `copier.yml`.
* `uv run j2lint template -i jinja-statements-delimiter single-statement-per-line jinja-statements-indentation` lints the Jinja templates under `template/`. Those three rules are ignored because they conflict with this template's single-line file/directory-name conditionals and `{%- -%}` whitespace control.

CI (`.github/workflows/lint.yml` and `test-template.yml`) runs the same checks, plus renders every `ctt.toml` variant and runs `ruff`/`pytest` against the rendered output.

---

## Repository Structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/                          # Bug/documentation/feature/tech-debt issue forms
│   └── workflows/
│       ├── lint.yml                             # rumdl + yamllint + j2lint on this repo's own files
│       ├── test-template.yml                    # renders every ctt.toml variant, then ruff/pytest against each
│       └── release.yml                          # PR-title lint + release-please + git-cliff changelog
├── template/                                    # _subdirectory in copier.yml; everything Copier renders
│   ├── {{ _copier_conf.answers_file }}.jinja    # writes .copier-answers.yml into the generated project
│   ├── .github/
│   │   ├── ISSUE_TEMPLATE/                      # copied as-is into generated projects
│   │   └── {% if github_actions %}workflows{% endif %}/
│   │       ├── lint.yml
│   │       ├── tests.yml.jinja
│   │       └── release.yml
│   ├── {% if github_actions %}cliff.toml{% endif %}
│   ├── {% if github_actions %}release-please-config.json{% endif %}.jinja
│   ├── {% if github_actions %}.release-please-manifest.json{% endif %}
│   ├── {% if include_notebooks %}notebooks{% endif %}/
│   │   ├── data_analysis_notebook.ipynb.jinja
│   │   └── data_processing_notebook.ipynb.jinja
│   ├── {% if include_reports %}reports{% endif %}/
│   │   ├── cleaning_log.md.jinja
│   │   ├── REPORT.md.jinja
│   │   └── figures/
│   ├── {% if project_type == 'data_analysis' %}README.md{% endif %}.jinja
│   ├── {% if project_type == 'data_science' %}README.md{% endif %}.jinja
│   ├── src/
│   │   └── {% if include_module %}{{module_name}}{% endif %}/  # installable package; data_science adds features/, models/
│   │       ├── data/
│   │       ├── visualization/
│   │       ├── {% if project_type == 'data_science' %}features{% endif %}/
│   │       └── {% if project_type == 'data_science' %}models{% endif %}/
│   ├── tests/
│   ├── justfile.jinja
│   ├── .pre-commit-config.yaml.jinja
│   ├── pyproject.toml.jinja
│   ├── .python-version.jinja
│   ├── .gitignore.jinja
│   └── .gitattributes
├── copier.yml                                    # Template questions and defaults
├── ctt.toml                                      # copier-template-tester scenarios, renders into .ctt/, gitignored
├── cliff.toml                                    # This repo's own changelog config
├── release-please-config.json
├── .release-please-manifest.json
├── .yamllint.yml
├── pyproject.toml                                # This repo's own dev tooling, not a package
├── .python-version
├── uv.lock
├── LICENSE
└── README.md
```

### File Descriptions

* **`.github/`**
  * **`ISSUE_TEMPLATE/`**: Issue templates for bug reports, documentation updates, feature proposals, and technical-debt resolution.
  * **`workflows/lint.yml`**: Lints this repository's own files. Runs `rumdl` for markdown, `yamllint` for YAML, and `j2lint` for the Jinja templates under `template/`.
  * **`workflows/test-template.yml`**: Renders every `ctt.toml` variant, then runs `ruff format --check`, `ruff check`, and `pytest` against each rendered output.
  * **`workflows/release.yml`**: Lints the PR title against Conventional Commits. On push, `release-please` opens or updates a release PR, and once a release is tagged, regenerates this repo's own `CHANGELOG.md` with `git-cliff`.
* **`template/`**: the Copier source tree. Directory and file names built from `{% if %}`/`{% endif %}` are how Copier conditionally includes or renames a path per the answers in [Template Options](#template-options). `{{ variable }}` names are filled in from those same answers.
  * **`{{ _copier_conf.answers_file }}.jinja`**: Renders `.copier-answers.yml` into the generated project, recording the answers used for later `copier update` runs.
  * **`.github/ISSUE_TEMPLATE/`**: Copied into the generated project as-is.
  * **`.github/{% if github_actions %}workflows{% endif %}/`**: `lint.yml` runs ruff, `tests.yml.jinja` runs pytest with a coverage flag conditional on `include_module`, and `release.yml` runs PR-title lint plus release-please and git-cliff. All three are only included when `github_actions` is true.
  * **`{% if github_actions %}cliff.toml{% endif %}`**, **`{% if github_actions %}release-please-config.json{% endif %}.jinja`**, **`{% if github_actions %}.release-please-manifest.json{% endif %}`**: Changelog and release-please config for the generated project, only included when `github_actions` is true.
  * **`{% if include_notebooks %}notebooks{% endif %}/`**: Starter notebooks for data processing and analysis, only included when `include_notebooks` is true.
  * **`{% if include_reports %}reports{% endif %}/`**: Write-up, cleaning log, and a `figures/` folder, only included when `include_reports` is true.
  * **`{% if project_type == 'data_analysis' %}README.md{% endif %}.jinja`**, **`{% if project_type == 'data_science' %}README.md{% endif %}.jinja`**: The generated project's own README, one variant per `project_type`. Exactly one renders.
  * **`src/{% if include_module %}{{module_name}}{% endif %}/`**: The installable package when `include_module` is true, or unpackaged folders directly under `src/` otherwise. `data/` and `visualization/` are always present; `features/` and `models/` are added when `project_type` is `data_science`.
  * **`tests/`**: `pytest` fixtures and an example test, always included.
  * **`justfile.jinja`**, **`.pre-commit-config.yaml.jinja`**, **`pyproject.toml.jinja`**, **`.python-version.jinja`**, **`.gitignore.jinja`**, **`.gitattributes`**: Generated project's root-level tooling config.
* **`copier.yml`**: The questions and defaults documented in [Template Options](#template-options).
* **`ctt.toml`**: [copier-template-tester](https://github.com/KyleKing/copier-template-tester) scenarios, currently `no-ci` and `ci`, varying `github_actions`. Rendered into `.ctt/` by `uv run ctt`.
* **`cliff.toml`**, **`release-please-config.json`**, **`.release-please-manifest.json`**: This repository's own git-cliff and release-please configuration. Uses `release-type: simple`, since there's no packaged code here whose version needs bumping.
* **`.yamllint.yml`**: `yamllint` config for this repository's own YAML.
* **`pyproject.toml`**, **`.python-version`**, **`uv.lock`**: This repository's own dev-tooling environment: `copier`, `copier-template-tester`, `rumdl`, `yamllint`, and `j2lint`. Not a Python package; see [Development](#development).
