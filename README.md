# Task Tracker

A command-line task tracker (`task-cli`) built with Java and Gradle, based on
the [roadmap.sh Task Tracker project](https://roadmap.sh/projects/task-tracker).

> **Status:** early development. The CLI currently only prints a placeholder
> greeting; task management commands are not implemented yet. See the
> [changelog](CHANGELOG.md) for released versions.

## Requirements

- JDK 25 (the Gradle wrapper is included, no separate Gradle install needed)

## Run

```sh
./gradlew run
```

## Test

```sh
./gradlew test
```

`./gradlew spotlessApply` formats the code.

## Install as `task-cli`

```sh
./gradlew installDist
app/build/install/task-cli/bin/task-cli
```

## Contributing

### Commits

This repo uses [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>[optional scope]: <description>
```

Common types: `feat`, `fix`, `docs`, `build`, `chore`, `refactor`, `test`.
Mark breaking changes with `!` after the type (e.g. `feat!: ...`) or a
`BREAKING CHANGE:` footer.

### Versioning

This repo follows [Semantic Versioning](https://semver.org/) (`MAJOR.MINOR.PATCH`).
The current version is set in `gradle.properties`.

- `fix` → PATCH
- `feat` → MINOR
- breaking change → MAJOR (while below 1.0.0, breaking changes may bump MINOR)

User-facing changes are recorded in [CHANGELOG.md](CHANGELOG.md)
([Keep a Changelog](https://keepachangelog.com/) format) under `Unreleased`
until a release is cut.

## License

Released under the [MIT License](LICENSE).
