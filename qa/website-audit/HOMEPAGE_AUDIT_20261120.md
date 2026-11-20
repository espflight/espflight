# ESPFlight — Homepage Audit & Correction

**Review date:** 20 November 2026. Source: user-uploaded `public_html_11202026.zip`.

## User-approved slogans (preserve both)

| Language | Exact homepage slogan | Markup |
| --- | --- | --- |
| English | **Learn. Build. Fly.** | `lang="en" dir="ltr"` |
| Persian | **یاد بگیر. بساز. پرواز کن.** | `lang="fa" dir="rtl"` |

The previous audit incorrectly treated the approved Persian translation as a defect. **That finding has been withdrawn and its source modification was reverted byte-for-byte.** Do not overwrite the Persian H1 with English in future work.

## Source state and scope

- `index.html` (English): unchanged from uploaded source.
- `fa/index.html` (Persian): restored, byte-for-byte identical to uploaded source.
- Persian original source SHA-256: `2a0d7b57efab5de90eab059f1b99f6ba4cf20b8f8060653392cefcd4b859aa4f`.
- **Current Homepage HTML differences relative to uploaded source: zero**. No PHP, API, admin, app, firmware, JS, CSS or flight logic changes.
- Previous "deploy" ZIP that contained the English hero in Persian page is obsolete and must not be installed. New correction/restore ZIP contains original Persian homepage.

## Tests

- **PASS** `python api/esp/tests/site_integrity.py`: 164 pages, 162 sitemap URLs, 22,384 local references, 1,482 fragments after restoration.
- **PASS** `python api/esp/tests/release_preflight_v57.py`: 164 HTML files, 50 CSS, 2,974 local asset references after restoration.
- Verified actual English and Persian H1 strings and their lang/dir attributes against uploaded baseline.
- Historical offline Chromium responsive checks: 32 combinations, prior audit; visual browser testing **not rerun after the restoration**.
- Historical four selected interactions/media checks: prior audit; **not rerun**.
- Live host, cache, HTTP headers, Lighthouse, independent browsers and production deployment: **not tested**.

## Release decision

- If host already has the original Persian hero, **do not deploy any Homepage patch**.
- If the earlier incorrect patch was installed, back up live `fa/index.html`, compare current state and restore the original file from `ESPFlight_Home_20261120_PERSIAN_SLOGAN_RESTORE.zip` only if appropriate. Then test live.
- Homepage is recorded as locally reviewed with no required source changes, **not** live verified.

## Next

Page 002 **Platform**, English and Persian, follows in the new 82-page sequential audit.
