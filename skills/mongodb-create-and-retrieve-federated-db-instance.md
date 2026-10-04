---
name: mongodb-create-and-retrieve-federated-db-instance
description: Create a new Federated Database Instance in a project and then retrieve its details.
api: openapi/mongodb-data-federation-api-openapi.yml
operations:
- createGroupDataFederation
- getGroupDataFederation
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/mongodb-data-federation-api-openapi.yml ; every operationId checked against the contract
---

# mongodb-create-and-retrieve-federated-db-instance

Create a new Federated Database Instance in a project and then retrieve its details.

## Steps

1. 1. Call `createGroupDataFederation` with the required request body fields (`groupId`, `tenantName`, and the federated instance configuration).
2. 2. Call `getGroupDataFederation` with the `groupId` and `tenantName` returned/used in step 1 to fetch the instance details.

## Rules

- Auth: Include a valid DigestAuth or ServiceAccounts OAuth2 token in the request headers.
- Rate limit: GROUP scope – 1200 requests capacity, refills at 500 requests per 60 seconds.
