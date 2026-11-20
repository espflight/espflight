# ESPFlight — Fresh Homepage Audit (20 November 2026)

## Scope
- Source: uploaded `public_html_11202026.zip` (SHA-256 `e84eb0e1e0a9a71bb7504451b43de479283f5551fc9b43c24f0e3de7c2e747b1`).
- Source inventory: 164 HTML (82 EN / 82 FA) and 50 CSS files.
- Examined: `index.html` and `fa/index.html`; source integrity and static preflight re-run globally.

## Correction made
The Persian homepage hero H1 contained a translation of the official brand slogan. Only `fa/index.html` changed: H1 now says **Learn. Build. Fly.**, with `lang=en`, `dir=ltr`. English homepage and remaining Persian copy remain unchanged.

Source SHA-256 of the changed file:
- Before: `2a0d7b57efab5de90eab059f1b99f6ba4cf20b8f8060653392cefcd4b859aa4f`.
- After: `42ca2a8de0e29bf1f143963192513162365adbf154b4d9b768546949ca833dd0`.

## Completed checks
- PASS `python api/esp/tests/site_integrity.py`: 164 pages, 162 sitemap URLs, 22,384 local refs, 1,482 fragments.
- PASS `python api/esp/tests/release_preflight_v57.py`: 164 pages, 50 CSS, 2,974 local asset refs.
- PASS 32 inlined-asset Chromium responsive/layout checks: EN/FA x light/dark x widths 320, 360, 390, 430, 600, 768, 1024, 1440 px. No horizontal overflow, clipped headings, unintended panel shadows or page JS errors.
- PASS four selected interaction/media smoke cases: EN/FA x 390/1440 px, all 3 images loaded after viewport scroll; theme toggle; mobile menu with Escape or desktop language selector; no page JS exceptions.
- Reviewed homepage semantics, headings, canonical and hreflang metadata, JSON-LD syntax, alt text/image dimensions, internal linking, brand identity and key safety-related copy.

## Important limitations
Headless Chromium was tested using page.set_content with **actual local CSS, JS, fonts and images inlined** because browser navigation to localhost/file URLs is restricted in this environment. This is not a production HTTP test. Not performed: production deployment, live response headers/SSL/cache, full WCAG assistive-technology audit, full Lighthouse metrics, independent Safari/Firefox matrix, API/host security testing.

## Install
Deploy archive: `ESPFlight_Home_20261120_DEPLOY_INSIDE_PUBLIC_HTML.zip` contains only **fa/index.html**. Back up the current live file first; compare to expected baseline hash. Extract directly inside the existing `public_html` (no extra nested folder).

Rollback: `ESPFlight_Home_20261120_ROLLBACK_SOURCE_BASELINE.zip` contains the original **fa/index.html** from the uploaded source; only use on production after verifying the old version matches the actual host baseline, otherwise restore the live backup.

No PHP/API/admin/app/firmware/flight logic, JS or CSS files were modified.

## Outcome
Homepage: `ready_for_deploy` (local) — **not** `deployed_verified`. Next page in new audit sequence: **Platform** (EN/FA).
