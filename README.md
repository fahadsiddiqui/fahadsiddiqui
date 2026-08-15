# Fahad Siddiqui

I build data infrastructure and the systems that sit on top of it — mostly Go and Python, increasingly LLM-shaped.

Founder of [Datum Brain](https://datumbrain.com). We're a small senior team that gets called in when a pipeline is quietly losing data, a schema decision from two years ago is now the bottleneck, or someone needs an AI feature that survives contact with production. ~11 years in, 40+ production systems, mostly fintech, ad tech, health tech, proctoring and real estate.

## Things I've built

- **TrueAudience** (NMS360) — real-time ad fraud detection scoring 10M–100M events/day at sub-100ms. Go and Postgres, plus a lot of unglamorous work on cache concurrency, DST handling and OOM hunting.
- **Polymer** (Predict Data) — turned 100K+ unstructured documents into a queryable Neo4j knowledge graph. ~90% lower per-document processing cost.
- **Centrum AI** — enterprise agent platform: multi-LLM orchestration across Claude, OpenAI and Vertex, 70+ tools, executing generated Go inside sandboxed Docker.
- **PSI RSaaS** — multi-tenant exam scheduling at ~15K req/hour. New client integrations went from ~3 months to ~2 weeks, roughly $50K saved per onboarding.
- **Examity VRS** — WebRTC proctoring video infrastructure; 20–30 concurrent exams per proctor, WASM-powered screen blur.
- **DameTech** — autonomous controller for a 3.2MW Bitcoin mining operation, throttling against real-time electricity prices.
- **Mecku** — visual ETL over Scala/Spark so analysts can compose pipelines without writing Spark.
- **Zolvat** — EMI stack with SEPA transfers, KYC and sanction screening across multiple watchlists.

Write-ups: [datumbrain.com/case-studies](https://datumbrain.com/case-studies) · fuller history at [fsdqui.dev](https://fsdqui.dev)

## Open source

Small tools I needed badly enough to extract and maintain, plus a recent stretch on AI-tooling safety.

| | |
|---|---|
| [otters](https://github.com/datumbrain/otters) | Pandas-style DataFrame library for Go — fluent filter/group/sort, type-safe columns, zero-copy typed slices |
| [claude-code-privacy-guard](https://github.com/datumbrain/claude-code-privacy-guard) | Claude Code plugin that blocks prompts containing API keys, credentials and PII before they leave your machine |
| [niimbot-d110-api](https://github.com/datumbrain/niimbot-d110-api) | Go API for the NIIMBOT D110 label printer |
| [aws-macie-pii-confidential-regexes](https://github.com/datumbrain/aws-macie-pii-confidential-regexes) | PII and confidential-data regex list compiled out of AWS Macie |
| [nulltypes](https://github.com/datumbrain/nulltypes) | GORM null-type JSON marshalling/unmarshalling mixins |
| [keyprobe](https://github.com/datumbrain/keyprobe) | LLM API key validator — detects the provider, hits live endpoints, reports what the key can actually do |
| [gossub](https://github.com/datumbrain/gossub) · [npy](https://github.com/datumbrain/npy) | `spark-submit` from Go; NumPy `.npy` reader/writer in Go |

Lately I've been auditing agentic dev tools for local trust-boundary bugs. On Andrew Ng's [openworker](https://github.com/andrewyng/openworker) I reported an unauthenticated local sidecar API that let any local process drive shell and file tools, a shell-allowlist bypass via command chaining, over-permissive localhost CORS, and an OAuth callback that never validated `state` — then sent the [hardening PR](https://github.com/andrewyng/openworker/pull/49) that fixed them.

Older contributions: [petl](https://github.com/petl-developers/petl) (JSONL support, memory footprint) and [mimetype](https://github.com/gabriel-vasile/mimetype).

## Reach me

- [fahad@datumbrain.com](mailto:fahad+fromgithub@datumbrain.com?subject=Inquiry%20From%20Github) — work
- [fsdqui@gmail.com](mailto:fsdqui@gmail.com?subject=Inquiry%20From%20Github) — personal
- [linkedin.com/in/fsdqui](https://linkedin.com/in/fsdqui)

Happy to talk about Go data tooling, keeping LLM features honest in production, or rescuing a pipeline someone else built.
