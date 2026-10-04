---
name: mongodb-create-get-delete-cluster
description: Create a new cluster in a project, retrieve its details, and then delete it.
api: openapi/mongodb-clusters-api-openapi.yml
operations:
- createGroupCluster
- getGroupCluster
- deleteGroupCluster
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/mongodb-clusters-api-openapi.yml ; every operationId checked against the contract
---

# mongodb-create-get-delete-cluster

Create a new cluster in a project, retrieve its details, and then delete it.

## Steps

1. 1. `createGroupCluster` – requires `groupId` path parameter and request body with cluster configuration.
2. 2. `getGroupCluster` – requires `groupId` and `clusterName` path parameters to fetch the created cluster.
3. 3. `deleteGroupCluster` – requires `groupId` and `clusterName` path parameters to remove the cluster.

## Rules

- Auth: include a valid ServiceAccounts OAuth2 token in the `Authorization` header (Bearer).
- Rate limit: GROUP scope, capacity 1200 requests, refill 500 per 60 seconds; on exhaustion no special HTTP response defined.
- Idempotency: `createGroupCluster` is not idempotent; ensure unique `clusterName` or handle conflict responses.
- Errors: API returns standard HTTP error codes (e.g., 4xx for client errors, 5xx for server errors) as defined by MongoDB Atlas.
