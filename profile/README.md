<div align="center">

<img src="https://raw.githubusercontent.com/uptimepage/.github/main/profile/og.png" width="720" alt="Uptimepage: status pages and uptime monitoring">

[**Start free**](https://app.uptimepage.dev/login?redirect_after=%2F) · [Docs](https://uptimepage.dev/docs) · [Source](https://github.com/uptimepage/uptimepage)

</div>

---

Uptimepage is a hosted uptime-monitoring and public status-page service for teams. Monitor websites and APIs from multiple regions, alert the people on call, and publish incidents for customers from the same product.

Start on the hosted service at [uptimepage.dev](https://uptimepage.dev). The same production code is public under AGPL, so your team can inspect it or self-host when you need full control.

## Why Uptimepage

- **A login for each teammate, not a shared password.** Owner and member roles, with GitHub or email invites.
- **API-first.** Every monitor, status page, and incident is a REST resource you can manage by hand or with Terraform.
- **MCP server.** Point an AI assistant at `mcp.uptimepage.dev` to check status, review incidents, and manage monitors over OAuth.
- **Checks from multiple regions**, so one bad vantage point does not page the whole team.
- **Real status pages** with incident timelines, scheduled maintenance, and email or webhook subscriptions.
- **Alerts where your team already works**, with confirmation thresholds and a recovery notice when the incident clears.

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
| `flow` | replay a scripted browser login, alert when a step fails |

## Alerts

Slack, Discord, Microsoft Teams, Telegram, PagerDuty, Pushover, ntfy, email, SMS, and generic webhooks. Route different monitors to different channels, require several failed checks before paging, and re-notify while an incident stays open.

## Repositories

| Repo | What it is |
|---|---|
| [**uptimepage**](https://github.com/uptimepage/uptimepage) | The service: async Rust (Tokio, Axum), Postgres for config, ClickHouse for high-cardinality results. REST API, public status pages, Prometheus metrics. |
| [**terraform-provider-uptimepage**](https://github.com/uptimepage/terraform-provider-uptimepage) | Manage monitors and notification channels as code over the `/api/v1` REST API. |

## Getting started

The fastest path is the hosted service: [start free](https://app.uptimepage.dev/login?redirect_after=%2F), add a target, and flip on the public status page. Self-hosting and the full API are covered in the [docs](https://uptimepage.dev/docs).

<div align="center">
<sub>Hosted service · start free · no card</sub>
</div>
