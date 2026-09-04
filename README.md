# app-poc-2

POC: product repository 2 (backend — Kotlin + Ktor).

Hello world Kotlin + Ktor. `GET /` returns `{"message": "Hello World"}`,
`GET /health` returns `{"status": "ok"}`.

## Run locally

This repository does not include the Gradle Wrapper (binary, not versionable
by this file-creation process). With Gradle installed locally:

```bash
gradle run    # starts the server on :8080
gradle test   # runs ApplicationTest
```

To generate the wrapper and avoid depending on a global Gradle:

```bash
gradle wrapper --gradle-version 8.10
git add gradlew gradlew.bat gradle/
```

## Stack

Kotlin 1.9, Ktor 2.3 (Netty), kotlinx.serialization, tested with
Ktor's own `testApplication`. See `.agentic/config.yml` for what the
agentic pipeline knows about this repository.
