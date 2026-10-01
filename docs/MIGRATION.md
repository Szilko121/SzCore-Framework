# Migration

## Fresh install

v1.4.0-rc1 uses the SzCore namespace:
- resources: `szcore`, `szcore_*`
- SQL tables: `szcore_*`
- events: `szcore:` / `szcore_*:`
- ACE: `szcore.*`
- citizen ID prefix: `SZ-`

## From the former Nexus development namespace

Treat v1.4.0-rc1 as a namespace transition, not a drop-in folder rename. Back up the database and migrate table names/data deliberately. Do not run old Nexus and SzCore resources simultaneously against the same data.

## From ESX/Qbox

A migration should separately address:
- identifiers and character IDs
- money/accounts
- jobs/gangs/groups
- inventory/item metadata
- vehicles/properties/garage state
- appearance
- society data

Test on a cloned database before production.
