# ESPFlight — Homepage EN/FA Audit (new cycle)

**Cycle:** `website-zero-start-20261120`  
**Page:** 001 Homepage  
**Source:** uploaded `public_html_11202026.zip` (SHA-256 `e84eb0e1e0a9a71bb7504451b43de479283f5551fc9b43c24f0e3de7c2e747b1`)  
**Status:** `ready_for_deploy` locally; **NOT** `deployed_verified`.

## Source and inventory
- Recovered and independently read the complete ZIP; its hash matched the registered reference.
- Rebuilt navigation inventory from actual website main menu, Docs sidebar, footer and HTML routes: **82 bilingual page pairs / 164 HTML files** (82 EN and 82 FA), 50 CSS files.
- English source: `index.html` SHA-256 `b475d138caba9ce014f1b2be3509df5a3f2002e1f1f4669057ebf373a9920344`.
- Persian source: `fa/index.html` SHA-256 `2a0d7b57efab5de90eab059f1b99f6ba4cf20b8f8060653392cefcd4b859aa4f`.
- **No website source changes** were necessary. Both files remain byte-for-byte identical to original uploaded archive.

## Localized branding
- EN H1 exactly **Learn. Build. Fly.** (`lang=en`, `dir=ltr`).
- FA H1 exactly **یاد بگیر. بساز. پرواز کن.** (`lang=fa`, `dir=rtl`).
- Both approved slogans are preserved, without replacing the Persian translation.
- Homepage license summaries match `espflight/espflight/LICENSING_OVERVIEW.md`: firmware MIT, hardware CERN-OHL-P-2.0, docs CC BY 4.0, app proprietary. Maker/brand language matches `BRAND_POLICY.md`.
- Firmware pseudo-code is explicitly marked illustrative.

## Fresh test evidence (2026-11-20)
| Scope | Actual result |
| --- | --- |
| Homepage source static checks | **34/34 PASS** — lang/dir, headings, slogans, canonical/hreflang, JSON-LD syntax, alt/size, duplicate IDs, internal homepage links, approved footer copy, source hashes |
| Browser layout & images | **32/32 PASS** — EN/FA x light/dark x widths 320, 360, 390, 430, 600, 768, 1024, 1440 px |
| Selected interactions/errors | **24/24 PASS** — theme toggle, mobile menu with Escape, desktop language selector, no page JS errors at 390/1440 px |
| Site integrity | **PASS** — 164 HTML pages, 162 sitemap URLs, 22,384 local references, 1,482 fragments |
| Release preflight | **PASS** — 164 HTML, 50 CSS, 2,974 local asset references |

The first browser test run timed out after 26 successful viewport cases; the remaining six cases were executed separately and passed. It would be inaccurate to claim that the interrupted process itself completed.

**Browser limitation:** The current testing environment rendered actual site styles, scripts, fonts and images inlined into headless Chromium documents rather than serving from the production hosting stack. This checks layout/interaction locally but not live server behavior.

## Not tested
- Actual deployment, live server file equality, HTTP/TLS, caching, live PHP/API integration and backend security.
- Independent Safari/Firefox browser matrix, full assistive-technology and WCAG conformance testing, Lighthouse/Core Web Vitals.
- Physical hardware and drone flight.

## Delivery
- Source files modified: **0**.
- Deployment ZIP: **not applicable** (no code changes).
- Rollback ZIP: **not applicable**.
- Separate offline evidence/report ZIP available in the originating chat; this PR stores the persistent report and state.

## Next
**Page 002 Platform**, `platform/index.html` and `fa/platform/index.html`. Resume using this branch's `progress.json` in the next session. Production verification of Homepage remains outstanding; never mark `deployed_verified` without actual host checks.
