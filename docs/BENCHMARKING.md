# Benchmarking

`szcore_benchmark` is a portable benchmark resource intended to run on SzCore, ESX or Qbox test servers.

It separates:

1. **LIVE API** — actual running framework APIs
2. **ARCHITECTURE MODEL** — controlled synthetic player/index models
3. **COMMON SYNTHETIC** — framework-neutral CPU/data-structure workload
4. **DB measurements** — controlled read/write latency where configured

Use multiple rounds and compare median/p95, ops/s and memory. Run every framework on the same machine, artifact, DB and configuration.

Do not infer a production winner from idle resmon alone. Network/statebag/entity/OneSync performance requires real clients or an appropriate load environment.
