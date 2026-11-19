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

## Install as `task-cli`

```sh
./gradlew installDist
app/build/install/task-cli/bin/task-cli
```

## License

Released under the [MIT License](LICENSE).
