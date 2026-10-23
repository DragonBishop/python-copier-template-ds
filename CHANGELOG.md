## [2.2.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v2.1.0...v2.2.0) - 2026-10-23

### 🚀 Features

- Link commit hashes and versions in git-cliff changelogs ([01d14ad](https://github.com/DragonBishop/python-copier-template-ds/commit/01d14ada7843429466c54853b8acd41d56f9bd7e))

### 🐛 Bug Fixes

- *(deps)* Update template dependencies ([10893c5](https://github.com/DragonBishop/python-copier-template-ds/commit/10893c5c7d3da59b3ed0006167a33adb32e97e1f))
- *(deps)* Update actions/checkout action to v7 ([bf73d4f](https://github.com/DragonBishop/python-copier-template-ds/commit/bf73d4f79649d46e9be72e01f333a52ac4405421))
- *(deps)* Update actions/setup-python action to v7 ([f1ab275](https://github.com/DragonBishop/python-copier-template-ds/commit/f1ab275acfeef096f96e5417d8333f4adf573e88))

### 📚 Documentation

- Copy the template from its full git URL ([a511132](https://github.com/DragonBishop/python-copier-template-ds/commit/a5111327dd7d279510d2bbad84eef03ef76d3bae))

### ⚙️ Miscellaneous Tasks

- Run workflows on main ([d33cd0e](https://github.com/DragonBishop/python-copier-template-ds/commit/d33cd0ea0959f9c64d9546b5b224b87042fc8b31))

## [2.1.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v2.0.0...v2.1.0) - 2026-10-19

### 🚀 Features

- *(renovate)* Group minor and patch updates into one PR ([781aa2f](https://github.com/DragonBishop/python-copier-template-ds/commit/781aa2fc0cc0e57c6ee9710a47e43ef4ef15923b))

### ⚙️ Miscellaneous Tasks

- Skip tests on release-only PRs ([fc9185c](https://github.com/DragonBishop/python-copier-template-ds/commit/fc9185c0c72defb5998b71533b29780391f96a7f))

## [2.0.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.7.1...v2.0.0) - 2026-10-19

### 🚀 Features

- Add support for testing commit messages in cliff.toml ([ebd1d40](https://github.com/DragonBishop/python-copier-template-ds/commit/ebd1d403f144d7b1d1229ab965380d38d7eb2680))
- Add renovate configuration for dependency management ([1c130fe](https://github.com/DragonBishop/python-copier-template-ds/commit/1c130fe44a0212fd15c7499b3385fece1ca92b89))
- Add Renovate config as a tooling option ([ec096bd](https://github.com/DragonBishop/python-copier-template-ds/commit/ec096bd52e6eb435a7af178539c3ace2bec133bf))
- [**breaking**] Replace project questions with structure and tooling multi-selects ([1f4a6bb](https://github.com/DragonBishop/python-copier-template-ds/commit/1f4a6bb737eeb004e0301f583fb47aa89f7c2e9b))
- Add Semgrep tooling option ([21b320e](https://github.com/DragonBishop/python-copier-template-ds/commit/21b320eeebd6d4161f1af85bfcb891e336e1079b))
- Add 7-day dependency cooldown ([6c80726](https://github.com/DragonBishop/python-copier-template-ds/commit/6c807263eaa75810493cc95e201b8f5e37e16070))
- Lint PR commits instead of PR titles ([626c072](https://github.com/DragonBishop/python-copier-template-ds/commit/626c0724d79909a820237928a1e03963ab49702e))

### 🐛 Bug Fixes

- Add README.md to _skip_if_exists in copier.yml ([85fe08e](https://github.com/DragonBishop/python-copier-template-ds/commit/85fe08e93b7fefda269a64dfe9601ca406624491))
- Write GitHub release notes with git-cliff ([88cb455](https://github.com/DragonBishop/python-copier-template-ds/commit/88cb455017a49553ce3e5f4eba1cf85247ce1679))

### 📚 Documentation

- Consolidate commit and PR requirements into one section ([5e72c0e](https://github.com/DragonBishop/python-copier-template-ds/commit/5e72c0e41c4dd341cd0c52b7422ee3114ea4b992))

### ♻️ Refactor

- [**breaking**] Always generate the module under src/ ([ba0f8c5](https://github.com/DragonBishop/python-copier-template-ds/commit/ba0f8c5f21a40a2316c1cdc86066752b9c6f85f3))
- [**breaking**] Merge the README variants and gate notebooks/reports on structure ([c2a593a](https://github.com/DragonBishop/python-copier-template-ds/commit/c2a593ac9380b8f8b52b6d147f0a40ed6b578c63))
- [**breaking**] Gate workflows and release files on tooling choices ([53666bf](https://github.com/DragonBishop/python-copier-template-ds/commit/53666bf272ed93fcdeecdac0f6a271e6fa6e25b3))

### ⚙️ Miscellaneous Tasks

- Pin GitHub Actions to commit SHAs ([7cea3de](https://github.com/DragonBishop/python-copier-template-ds/commit/7cea3dee8a090c866c2b02ba7548c02929c77869))
- Scan this repo with Semgrep ([c098407](https://github.com/DragonBishop/python-copier-template-ds/commit/c098407b4f0c308b00180c4158178b67832bf99d))

## [1.7.1](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.7.0...v1.7.1) - 2026-09-30

### 🐛 Bug Fixes

- Update justfile to initialize git with main branch and implement minot bug fixes on jinja templates ([f8c9928](https://github.com/DragonBishop/python-copier-template-ds/commit/f8c9928c483abd0cdc2993f79e677a5cd9ac9fa7))

## [1.7.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.6.0...v1.7.0) - 2026-09-23

### 🚀 Features

- Update release workflow to conditionally regenerate CHANGELOG.md and adjust commit messages ([b797a87](https://github.com/DragonBishop/python-copier-template-ds/commit/b797a87dc31b3055b1f08b84cb04785092c88116))
- Update release workflow to use GitHub App client ID and upgrade token action version ([c04f9b4](https://github.com/DragonBishop/python-copier-template-ds/commit/c04f9b41df8289af5bb045d7f914efd46c18e2ff))

## [1.6.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.5.0...v1.6.0) - 2026-09-20

### 🚀 Features

- *(release)* Authenticate release-please with GitHub App token ([64e6966](https://github.com/DragonBishop/python-copier-template-ds/commit/64e6966e83ef679cbcd1527d13a7b1e50363d606))
- Enhance configuration for project setup and release management, edit README for clarity and readability. ([303d74c](https://github.com/DragonBishop/python-copier-template-ds/commit/303d74c400b5555d409e3ceffa4c072324adf745))

### ⚙️ Miscellaneous Tasks

- *(release)* Update version to 1.5.0 in pyproject.toml and uv.lock; adjust release-please config ([336887f](https://github.com/DragonBishop/python-copier-template-ds/commit/336887fa8977abd2c41b201f503f6229ebb3d3dc))

## [1.5.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.4.0...v1.5.0) - 2026-09-17

### 🚀 Features

- Add PyPI publishing support to the template ([41150ff](https://github.com/DragonBishop/python-copier-template-ds/commit/41150ff30ca0b340d44914ea6ff10a66fb84dbad))

### ⚙️ Miscellaneous Tasks

- Use dedicated PAT for release-please instead of repo Actions permission ([5085b5e](https://github.com/DragonBishop/python-copier-template-ds/commit/5085b5eda40304e3e53b89d120c189e89c1a2338))
- *(template)* Use dedicated PAT for release-please ([e2e2681](https://github.com/DragonBishop/python-copier-template-ds/commit/e2e2681fff1df50c2930d69a14c712ab9c571f7b))

## [1.4.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.3.1...v1.4.0) - 2026-08-31

### 🚀 Features

- Add GitHub Actions workflows for linting, testing, and release management ([8227f4c](https://github.com/DragonBishop/python-copier-template-ds/commit/8227f4c607df6d576f77498af6f7c39bae86b28a))
- Update configuration for GitHub Actions and improve markdown linting setup ([4e48ebe](https://github.com/DragonBishop/python-copier-template-ds/commit/4e48ebe708b350cd260192b657d6202192cbcaee))
- Add CI for template repo itself, including release-please, git-cliff, and linting. Updated python dependencies for project and template. ([f88ed2c](https://github.com/DragonBishop/python-copier-template-ds/commit/f88ed2ca475d5abfdce5e0f09876e9fda0d68746))
- Enhance README with detailed template options and project structure descriptions ([a87c93e](https://github.com/DragonBishop/python-copier-template-ds/commit/a87c93eb49f96ff497c81912805b267e6c2dfa0b))
- Add GITHUB_TOKEN to release workflow and update rumdl exclusions ([c534f39](https://github.com/DragonBishop/python-copier-template-ds/commit/c534f39479323add929ee95ab50a78c8c9fd7d6d))

### 🐛 Bug Fixes

- *(template)* Lint fixes caught by the new CI ([f4601d0](https://github.com/DragonBishop/python-copier-template-ds/commit/f4601d095585a7349464bf24971f76e434d457be))

## [1.3.1](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.3.0...v1.3.1) - 2026-08-30

### 🚀 Features

- Make notebook tooling conditional on include_notebooks and update dependencies ([cde17cc](https://github.com/DragonBishop/python-copier-template-ds/commit/cde17cc0ef51a42d0c9973cc5bd56af01ec639c4))
- Make jupyter types_or conditional and allow multi-doc YAML in pre-commit ([43b1312](https://github.com/DragonBishop/python-copier-template-ds/commit/43b13127bafad4e2606c66a794f2829e4137d065))

## [1.3.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.2.1...v1.3.0) - 2026-08-24

### 🚀 Features

- Restore pre-commit and rumdl from upstream ([bfc9829](https://github.com/DragonBishop/python-copier-template-ds/commit/bfc982985275a26a28e06a7b6f6b7a84118a348b))

## [1.2.1](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.2.0...v1.2.1) - 2026-08-24

### 📚 Documentation

- Comment the copier-answers gitignore entry ([f54579d](https://github.com/DragonBishop/python-copier-template-ds/commit/f54579d2f6537c0c0cff32d8f6720d489b1595a3))

## [1.2.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.0.3...v1.2.0) - 2026-08-24

### 🚀 Features

- Make notebooks/ and reports/ optional, treat as one-time scaffolding ([25d61b4](https://github.com/DragonBishop/python-copier-template-ds/commit/25d61b4153396e97c9de65b81a83dea11a00d488))
- Treat src/ as one-time scaffolding too ([efaee23](https://github.com/DragonBishop/python-copier-template-ds/commit/efaee234c1d6f81256948198ccba46a1f470bdd7))
- Restore lint CI job and ruff dependency group from upstream ([158ecf2](https://github.com/DragonBishop/python-copier-template-ds/commit/158ecf23fec217111f8d83ea13b9aa2c35a840a7))

## [1.0.3](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.0.2...v1.0.3) - 2026-08-05

### 🐛 Bug Fixes

- Correct conditional syntax in install command and improve git initialization check ([97e3be9](https://github.com/DragonBishop/python-copier-template-ds/commit/97e3be97dfec813baaeb4f87497b8c24f6b9c778))

## [1.0.2](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.0.1...v1.0.2) - 2026-08-05

### 🐛 Bug Fixes

- Declare hatchling wheel packages explicitly ([adfce48](https://github.com/DragonBishop/python-copier-template-ds/commit/adfce482aef92bbbde3056e12c621f01f29df95c))

## [1.0.1](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.0.0...v1.0.1) - 2026-08-02

### 🐛 Bug Fixes

- Corrections to issue forms missed in v1.0.0 ([a0e7b0e](https://github.com/DragonBishop/python-copier-template-ds/commit/a0e7b0ec8bed0a4dab295d6c3c4826910cd8da5b))

## [1.0.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v0.1.1...v1.0.0) - 2026-08-02

### 🚀 Features

- [**breaking**] Replace markdown issue templates with issue forms ([554d2c9](https://github.com/DragonBishop/python-copier-template-ds/commit/554d2c954dbb8b10a17b9d28c6fa990d0bd10b51))

## [0.1.1](https://github.com/DragonBishop/python-copier-template-ds/compare/v0.1.3...v0.1.1) - 2026-08-01

### 🚀 Features

- Add project type and module inclusion options to copier template; implement CI workflow and update README structure ([8c9c3fd](https://github.com/DragonBishop/python-copier-template-ds/commit/8c9c3fd26a72d6b080477eb8379d5d96fd46e994))

### ⚙️ Miscellaneous Tasks

- Add GitHub issue templates for bug reports, documentation updates, feature proposals, and technical debt resolution ([c4f993b](https://github.com/DragonBishop/python-copier-template-ds/commit/c4f993b8569ec899b99d41dc1c731251f374d976))
- Moved issue templates for bug reports, documentation updates, feature proposals, and technical debt resolution ([80004a7](https://github.com/DragonBishop/python-copier-template-ds/commit/80004a7071bb3c7d7784bfdf1e00004fca85a15b))
- Update issue templates for consistency and clarity ([48e1fc4](https://github.com/DragonBishop/python-copier-template-ds/commit/48e1fc4cb89f83f8f820641500f6ba09f702aded))
- Update README and issue templates for consistency and clarity ([3bfde9c](https://github.com/DragonBishop/python-copier-template-ds/commit/3bfde9c8be172d4bebbf5fc0add675977dd973f8))

### Refactor

- Remove pre-commit/Ruff, update README and template structure ([0e9973f](https://github.com/DragonBishop/python-copier-template-ds/commit/0e9973f521c93d046e81b341bdbd42bac9cd5ad9))

## [0.1.2](https://github.com/DragonBishop/python-copier-template-ds/releases/tag/v0.1.2) - 2026-03-17

