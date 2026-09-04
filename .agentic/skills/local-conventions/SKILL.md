---
name: local-conventions-app-poc-2
description: Use this skill when editing routes or tests in this repository (app-poc-2). Complements the platform's generic Kotlin skills with project-specific details.
---

# Repository conventions (app-poc-2)

This skill is local — it exists only in this repo, supplements the platform
skills, and is never visible to other repos.

## This repository
Hello-world Ktor with Netty, kotlinx.serialization for JSON. Routes are
organized as `Route` extension functions in `Application.kt`
(`helloRoutes()`, `healthRoutes()`) — when adding a new route, follow the
same extension-function pattern instead of inflating the `routing { }` block.

## Exposed contract
`GET /` and `GET /health` are consumed by `app-poc-1`. Changing the
response format here is a contract change — discuss the versioning strategy
in the plan before implementing.
