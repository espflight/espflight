# ESPFlight — Website Audit (Current Cycle)

**Cycle:** `website-zero-start-20261120` — authoritative branch `audit/website-zero-start-20261120`.

## Honest progress
| Category | Count |
| --- | ---: |
| Verified bilingual page pairs | 82 |
| Page under final review | **1 — Homepage** |
| Ready for deploy | **0** |
| Verified on production | **0** |
| Pending | **81** |

### Page 001 — Homepage
The deeper audit now contains **real source changes**, rather than a no-change technical report. See [Homepage deep review](HOMEPAGE_DEEP_REVIEW_20261120.md).

- 4 hero quick links per language made functional.
- EN/FA copy, metadata and descriptions improved.
- Technical telemetry terminology corrected.
- Styles remain green, flat/shadowless and bilingual.
- Original Persian slogan **یاد بگیر. بساز. پرواز کن.** and English slogan **Learn. Build. Fly.** are preserved.
- Targeted test suite **76/76 PASS**, site-integrity and release preflight PASS.

**Current status: `in_progress` pending owner's final visual/content acceptance.** Local test success is not owner acceptance and not live deployment.

### Tracking
- `progress.json` — page inventory / statuses / modified file hashes.
- `issues.json` — fixes and outstanding owner/production gates.
- `changelog.md` — actual actions and tests.
- `SESSION_HANDOFF.md` — next-chat recovery.
- `HOMEPAGE_DEEP_REVIEW_20261120.md` — current authoritative page-001 report.
- `HOMEPAGE_AUDIT_20261120.md` — superseded baseline note, not an approval.

**Next:** Complete Homepage final review. Only then audit Page 002 Platform.

No API/admin/app/firmware/flight logic was modified through this audit.
