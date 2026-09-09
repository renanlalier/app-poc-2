## Build and Test

```bash
gradle build -x test
gradle test
```

## Code Conventions

- Maintain the REST contract: `GET /` → `{"message":"Hello World"}`, `GET /health` → `{"status":"ok"}`.
- Apply expand/contract for any public contract change; no breaking changes without versioning.
- Open a draft PR targeting `main` with branch `agentic/<execution_id>`. Close the triggering sub-issue with `Closes #<n>` in the PR body.
