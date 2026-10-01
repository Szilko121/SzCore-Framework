# Server API conventions

The native core resource is `szcore`.

Typical integration style:

```lua
local player = exports.szcore:GetPlayer(source)
local byCitizen = exports.szcore:GetPlayerByCitizenId(citizenid)
local players = exports.szcore:GetPlayers()
```

Prefer exported functions for stable cross-resource calls. Use core callbacks when a request/response crosses the client/server boundary. Use hooks for extensibility where the caller should not need to know every consumer.

## Core API areas

- Player lookup and lifecycle
- Money/accounts and transaction ledger
- Jobs, gangs and generic groups
- Metadata
- Permissions and ACE helpers
- Callback creation/invocation
- Hook registration
- Secure network events
- Command registration
- Routing buckets
- Persistent storage
- Schema migrations
- Audit/metrics
- Shared definitions

The exact exported function list is versioned with the `szcore` repository and its `docs/API.md`.
