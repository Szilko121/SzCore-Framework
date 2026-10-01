# Getting started

## Requirements

- Current FXServer with OneSync enabled
- MariaDB/MySQL compatible database
- `oxmysql`
- txAdmin recommended for first deployment

## Recommended installation

1. Create a clean txAdmin server deployment.
2. Use the remote recipe from `SzCore-Recipe`.
3. Configure the database connection and Cfx license.
4. Review ACE permissions before opening the server.
5. Start the server and confirm the core migration/schema step completes.
6. Create a test character.
7. Test money, inventory, vehicles, garage, society and persistence.
8. Restart the whole server and verify character/vehicle/inventory recovery.
9. Run the benchmark suite and FXServer profiler.
10. Only then move the RC to production.

Every feature resource is optional in principle, but you must also remove/reconfigure resources that depend on it.
