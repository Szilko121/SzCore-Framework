# Database and persistence

The fresh-install schema is maintained by the `szcore` core and mirrored in `SzCore-Recipe/database/szcore.sql`.

Main tables include:

- `szcore_accounts`
- `szcore_characters`
- `szcore_character_groups`
- `szcore_money_ledger`
- `szcore_financial_accounts`
- `szcore_account_transactions`
- `szcore_storage`
- `szcore_societies`
- `szcore_society_members`
- `szcore_inventories`
- `szcore_inventory_items`
- `szcore_bills`
- `szcore_vehicles`
- `szcore_vehicle_keys`
- `szcore_appearance`
- `szcore_outfits`
- `szcore_queue_priorities`
- `szcore_audit_log`
- `szcore_schema_migrations`
- `szcore_bans`

Use migrations for schema changes. Never edit a live production database manually without a backup and a rollback plan.
