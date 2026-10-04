---
name: mongodb-create-database-user
description: Create a new database user in a project and retrieve its details.
api: openapi/mongodb-database-users-api-openapi.yml
operations:
- createGroupDatabaseUser
- getGroupDatabaseUser
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/mongodb-database-users-api-openapi.yml ; every operationId checked against the contract
---

# mongodb-create-database-user

Create a new database user in a project and retrieve its details.

## Steps

1. 1. Call `createGroupDatabaseUser` with required body fields `databaseName`, `username`, and `password`.
2. 2. Call `getGroupDatabaseUser` with path parameters `databaseName` and `username` to fetch the created user.

## Rules

- Auth: Include a DigestAuth header or a ServiceAccounts OAuth2 token in the request.
- Idempotency: The `createGroupDatabaseUser` operation is not idempotent; repeat calls will create duplicate users.
- Rate limit: 1200 requests per group with a refill of 500 requests per 60 seconds.
