# Events, callbacks and hooks

## Lifecycle events

Native modules react to SzCore lifecycle events for player load/unload and player-data changes. Do not invent a second player-loaded state in feature resources.

## Callbacks

Use the core callback service for request/response workflows. Apply timeouts and never assume an untrusted client response is authoritative.

## Hooks

Hooks allow resources to observe, cancel or modify supported operations without hard-coding feature dependencies into the core.

## Network events

A raw network event is not automatically a public API. Sensitive events should be registered through the secure-event service or validate source, permission, distance, entity ownership and input server-side.

Each resource repository includes a generated `docs/API.md` listing events detected in that release.
