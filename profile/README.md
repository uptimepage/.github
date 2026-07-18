<div align="center">

<img src="https://raw.githubusercontent.com/uptimepage/.github/main/profile/og.png" width="720" alt="UptimePage: status pages and uptime monitoring">

[**uptimepage.dev**](https://uptimepage.dev) · [Docs](https://uptimepage.github.io/uptimepage/) · [Sign in with GitHub](https://uptimepage.dev)

</div>

---

UptimePage is open-source uptime monitoring with status pages built in. Create a monitor with one API call, then publish a customer-facing status page with incidents and scheduled maintenance in under a minute. Use it hosted at [uptimepage.dev](https://uptimepage.dev) or self-host the whole stack.

## Why UptimePage

- **API-first.** Every monitor, status page, and incident is a REST resource you can manage by hand or with Terraform.
- **MCP server.** Point an AI assistant at `mcp.uptimepage.dev` to check status, review incidents, and manage monitors over OAuth.
- **Checks from multiple regions**, so one bad vantage point does not page the whole team.
- **Real status pages** with incident timelines, scheduled maintenance, and email or webhook subscriptions.
- **Alerts where your team already works**, with confirmation thresholds and a recovery notice when the incident clears.
- **One binary, your choice of host.** The same service powers the hosted product and self-hosting, backed by Postgres and ClickHouse.

## Check types

| Type | Purpose |
|---|---|
| `http` | request a URL, match status, body, or latency |
| `tcp` | open a TCP socket within a timeout |
| `ping` | send an ICMP echo, alert when no reply arrives |
| `dns` | resolve a record, optionally match a value |
| `tls_cert` | parse the leaf certificate, alert before it expires |
| `domain_expiry` | query RDAP, alert before the domain expires |
| `heartbeat` | expect a regular check-in from a job, alert when it goes silent |

## Alerts

Slack, Discord, Microsoft Teams, Telegram, PagerDuty, Pushover, ntfy, email, SMS, and generic webhooks. Route different monitors to different channels, require several failed checks before paging, and re-notify while an incident stays open.

## Repositories

| Repo | What it is |
|---|---|
| [**uptimepage**](https://github.com/uptimepage/uptimepage) | The service: async Rust (Tokio, Axum), Postgres for config, ClickHouse for high-cardinality results. REST API, public status pages, Prometheus metrics. |
| [**terraform-provider-uptimepage**](https://github.com/uptimepage/terraform-provider-uptimepage) | Manage monitors and notification channels as code over the `/api/v1` REST API. |

## Getting started

The fastest path is the hosted service: sign in at [uptimepage.dev](https://uptimepage.dev) with GitHub, add a target, and flip on the public status page. Self-hosting and the full API are covered in the [docs](https://uptimepage.github.io/uptimepage/).

<div align="center">
<sub>Free forever · no card · <a href="https://uptimepage.dev">uptimepage.dev</a></sub>
</div>
