<div align="center">

<img src="https://raw.githubusercontent.com/uptimepage/.github/main/profile/org-icon.png" width="96" alt="UptimePage">

# UptimePage

**Status pages and uptime monitoring.** Hosted, free, open source.

[**uptimepage.dev**](https://uptimepage.dev) · [Docs](https://uptimepage.github.io/uptimepage/) · [Sign in with GitHub](https://uptimepage.dev)

</div>

---

One `POST`, public in 30 seconds. Run HTTP, TCP, DNS, TLS-certificate-expiry, and domain-expiry checks against your targets — then turn them into a customer-facing status page with incidents and scheduled maintenance. Alerts go to Slack, generic webhooks, or Telegram.

## Repositories

| Repo | What it is |
|---|---|
| [**uptimepage**](https://github.com/uptimepage/uptimepage) | The service — async Rust (Tokio · Axum), Postgres for config, ClickHouse for high-cardinality results. REST API, public status pages, Prometheus metrics. |
| [**terraform-provider-uptimepage**](https://github.com/uptimepage/terraform-provider-uptimepage) | Manage monitors and notification channels as code over the `/api/v1` REST API. |

## Check types

| Type | Purpose |
|---|---|
| `http` | request a URL, match status / body / latency |
| `tcp` | open a TCP socket within a timeout |
| `dns` | resolve a record, optionally match a value |
| `tls_cert` | parse the leaf cert, alert before it expires |
| `domain_expiry` | query RDAP, alert before the domain expires |

## Getting started

The fastest path is the hosted service — sign in at [uptimepage.dev](https://uptimepage.dev) with GitHub, add a target, flip on the public status page. Self-hosting and the full API are covered in the [docs](https://uptimepage.github.io/uptimepage/).

<div align="center">
<sub>Free forever · no card · <a href="https://uptimepage.dev">uptimepage.dev</a></sub>
</div>
