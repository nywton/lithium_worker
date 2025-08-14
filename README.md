# Deno Kv Jobs

> A tiny, ergonomic job system for Deno that feels like Rails ActiveJob and runs entirely on **Deno KV** — with **built-in idempotency** to guarantee single execution per key.

* `perform_now` / `perform_later`
* `set({ wait, wait_until, queue })` scheduling
* Named **queues** (userland filtered)
* **Idempotency** (exactly‑once per key) with KV atomics + lock/done markers
* **Retries** with exponential backoff + jitter and `retry_on(Error, rule)`
* Minimal **Worker** based on `kv.listenQueue`
* Small, typed API surface

Works with Deno’s built‑in KV—no extra infra.

