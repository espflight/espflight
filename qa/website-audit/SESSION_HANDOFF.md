# ESPFlight — Fresh Website Audit Handoff

**User-requested restart:** 20 November 2026. Baseline is uploaded `public_html_11202026.zip`: 82 English + 82 Persian files.

## CRITICAL — owner correction of slogans
- English homepage hero: **Learn. Build. Fly.** (lang=en, dir=ltr).
- Persian homepage hero: **یاد بگیر. بساز. پرواز کن.** (lang=fa, dir=rtl).
- Do not translate/replace Persian homepage slogan with English. Earlier false-positive “branding fix” was withdrawn and source restored byte-for-byte to upload.
- All Homepage HTML now matches the baseline. No Homepage deployment required unless a mistaken previous ZIP was already installed.

## Progress
- Page 001 Homepage: locally audited, original copy preserved, static tests passed after restoration. NOT verified on production.
- Page 002 **Platform** is next: `platform/index.html` + `fa/platform/index.html`.
- Full ordered inventory and current statuses are in `progress.json`; do not reuse the prior Docs cycle.

## Process
Audit actual source, implement minimal fixes with user-approved localization, test and register evidence. Preserve global Design System and healthy API/admin/app/flight logic. Update progress/issues/changelog/handoff after each page.
