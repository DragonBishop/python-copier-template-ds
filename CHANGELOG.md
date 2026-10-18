## [2.0.0] - 2026-10-17

### 🚀 Features

- Add support for testing commit messages in cliff.toml
- Add renovate configuration for dependency management
- [**breaking**] Replace project questions with structure and tooling multi-selects
- Add Semgrep tooling option
- Add 7-day dependency cooldown

### 🐛 Bug Fixes

- Add README.md to _skip_if_exists in copier.yml

### ⚙️ Miscellaneous Tasks

- Pin GitHub Actions to commit SHAs
## [2.1.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v2.0.0...v2.1.0) (2026-10-18)


### 🚀 Features

* replace git-cliff with release-please changelog ([c777573](https://github.com/DragonBishop/python-copier-template-ds/commit/c7775738bff448b878c5bc760ff731fd61f909cb))
* replace git-cliff with release-please changelog ([9c881d9](https://github.com/DragonBishop/python-copier-template-ds/commit/9c881d9792ca76e506368e919927b82478972fef))


### 🐛 Bug Fixes

* always title-case the project display name ([8368382](https://github.com/DragonBishop/python-copier-template-ds/commit/8368382ca95d418e6968af60c0f88fd55c371d83))

## [1.7.1] - 2026-09-30

### 🐛 Bug Fixes

- Update justfile to initialize git with main branch and implement minot bug fixes on jinja templates
## [1.7.0] - 2026-09-23

### 🚀 Features

- Update release workflow to conditionally regenerate CHANGELOG.md and adjust commit messages
- Update release workflow to use GitHub App client ID and upgrade token action version
## [1.6.0] - 2026-09-20

### 🚀 Features

- *(release)* Authenticate release-please with GitHub App token
- Enhance configuration for project setup and release management, edit README for clarity and readability.

### ⚙️ Miscellaneous Tasks

- *(release)* Update version to 1.5.0 in pyproject.toml and uv.lock; adjust release-please config
## [1.5.0] - 2026-09-17

### 🚀 Features

- Add PyPI publishing support to the template

### ⚙️ Miscellaneous Tasks

- Use dedicated PAT for release-please instead of repo Actions permission
- *(template)* Use dedicated PAT for release-please
## [1.4.0] - 2026-08-31

### 🚀 Features

- Add GitHub Actions workflows for linting, testing, and release management
- Update configuration for GitHub Actions and improve markdown linting setup
- Add CI for template repo itself, including release-please, git-cliff, and linting. Updated python dependencies for project and template.
- Enhance README with detailed template options and project structure descriptions
- Add GITHUB_TOKEN to release workflow and update rumdl exclusions

### 🐛 Bug Fixes

- *(template)* Lint fixes caught by the new CI
## [1.3.1] - 2026-08-30

### 🚀 Features

- Make notebook tooling conditional on include_notebooks and update dependencies
- Make jupyter types_or conditional and allow multi-doc YAML in pre-commit
## [1.3.0] - 2026-08-24

### 🚀 Features

- Restore pre-commit and rumdl from upstream
## [1.2.1] - 2026-08-24

### 📚 Documentation

- Comment the copier-answers gitignore entry
## [1.2.0] - 2026-08-24

### 🚀 Features

- Make notebooks/ and reports/ optional, treat as one-time scaffolding
- Treat src/ as one-time scaffolding too
- Restore lint CI job and ruff dependency group from upstream
## [1.0.3] - 2026-08-05

### 🐛 Bug Fixes

- Correct conditional syntax in install command and improve git initialization check
## [1.0.2] - 2026-08-05

### 🐛 Bug Fixes

- Declare hatchling wheel packages explicitly
## [1.0.1] - 2026-08-02

### 🐛 Bug Fixes

- Corrections to issue forms missed in v1.0.0
## [1.0.0] - 2026-08-02

### 🚀 Features

- [**breaking**] Replace markdown issue templates with issue forms
## [0.1.1] - 2026-08-01

### 🚀 Features

- Add project type and module inclusion options to copier template; implement CI workflow and update README structure

### ⚙️ Miscellaneous Tasks

- Add GitHub issue templates for bug reports, documentation updates, feature proposals, and technical debt resolution
- Moved issue templates for bug reports, documentation updates, feature proposals, and technical debt resolution
- Update issue templates for consistency and clarity
- Update README and issue templates for consistency and clarity

### Refactor

- Remove pre-commit/Ruff, update README and template structure
## [0.1.2] - 2026-03-17
