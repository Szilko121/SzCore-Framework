# Installation

## txAdmin

Use the separate repository:

`https://github.com/Szilko121/SzCore-Recipe`

The recipe downloads each SzCore module from its own GitHub repository.

## Manual startup order

```cfg
ensure oxmysql

ensure szcore
ensure szcore_world
ensure szcore_queue
ensure szcore_ui
ensure szcore_interact
ensure szcore_multichar
ensure szcore_spawn
ensure szcore_inventory
ensure szcore_society
ensure szcore_banking
ensure szcore_billing
ensure szcore_vehicles
ensure szcore_vehiclekeys
ensure szcore_garage
ensure szcore_vehiclefailure
ensure szcore_smallresources
ensure szcore_paycheck
ensure szcore_status
ensure szcore_death
ensure szcore_appearance
ensure szcore_admin
ensure szcore_benchmark
```

Compatibility adapters are optional. Start only the adapter required by a third-party legacy resource.

## Updating

Production servers should pin known release tags. Read changelog, migration notes and SQL changes before an update. Back up the database before schema migrations.
