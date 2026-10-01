# Security and permissions

## Trust model

The server is authoritative for:
- money and balances
- inventory and item mutation
- persistent vehicle ownership/state
- permissions/groups
- character persistence
- admin actions

## ACE

SzCore uses the `szcore.*` ACE namespace. UI visibility never replaces a server-side permission check.

## Secure events

The core secure-event service supports rate limits, player requirements, permission gates, simple schemas and custom validators.

## World actions

When a client references a player/entity/vehicle, validate proximity and ownership/control server-side when practical.

## Logging

Critical economy/admin/security operations should write structured audit entries. Do not log secrets or authentication credentials.

## Reporting vulnerabilities

Avoid posting exploitable security details publicly before a fix is available. Use the repository owner’s private contact/security channel when configured.
