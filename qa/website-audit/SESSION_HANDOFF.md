# ESPFlight — New Audit Handoff

**2026-11-20: User explicitly reset website QA from the first page.** Do not reuse previous Docs audit completion states. This tracker branch supersedes old draft tracker; historical data is archival.

## Source
- User upload: `public_html_11202026.zip`, SHA-256 `e84eb0e1e0a9a71bb7504451b43de479283f5551fc9b43c24f0e3de7c2e747b1`.
- 82 bilingual page pairs, 164 HTML, 50 CSS. Full ordered inventory in `progress.json`.
- The live hosting deployment has **not** been matched to source.

## Just completed
- Homepage EN and FA reviewed.
- Only `fa/index.html` revised: H1 set to official exact slogan `Learn. Build. Fly.`.
- Responsive and functional offline tests passed; see `HOMEPAGE_AUDIT_20261120.md`.
- Deployment and rollback ZIPs delivered separately to the project owner.
- Homepage = `ready_for_deploy`, not live-verified.

## Continue next
- **Page 002 Platform**, `platform/index.html` and `fa/platform/index.html`.
- Inspect and fix both languages, both themes, desktop/mobile, technical content, links, semantics, SEO, accessibility, performance and regressions.
- No modifications to API/admin/mobile app or flight logic without verified need.
- Refresh this entire audit registry and changelog after completion.
