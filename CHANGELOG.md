## [2.2.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v2.1.0...v2.2.0) - 2026-10-23

### 🚀 Features

- Link commit hashes and versions in git-cliff changelogs ([02a1458](https://github.com/DragonBishop/python-copier-template-ds/commit/02a1458d80f70725ca2fb8ce96a644efd4c67223))

### 🐛 Bug Fixes

- *(deps)* Update template dependencies ([1cf7618](https://github.com/DragonBishop/python-copier-template-ds/commit/1cf76181de9b60da4e50bbdc86c3155908609e2a))
- *(deps)* Update actions/checkout action to v7 ([725c235](https://github.com/DragonBishop/python-copier-template-ds/commit/725c23541ac778ae57709779321595a929650c3f))
- *(deps)* Update actions/setup-python action to v7 ([8b892ba](https://github.com/DragonBishop/python-copier-template-ds/commit/8b892bae4ffb64c9962770720e63b966b5508ac2))

### 📚 Documentation

- Copy the template from its full git URL ([7430a74](https://github.com/DragonBishop/python-copier-template-ds/commit/7430a74df4fa4b4ace6d02e13c19b9cd9482eb83))

### ⚙️ Miscellaneous Tasks

- Run workflows on main ([8034b0b](https://github.com/DragonBishop/python-copier-template-ds/commit/8034b0b983917f3dfac2d18a79c493ac430c748e))

## [2.1.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v2.0.0...v2.1.0) - 2026-10-19

### 🚀 Features

- *(renovate)* Group minor and patch updates into one PR ([1266fb4](https://github.com/DragonBishop/python-copier-template-ds/commit/1266fb4417cab3b08544300ee35a6aaa2979a3e2))

### ⚙️ Miscellaneous Tasks

- Skip tests on release-only PRs ([55a23be](https://github.com/DragonBishop/python-copier-template-ds/commit/55a23be79daab4d328e25b34846e831dee278c33))

## [2.0.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.7.1...v2.0.0) - 2026-10-19

### 🚀 Features

- Add support for testing commit messages in cliff.toml ([3c41ef4](https://github.com/DragonBishop/python-copier-template-ds/commit/3c41ef4b4f3f3f38d00a564344e02898737746bf))
- Add renovate configuration for dependency management ([4d3357a](https://github.com/DragonBishop/python-copier-template-ds/commit/4d3357a333dacaadd916cd52c58c90d5e852b552))
- Add Renovate config as a tooling option ([02d6dda](https://github.com/DragonBishop/python-copier-template-ds/commit/02d6dda1d583a0a158e561fca73e6b165c28934a))
- [**breaking**] Replace project questions with structure and tooling multi-selects ([24f61bd](https://github.com/DragonBishop/python-copier-template-ds/commit/24f61bdb0953a13c1877e3390b93b92f76134b3b))
- Add Semgrep tooling option ([acffd48](https://github.com/DragonBishop/python-copier-template-ds/commit/acffd4879021dacb3dc56bb2ca39b94cccfe90de))
- Add 7-day dependency cooldown ([95e25fc](https://github.com/DragonBishop/python-copier-template-ds/commit/95e25fce512d3a20177315c97038b584b239eb7e))
- Lint PR commits instead of PR titles ([fd4af7c](https://github.com/DragonBishop/python-copier-template-ds/commit/fd4af7c54fde5cdde229ea887420dc725f10a60c))

### 🐛 Bug Fixes

- Add README.md to _skip_if_exists in copier.yml ([dfbe11f](https://github.com/DragonBishop/python-copier-template-ds/commit/dfbe11fa5d545c866868a7833fa7419c78fffe34))
- Write GitHub release notes with git-cliff ([e5dc2af](https://github.com/DragonBishop/python-copier-template-ds/commit/e5dc2af7e9f0c643935cf17b283630044c0ac73d))

### 📚 Documentation

- Consolidate commit and PR requirements into one section ([94a2ea9](https://github.com/DragonBishop/python-copier-template-ds/commit/94a2ea9210349c9524ecc9db52e70157a367730c))

### ♻️ Refactor

- [**breaking**] Always generate the module under src/ ([7b34c6d](https://github.com/DragonBishop/python-copier-template-ds/commit/7b34c6df3ab8622d110cfa936b878c246b057f5d))
- [**breaking**] Merge the README variants and gate notebooks/reports on structure ([73493ed](https://github.com/DragonBishop/python-copier-template-ds/commit/73493edfb1320ec55502fb32d46661f052a0e0ca))
- [**breaking**] Gate workflows and release files on tooling choices ([b97e968](https://github.com/DragonBishop/python-copier-template-ds/commit/b97e968d343dc3660b71b72a6b6ff5afeba5cd69))

### ⚙️ Miscellaneous Tasks

- Pin GitHub Actions to commit SHAs ([d6da400](https://github.com/DragonBishop/python-copier-template-ds/commit/d6da4007af6284510718d22f5442f3fd581dd276))
- Scan this repo with Semgrep ([ace3e13](https://github.com/DragonBishop/python-copier-template-ds/commit/ace3e1396a6716b6b5ba4327f0b316e8172059c3))

## [1.7.1](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.7.0...v1.7.1) - 2026-09-30

### 🐛 Bug Fixes

- Update justfile to initialize git with main branch and implement minot bug fixes on jinja templates ([a126abb](https://github.com/DragonBishop/python-copier-template-ds/commit/a126abb8747b7c36ca07ac7316e31ffa7b064717))

## [1.7.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.6.0...v1.7.0) - 2026-09-23

### 🚀 Features

- Update release workflow to conditionally regenerate CHANGELOG.md and adjust commit messages ([fdd734e](https://github.com/DragonBishop/python-copier-template-ds/commit/fdd734ebe6d2311be1ad5a9ca6b14995f326e60e))
- Update release workflow to use GitHub App client ID and upgrade token action version ([590d6d8](https://github.com/DragonBishop/python-copier-template-ds/commit/590d6d8c0a56d94e76cbf22dd7c08b879a70ad27))

## [1.6.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.5.0...v1.6.0) - 2026-09-20

### 🚀 Features

- *(release)* Authenticate release-please with GitHub App token ([f99692b](https://github.com/DragonBishop/python-copier-template-ds/commit/f99692b4f18bbdc55e3335b899793ddf785c8ebe))
- Enhance configuration for project setup and release management, edit README for clarity and readability. ([44d40b6](https://github.com/DragonBishop/python-copier-template-ds/commit/44d40b6a97cf171dc74c53ce1fe8bdd5b2c489a0))

### ⚙️ Miscellaneous Tasks

- *(release)* Update version to 1.5.0 in pyproject.toml and uv.lock; adjust release-please config ([fc8d9a9](https://github.com/DragonBishop/python-copier-template-ds/commit/fc8d9a9ced2af522663aa12f86621a0e4ba01fe2))

## [1.5.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.4.0...v1.5.0) - 2026-09-17

### 🚀 Features

- Add PyPI publishing support to the template ([578fb56](https://github.com/DragonBishop/python-copier-template-ds/commit/578fb56d8ae03830f2468cf0f6a93d4dc8ad7570))

### ⚙️ Miscellaneous Tasks

- Use dedicated PAT for release-please instead of repo Actions permission ([039857c](https://github.com/DragonBishop/python-copier-template-ds/commit/039857cb37e4bf55d46e27826f8e354c5dec7e49))
- *(template)* Use dedicated PAT for release-please ([cd823c3](https://github.com/DragonBishop/python-copier-template-ds/commit/cd823c3f85dc4d83349b188ba07fc62e2a3f4a23))

## [1.4.0](https://github.com/DragonBishop/python-copier-template-ds/compare/v1.3.1...v1.4.0) - 2026-08-31

### 🚀 Features

- Add GitHub Actions workflows for linting, testing, and release management ([8227f4c](https://github.com/DragonBishop/python-copier-template-ds/commit/8227f4c607df6d576f77498af6f7c39bae86b28a))
- Update configuration for GitHub Actions and improve markdown linting setup ([4e48ebe](https://github.com/DragonBishop/python-copier-template-ds/commit/4e48ebe708b350cd260192b657d6202192cbcaee))
- Add CI for template repo itself, including release-please, git-cliff, and linting. Updated python dependencies for project and template. ([f88ed2c](https://github.com/DragonBishop/python-copier-template-ds/commit/f88ed2ca475d5abfdce5e0f09876e9fda0d68746))
- Enhance README with detailed template options and project structure descriptions ([a87c93e](https://github.com/DragonBishop/python-copier-template-ds/commit/a87c93eb49f96ff497c81912805b267e6c2dfa0b))
- Add GITHUB_TOKEN to release workflow and update rumdl exclusions ([88b21ba](https://github.com/DragonBishop/python-copier-template-ds/commit/88b21babdfb68b370c8abd9ba40c3608aa07d22a))

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

