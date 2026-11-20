# ESPFlight — Homepage Deep Visual, UX and Content Review
**Date:** 2026-11-20
**Cycle:** website-zero-start-20261120
**Page:** 001, English / and Persian /fa/
**Baseline:** public_html_11202026.zip, SHA256 e84eb0e1e0a9a71bb7504451b43de479283f5551fc9b43c24f0e3de7c2e747b1
**Status:** in_progress — owner-requested final visual/content review pending; no production verification.

## Actual source changes
Exactly three files changed (the complete deploy and rollback packages were delivered in the chat):
- `index.html`: clearer hero/meta/OG/Twitter copy; more accurate three-part platform heading and engineering-section description; four functional hero quick links; replace potentially misleading "Battery status" with "Supply-voltage data"; cache-busting stylesheet query.
- `fa/index.html`: matched natural Persian copy, four Persian-language links, accurate "داده‌های ولتاژ تغذیه", stylesheet query. **Owner-approved Persian hero AND footer slogan «یاد بگیر. بساز. پرواز کن.» preserved exactly.**
- `assets/home-ux-v30-20261018.css`: homepage-only flat interactive tile styling, hover and visible keyboard focus, 44px minimum mobile targets, reduced-motion support, dark/light and RTL parity. No box shadows.

Four hero links now target the corresponding language's Firmware, Hardware, App and Docs Build Overview pages.

## Fresh local verification
- **76/76 targeted checks passed**, including 20 static content/HTML checks, 32 responsive-browser scenarios (2 languages x 2 themes x 8 widths 320–1440px), and 24 keyboard focus/theme/menu/language selector checks.
- Browser tests confirmed image loads, no horizontal overflow, no clipped primary headings, 44px clickable touch targets, no JavaScript exceptions, and no unexpected box shadows in checked cards.
- `api/esp/tests/site_integrity.py`: PASS, 164 pages, 162 sitemap URLs, 22,392 local references and 1,482 fragment links.
- `api/esp/tests/release_preflight_v57.py`: PASS, 164 HTML pages, 50 CSS files, 2,974 local asset references.
- CSS parser: 0 errors.
- Deployment and rollback ZIP: manifest, CRC, SHA-256, relative paths and mode 0644 verified.
- Browser testing inlined original website resources because Chromium blocked local HTTP; NOT equivalent to live production verification.

## Modified file SHA-256
- `index.html`: f63553129b771292f2ab2bebbf74f0efb5a950135b5ae3ea1f45fc382e484875
- `fa/index.html`: e182783324b14b9e26b7a910969075132be1e9ecae87d9519b55f147cc38cac8
- `assets/home-ux-v30-20261018.css`: 75a4fe9cbbfebc0fbacc5e9cd967737e33d29fc7a6db30999e65d1df9cca4e3b

## Explicit limitations / owner review gate
User must review the improved visual/copy result before marking the Homepage ready_for_deploy. Live host, response headers, TLS/CDN/cache, mobile physical devices, full WCAG assistive-tech checks, Lighthouse/Core Web Vitals, Safari/Firefox and API integration were NOT tested.

Deploy ZIP: `ESPFlight_Home_Visual_Content_Final_20261120_DEPLOY.zip` (3 changed files, relative to existing public_html).
Rollback ZIP: `ESPFlight_Home_Visual_Content_Final_20261120_ROLLBACK.zip` (3 original files from uploaded ZIP, NOT necessarily current live-host baseline).
Before deployment, back up live files and compare versions, then extract ZIP inside the existing `public_html` and verify both pages on the actual host. Do NOT automatically deploy or overwrite newer host files.

## Next action
Finish owner-requested final visual/copy acceptance on **Homepage**. Only after that, continue page 002 **Platform** EN/FA. Preserve all API/admin/app/firmware/flight logic.
