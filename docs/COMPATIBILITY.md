# Compatibility

SzCore is independent from ESX, QB-Core and Qbox.

Optional adapters:

- `szcore_compat_esx`
- `szcore_compat_qb`
- `szcore_compat_qbox`

Their purpose is to translate commonly used legacy exports/events to SzCore services.

Compatibility is intentionally **not claimed as 100% universal**. Third-party scripts may depend on undocumented internals, exact object shapes, external inventory/banking libraries or framework-specific side effects.

For a problematic third-party resource, document the missing API and add a targeted compatibility test before extending the adapter.
