# Architecture

## Core versus modules

`szcore` owns framework state and common services. Feature gameplay stays in independent `szcore_*` resources so it can be upgraded, restarted or omitted without making the core monolithic.

## Player registry

The core keeps indexed registries for source, citizen ID, license, job, duty job, gang and group lookups. Hot-path lookups should use those indexes rather than scanning every player.

## Player lifecycle

A character moves through account/character selection, login, loaded runtime state, dirty-state changes, save and logout. Other resources should react to the SzCore lifecycle instead of creating their own duplicate player truth.

## Persistence

Player data uses dirty/version-aware saving. Inventory uses dirty-slot persistence. Vehicle location writes are movement-gated. DB writes should be batched where atomicity and correctness allow it.

## Server authority

Money, inventory, persistent vehicles, permissions and critical gameplay state are mutated on the server. Client UI is presentation/input, not authority.

## Services

The core provides callbacks, hooks, commands, secure events, groups/permissions, account/ledger services, storage, migrations, routing buckets, audit and metrics.

## State bags

Only replication-friendly flat/compact state should be placed in state bags. Large server objects and private state remain server-side.

## Compatibility

ESX/QB/Qbox adapters translate common APIs to native SzCore calls. They are separate resources so compatibility code does not contaminate the native core.
