# Development guide

1. Native feature resources use the `szcore_` prefix.
2. Keep feature gameplay out of the core when it can be an optional module.
3. Keep persistent mutations server-authoritative.
4. Use indexed registry lookups in hot paths.
5. Prefer events/callbacks/hooks over polling.
6. Batch dirty persistence where correctness permits.
7. Validate player/entity distance and ownership for world interactions.
8. Version public exports deliberately.
9. Document breaking API/schema changes.
10. Run Lua/JS syntax, manifest, dependency, cross-export and regression validation before release.
11. Benchmark on the same environment before claiming a performance improvement.
