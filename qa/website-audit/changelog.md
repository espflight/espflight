# ESPFlight Website — New Audit Cycle

## 2026-11-20 — Restart from Homepage
- Reset all 82 paired routes to `pending`, except Page 001 Homepage.
- Enumerated source based on main menu and Docs sidebar with remaining real filesystem routes.
- Reviewed Home EN/FA; fixed official slogan mismatch in Persian H1, exactly one HTML file.
- Re-ran local integrity/preflight and Chromium offline responsive + selected interactions.
- Homepage marked `ready_for_deploy` (not deployed); Platform next.

## 2026-11-20 — Owner correction: preserve localized Persian slogan
- Incorrect English-only replacement of Persian homepage H1 has been reverted byte-for-byte.
- Preserve `یاد بگیر. بساز. پرواز کن.` in Persian hero, `Learn. Build. Fly.` in English hero.
- Withdrawn HOME-001 as a false-positive issue; no current homepage source changes.
- Re-ran site integrity and release preflight after restoration: both PASS.
- Earlier English-only deploy ZIP is obsolete. New restore package provided if wrong patch was previously installed.
- Page 002 Platform remains next; page 001 not live-verified.
