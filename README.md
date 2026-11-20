# Task Tracker

[![CI](https://github.com/ahmadshalabi/task-tracker/actions/workflows/ci.yml/badge.svg)](https://github.com/ahmadshalabi/task-tracker/actions/workflows/ci.yml)
[![Release](https://img.shields.io/github/v/release/ahmadshalabi/task-tracker)](https://github.com/ahmadshalabi/task-tracker/releases/latest)
[![License: MIT](https://img.shields.io/github/license/ahmadshalabi/task-tracker)](LICENSE)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-%23FE5196?logo=conventionalcommits&logoColor=white)](https://www.conventionalcommits.org/)
[![SemVer](https://img.shields.io/badge/SemVer-2.0.0-blue)](https://semver.org/)

A command-line task tracker (`task-cli`) built with Java and Gradle, based on
the [roadmap.sh Task Tracker project](https://roadmap.sh/projects/task-tracker).

> **Status:** early development. The CLI currently only prints a placeholder
> greeting; task management commands are not implemented yet. See the
> [changelog](CHANGELOG.md) for released versions.

## Download

1. Download the archive for your platform from the
   [releases page](https://github.com/ahmadshalabi/task-tracker/releases)
   (Linux x64, macOS Apple Silicon or Windows x64). No Java needed.
2. Extract it.
3. Run the launcher:
   - Linux: `task-cli/bin/task-cli`
   - macOS: `task-cli.app/Contents/MacOS/task-cli`
   - Windows: `task-cli\task-cli.exe`

## Build from source

Requires JDK 25 (the Gradle wrapper is included).

```sh
./gradlew run            # run the app
./gradlew test           # run the tests
./gradlew spotlessApply  # format the code
./gradlew installDist    # build app/build/install/task-cli/bin/task-cli
```

## Contributing

Commits follow [Conventional Commits](https://www.conventionalcommits.org/)
(`feat: ...`, `fix: ...`, `feat!: ...` for breaking changes) and versions follow
[Semantic Versioning](https://semver.org/):

- `fix` → PATCH
- `feat` → MINOR
- breaking change → MAJOR (while below 1.0.0, MINOR)

Record user-facing changes in [CHANGELOG.md](CHANGELOG.md) under `Unreleased`.

### Releasing

1. Set `version` in `gradle.properties`.
2. In `CHANGELOG.md`, move `Unreleased` entries under a new
   `## [x.y.z] - date` heading and update the links at the bottom.
3. Commit and merge (e.g. `chore: release x.y.z`).
4. Tag and push: `git tag vx.y.z && git push origin vx.y.z`.

The [Release workflow](.github/workflows/release.yml) then builds the archives
and publishes the GitHub release.

## License

Released under the [MIT License](LICENSE).
