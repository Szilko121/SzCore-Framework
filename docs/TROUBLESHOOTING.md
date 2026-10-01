# Troubleshooting

## UI does not open after a full server boot

Check startup order and asynchronous readiness. A resource being marked `started` does not guarantee its database/cache initialization has finished.

## Database errors

Confirm `oxmysql` starts first, the connection string is correct and the schema/migrations completed.

## Third-party ESX/QB/Qbox script fails

Enable only the matching compatibility adapter. Identify the exact export/event/object shape the script expects. Compatibility is broad but not universal.

## Vehicle does not persist correctly

Confirm OneSync is enabled and inspect vehicle state/DB rows before assuming the garage is at fault.

## Performance

Use `szcore_benchmark`, `resmon` and the FXServer profiler. Compare repeatable workloads, not a single idle screenshot.
