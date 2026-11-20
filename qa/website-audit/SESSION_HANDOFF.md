# ESPFlight website — zero-start session handoff

**Audit cycle:** `website-zero-start-20261120`

**Authoritative audit branch:** `audit/website-zero-start-20261120`

**Tracking directory:** `qa/website-audit/`

## Current state
- Audit initialized; **0 pages completed**; no historic page completion inherited.
- Homepage is the **first pending page**, not locally approved or production verified.
- Source to recover: latest available `public_html` ZIP. Previously uploaded candidate `public_html_11202026.zip` (not guaranteed available in another chat).
- First task: inspect actual current source, build canonical ordered EN/FA page inventory, then audit Homepage in both languages and both themes.

## Critical localization
- English official slogan: **Learn. Build. Fly.**
- Persian approved slogan: **یاد بگیر. بساز. پرواز کن.**
- Preserve Persian copy; do not replace it with the English tagline.

## Future-session rule
Always read `progress.json` first. If the cycle already exists, **resume**; never initialize or clear statuses again merely because the master prompt says “from zero.” Reset only upon new explicit owner instruction and create another isolated cycle.

## Boundaries
Do not alter live website, backend/API/admin, mobile application, firmware, or flight logic without cause, verified source and necessary tests. Save source-change archives and rollback packages separately from GitHub audit metadata.
