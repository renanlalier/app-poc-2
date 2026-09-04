---
name: convencoes-locais-app-poc-2
description: Use esta skill ao editar rotas ou testes neste repositorio (app-poc-2). Complementa a skill generica de Kotlin/Ktor da platform com detalhes especificos deste projeto.
---

# Convenções deste repositório (app-poc-2)

Esta skill é local — só existe neste repo, soma-se às skills da platform
(incluindo `kotlin-ktor-boas-praticas`).

## Este repositório
Hello world Ktor com Netty, kotlinx.serialization para JSON. Rotas
organizadas em funções de extensão de `Route` em `Application.kt`
(`helloRoutes()`, `healthRoutes()`) — ao adicionar uma rota nova, siga o
mesmo padrão de função de extensão em vez de inflar o bloco `routing { }`.

## Contrato exposto
`GET /` e `GET /health` são consumidos pelo `app-poc-1` (ver
`config/capability-map.yml` na platform, regra `implies`). Mudança de
formato de resposta aqui é mudança de contrato — use expand/contract.
