# ESPFlight — Website Quality Audit

**New audit cycle started:** 20 November 2026. The owner requested a full restart, beginning with the Homepage.

## Current progress

| Metric | Count |
|---|---:|
| Bilingual page pairs inventoried | **82** |
| Audited locally and ready for deployment | **1** |
| Verified on the live production host | **0** |
| Pending review | **81** |

**Current:** [Homepage audit](HOMEPAGE_AUDIT_20261120.md) — both languages examined; only Persian H1 updated to the exact official slogan **Learn. Build. Fly.**

**Next in sequence:** Page 002 — Platform (`platform/index.html` and `fa/platform/index.html`).

## Tracking files

- [progress.json](progress.json) — ordered page inventory, statuses and source revisions.
- [issues.json](issues.json) — findings and unresolved deployment checks.
- [changelog.md](changelog.md) — per-session change record.
- [SESSION_HANDOFF.md](SESSION_HANDOFF.md) — instructions to continue in a new chat.
- [HOMEPAGE_AUDIT_20261120.md](HOMEPAGE_AUDIT_20261120.md) — detailed first-page report.

**Baseline:** uploaded `public_html_11202026.zip`, SHA-256 `e84eb0e1e0a9a71bb7504451b43de479283f5551fc9b43c24f0e3de7c2e747b1`.

**Important:** This audit repository branch contains metadata only. It does not deploy the website, alter working API/backend files or prove live-host readiness. Previous draft PR #1 was closed as superseded; this fresh cycle is tracked in draft PR #2.
