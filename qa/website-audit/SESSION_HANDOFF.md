# ESPFlight — Website QA Handoff

**Cycle:** website-zero-start-20261120
**Authoritative GitHub branch:** audit/website-zero-start-20261120
**Status:** Page 001 Homepage is **in_progress — awaiting owner's final visual/content review**. Do not declare it finished or skip to Platform until acceptance is recorded.

## Actual source baseline and new patch
- Original uploaded source: `public_html_11202026.zip` SHA-256 `e84eb0e1e0a9a71bb7504451b43de479283f5551fc9b43c24f0e3de7c2e747b1`.
- Deploy ZIP in original chat: `ESPFlight_Home_Visual_Content_Final_20261120_DEPLOY.zip`.
- Rollback ZIP in original chat: `ESPFlight_Home_Visual_Content_Final_20261120_ROLLBACK.zip`.
- Source modifications only: `index.html`, `fa/index.html`, `assets/home-ux-v30-20261018.css`.
- These ZIPs may not auto-mount in a new chat. Locate their actual bytes or request access; do not assume they are in the GitHub audit-only repository.

## What changed
1. Four inert homepage feature tiles are now functional accessible quick navigation links (to Firmware, Hardware, App, and Build Guide) with preserved flat design.
2. Homepage introductions and related meta/OG/Twitter descriptions simplified in both languages.
3. 'Three core tools' changed to 'Three connected parts', with equivalent Persian title; build-section repeated description refined.
4. Ambiguous 'Battery status' changed to accurate 'Supply-voltage data / داده‌های ولتاژ تغذیه'.
5. HTML stylesheet query updated to reload changed homepage-specific CSS.

## Tests freshly executed
- 76/76 targeted checks passed: 20 static, 32 responsive (2 languages x 2 themes x 8 widths), 24 focus/theme/menu/language interaction.
- site_integrity PASS; release_preflight_v57 PASS; CSS parser PASS.
- ZIP manifest/CRC/permission and file hashes verified.
- Chromium browser tests inlined the real site resources due to local HTTP being blocked; this does not validate actual production HTTP, CDN or real host.

## CRITICAL APPROVED COPY
- EN H1/footer **Learn. Build. Fly.**
- FA H1/footer **یاد بگیر. بساز. پرواز کن.**
Both preserved exactly. Do not replace Persian slogan.

## Next action
1. Read the updated `progress.json` and `HOMEPAGE_DEEP_REVIEW_20261120.md`.
2. Finish owner-requested visual/content acceptance for Homepage. Keep `in_progress` until acceptance.
3. After acceptance: set `ready_for_deploy`, with owner-approved package; only `deployed_verified` after actual live tests.
4. Then continue Page 002 Platform EN/FA.
5. Never reset the cycle in subsequent chats. Never modify API/admin/app/firmware or flight logic without a verified necessity.
