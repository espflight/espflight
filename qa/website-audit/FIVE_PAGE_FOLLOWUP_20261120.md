# ESPFlight — Website audit continuation (2026-11-20)

## Session scope and outcome
Re-opened the supplied master audit prompt and the saved GitHub QA tracker. Inspected **indexed public-page content**, historical audit reports and upstream GitHub technical references. Full current website source is not available in the container; no production HTML/CSS/JS/PHP was changed and **no local browser, responsive or server integration test was executed in this session**. Historical pass counts must not be used as current-session results.

## Historic five-page release gate
| Page | Indexed content observed | Status |
| --- | --- | --- |
| Next Steps | Four pathways; preserve known-good v1 configuration; continue into Build Overview | Historical report + search-index text only; source/deploy not confirmed |
| Build Overview | Six build stages; hardware release + editable design references | Historical report + indexed text only; source/deploy not confirmed |
| Components | Three component groups; WEMOSD1MINI/MPU-6050/U1/BATTERY; avoid unvalidated substitutions | Historical report + indexed text only; source/deploy not confirmed |
| Airframe & Power Selection | Five selection checks; power/motor compatibility cautions | Historical report + indexed text only; source/deploy not confirmed |
| Assembly | Seven assembly stages; propeller-off battery-disconnected checks | Historical report + indexed text only; source/deploy not confirmed |

Web-search indexing is **not** direct live HTTP verification. The source ZIP and deploy ZIP from historical Library results were inaccessible as bytes. No EN/FA pair or theme was rendered/tested here. These five pages remain blocked for source/deployment reconciliation.

## Findings (evidence class explicitly distinguished)

### 1. Conflicting Build sidebar among indexed snapshots — needs live verification
- Indexed Build Overview and Wiring & Orientation list **Airframe & Power Selection** as a separate Build navigation item.
- Indexed Components, Airframe & Power Selection and Assembly snapshots omit that entry from their Build sidebar, even though the pages themselves link to that topic.
- This could be differing snapshots, cache/index staleness or a template inconsistency. **Do not classify as a confirmed live-server defect** until the deployed HTML is read and versions compared.
- Next check: inspect both EN and FA HTML and the shared sidebar generation/template, then verify the entire 7-item Build navigation sequence on all pages.

### 2. Different footer/header branding in indexed Build snapshots — needs current-source verification
- Indexed Build Overview displays “ESP Flight” in the header/footer, whereas other indexed Build pages display “ESPFlight”.
- Official branding is **ESPFlight**; verify actual markup first, then correct only if the source still contains inconsistent visible brand text. Do not treat crawler text normalization as proof of a current live defect.

### 3. Direct application-release download reference — verified upstream mismatch
- Official `espflight/docs/BUILD_V1.0.md` includes a direct GitHub APK URL for Application v1.0.0.
- GitHub official API for `espflight/application/releases/tags/v1.0.0` returned `assets: []` on this date.
- Accordingly, the named GitHub release asset is not attached to that release. Reconcile website text and upstream documentation. Do not claim that *all* independent distribution channels lack an APK.

### 4. Wiring & Orientation — preliminary only, **not started as a deployable edit**
- Search-indexed page lists GPIO mapping but inconsistently omits D1/D2/D7/D8 and D4/RX labels in its motor and peripheral table.
- Official hardware `PINOUT.md` SHA `06c865f7104d0238160f9faf50ff399a89528108` confirms: M1 front-right D1/GPIO5, M2 rear-right D2/GPIO4, M3 rear-left D7/GPIO13, M4 front-left D8/GPIO15; status D4/GPIO2, buzzer RX/GPIO3, SDA D6/GPIO12, SCL D5/GPIO14.
- Official source warns about D8/GPIO15 bootstrap, D4/GPIO2 boot behavior and RX/GPIO3 UART receive behavior; MPU6050 at 0x68 is mandatory. Propose carefully scoped EN/FA improvements once the source is accessible, preserving legacy anchors and testing without propellers.

## Technical baseline checked
- Official `espflight/hardware/PINOUT.md`, SHA `06c865f7104d0238160f9faf50ff399a89528108`.
- Official `espflight/docs/BUILD_V1.0.md`, SHA `de3afcfbcd08ec0b1ee08cc7b80233541c9e3a1f`.
- Official release API for Application `v1.0.0`: no attached assets.

## Test matrix (this session)
| Check | Result |
| --- | --- |
| Historical audit report retrieval | Completed (evidence only) |
| GitHub progress/handoff recovery | Completed |
| Public search-index page text comparison | Completed for five EN pages (not direct live verification) |
| Official GitHub reference inspection | Completed |
| Current production HTTP from website | Not tested — environment cannot connect directly |
| Latest full website source diff | Blocked — archived ZIP byte access unavailable |
| Persian page content/RTL | Not tested |
| Light/dark themes, 320–1440 px | Not tested |
| JS/browser interactions | Not tested |
| Security, response headers, API regression | Not tested |
| ZIP deployment/rollback | Not created — no actual source changes |

## Required next action
1. Obtain/extract authorized current `public_html` bytes plus any already-prepared five-page patch if it exists.
2. Compare hashes against deployed EN/FA files and fix any shared Build sidebar inconsistency found in actual code.
3. Run responsive, interaction, content, localization, accessibility and regression checks on both versions.
4. If five-page batch is verified, continue **Wiring & Orientation** (next new page), then Motors & Propellers and Hardware Verification.
5. Keep the draft audit PR separate from production website code until verified.
