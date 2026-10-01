# SzCore Framework

**SzCore** is an independent, modular FiveM roleplay framework by **SzCode**.

> Current release candidate: **v1.4.0-rc1**

SzCore has its own player/character lifecycle, indexed player registry, economy, jobs/gangs/groups, permissions, callbacks, hooks, secure events, persistence, inventory, vehicles, UI and gameplay modules. ESX/QB/Qbox support is provided by optional compatibility adapters; those frameworks are not runtime dependencies.

## Install

The recommended installation path is the separate **[SzCore-Recipe](https://github.com/Szilko121/SzCore-Recipe)** repository.

Manual installation is also supported: every native resource lives in its own repository and may be cloned independently into `resources/[szcore]`.

## Native repositories

| Repository | Purpose |
|---|---|
| [szcore](https://github.com/Szilko121/szcore) | Core lifecycle, registry, money/accounts, groups, permissions, callbacks, hooks, secure events, storage, migrations, audit and metrics |
| [szcore_inventory](https://github.com/Szilko121/szcore_inventory) | Slot/weight inventory, metadata, usable items and weapons-as-items |
| [szcore_multichar](https://github.com/Szilko121/szcore_multichar) | Character selection and creation |
| [szcore_spawn](https://github.com/Szilko121/szcore_spawn) | Spawn and saved-position handling |
| [szcore_ui](https://github.com/Szilko121/szcore_ui) | Notify, TextUI and progress UI |
| [szcore_society](https://github.com/Szilko121/szcore_society) | Organization/boss management and society accounts |
| [szcore_banking](https://github.com/Szilko121/szcore_banking) | Banking and transaction history |
| [szcore_billing](https://github.com/Szilko121/szcore_billing) | Player/society invoices |
| [szcore_paycheck](https://github.com/Szilko121/szcore_paycheck) | Duty-aware paychecks |
| [szcore_vehicles](https://github.com/Szilko121/szcore_vehicles) | Owned vehicles and persistent vehicle state |
| [szcore_garage](https://github.com/Szilko121/szcore_garage) | Public/job/gang/shared garages and impound |
| [szcore_vehiclekeys](https://github.com/Szilko121/szcore_vehiclekeys) | Keys, locks, engine, hotwire, lockpick and carjack |
| [szcore_vehiclefailure](https://github.com/Szilko121/szcore_vehiclefailure) | Vehicle damage/failure and tyre bursts |
| [szcore_appearance](https://github.com/Szilko121/szcore_appearance) | Character studio and wardrobe |
| [szcore_status](https://github.com/Szilko121/szcore_status) | Hunger, thirst and stress |
| [szcore_death](https://github.com/Szilko121/szcore_death) | Injuries, bleeding, pain, last stand, death and revive |
| [szcore_interact](https://github.com/Szilko121/szcore_interact) | Native third-eye/target interactions |
| [szcore_queue](https://github.com/Szilko121/szcore_queue) | Priority queue, reserved slots and bans |
| [szcore_world](https://github.com/Szilko121/szcore_world) | Ped/traffic density, calm AI, wanted/dispatch control |
| [szcore_smallresources](https://github.com/Szilko121/szcore_smallresources) | Crouch, cruise, recoil, tackle, vehicle push/flip and other QoL |
| [szcore_admin](https://github.com/Szilko121/szcore_admin) | Admin panel and moderation tools |
| [szcore_benchmark](https://github.com/Szilko121/szcore_benchmark) | Portable SzCore/ESX/Qbox benchmark suite |

### Optional compatibility repositories

- [szcore_compat_esx](https://github.com/Szilko121/szcore_compat_esx)
- [szcore_compat_qb](https://github.com/Szilko121/szcore_compat_qb)
- [szcore_compat_qbox](https://github.com/Szilko121/szcore_compat_qbox)

## Documentation

- [Getting started](docs/GETTING_STARTED.md)
- [Installation and startup order](docs/INSTALLATION.md)
- [Architecture](docs/ARCHITECTURE.md)
- [Resource reference](docs/RESOURCES.md)
- [Server API conventions](docs/SERVER_API.md)
- [Events, callbacks and hooks](docs/EVENTS.md)
- [Security and permissions](docs/SECURITY.md)
- [Database and persistence](docs/DATABASE.md)
- [Compatibility](docs/COMPATIBILITY.md)
- [Benchmarking](docs/BENCHMARKING.md)
- [Migration](docs/MIGRATION.md)
- [Troubleshooting](docs/TROUBLESHOOTING.md)
- [Development guide](docs/DEVELOPMENT.md)

## Design principles

SzCore is built around indexed hot-path lookups, event-driven state changes, server-authoritative mutations, dirty/batch persistence, explicit modular boundaries and measurable performance.

No fixed resmon or “faster than ESX/Qbox” guarantee is made without an identical real-world benchmark. Use `szcore_benchmark`, the FXServer profiler and repeatable load tests for performance decisions.
