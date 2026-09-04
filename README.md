# app-poc-2

POC: repositório de produto (backend) — laboratório da pipe agêntica.

Hello world Kotlin + Ktor. `GET /` responde `{"message": "Hello World"}`,
`GET /health` responde `{"status": "ok"}`.

## Rodar localmente

Este repositório não inclui o Gradle Wrapper (binário, não versionável
por este processo de criação de arquivos). Com Gradle instalado
localmente:

```bash
gradle run    # sobe o servidor em :8080
gradle test   # roda ApplicationTest
```

Para gerar o wrapper e não depender de Gradle global:

```bash
gradle wrapper --gradle-version 8.10
git add gradlew gradlew.bat gradle/
```

## Stack

Kotlin 1.9, Ktor 2.3 (Netty), kotlinx.serialization, testado com
`testApplication` do próprio Ktor. Ver `.agentic/config.yml` para o
que a pipe agêntica sabe sobre este repositório.
