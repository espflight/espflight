# ESPFlight — Website QA Handoff

**Cycle:** `website-zero-start-20261120`  
**Authoritative branch:** `audit/website-zero-start-20261120`  
**Current progress:** 82 bilingual page pairs inventoried; 1 locally ready; 81 pending; 0 production-verified.

## Source baseline
- ZIP: `public_html_11202026.zip`.
- SHA-256: `e84eb0e1e0a9a71bb7504451b43de479283f5551fc9b43c24f0e3de7c2e747b1`.
- 164 HTML files (82 EN / 82 FA), 50 CSS files. Verified from extracted source, not inherited from old audit reports.
- This source may not be mounted in a different chat; locate it or recover it before editing. Live host file equivalence remains unverified.

## Page just finished locally
- Page 001 — Homepage EN `index.html`, FA `fa/index.html`.
- Status `ready_for_deploy` locally, not deployed-verified.
- No HTML/CSS/JS changes needed; source files are unchanged from uploaded archive.
- Passed **34/34** source checks, **32/32** responsive browser combinations, **24/24** interaction and JS checks; site-integrity and release-preflight suites PASS.
- Browser tests used inlined local CSS/JS/media, not actual production HTTP.
- Detailed evidence: `qa/website-audit/HOMEPAGE_AUDIT_20261120.md`.

## Approved slogans
- EN **Learn. Build. Fly.**
- FA **یاد بگیر. بساز. پرواز کن.**
Both are intentional. Never replace Persian hero with English.

## Next action
1. Read current `progress.json` and confirm its cycle and source version.
2. Next **Page 002 Platform**: `platform/index.html` and `fa/platform/index.html`, URLs `/platform/` and `/fa/platform/`.
3. Recheck source if a newer ZIP has been uploaded.
4. Audit EN/FA content/design/SEO/accessibility/security dependencies; fix only verified defects.
5. Run regression checks and update the same branch's tracking files. Never reset to zero in subsequent chats.

No API/admin/app/firmware/flight logic or production files were changed in this audit cycle.
