# ESPFlight Website Audit — Handoff (2026-11-20)

This is a provisional continuity checkpoint. It does **not** certify production.

## Evidence recovered
- Latest archived five-page batch: Next Steps; Build Overview; Components; Airframe & Power Selection; Assembly.
- Historical report: ESPFlight_Docs_Next_Five_Pages_20261120_AUDIT_REPORT.md. It records 160/160 responsive/layout and 40/40 interaction checks, performed offline on a prior source baseline; no current re-run.
- Associated deployment archive: ESPFlight_Docs_Next_Five_Pages_20261120_DEPLOY_INSIDE_PUBLIC_HTML.zip (Library metadata only; raw bytes inaccessible here).
- Previous source report: 164 HTML files, 82 EN + 82 FA. Only 81 navigation units provisionally recovered. Never invent the missing item.
- No current full source ZIP could be read; no HTML/CSS/PHP files were modified.
- Cached site views are not proof of current production state.

## Sequence to resume
1. Read progress.json and issues.json in this same directory.
2. Obtain a readable copy of the latest website source and the five-page deploy archive.
3. Compare hashes/versions and verify actual live deployment; earlier five pages cannot be skipped solely based on a prior success message.
4. Resolve the five-page verification gate; next new Docs page is **Wiring & Orientation** at https://espflight.com/docs/build/wiring/.
5. After Wiring & Orientation continue to Motors & Propellers, then Hardware Verification.

## Technical review already started for Wiring & Orientation
Verified official espflight/hardware/PINOUT.md mapping (SHA 06c865f7104d0238160f9faf50ff399a89528108):
M1 D1/GPIO5 front-right; M2 D2/GPIO4 rear-right; M3 D7/GPIO13 rear-left; M4 D8/GPIO15 front-left.
Status LED D4/GPIO2; buzzer RX/GPIO3; SDA D6/GPIO12; SCL D5/GPIO14.
Need warnings for GPIO15 (boot strap), GPIO2 (boot behavior), GPIO3 (UART RX), mandatory MPU6050 at 0x68 and propeller-off validation.

## Unverified
Host deployment, current EN/FA CSS, production headers/redirects, app download availability, complete source diffs, modern browser matrix, physical hardware.

No changes to production, API, admin, mobile app, firmware or flight logic were made by this recovery.
