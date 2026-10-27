# Changelog

All notable changes to this DMX/RDM/RZ controller project are recorded in this file.

## [1.1.4] - 2026-10-11

### Added
- RDM discovery keeps up to 128 fixtures. Fixture records live in PSRAM. The discovery task stack and UID scratch buffer remain in internal RAM.

### Changed
- When the web console, USB, or Bluetooth reads fixtures, copy one fixture at a time instead of placing the whole table on the task stack.
- The web fixture list uses a separate PSRAM buffer so up to 128 fixtures can be returned in one response.

### Fixed
- (none)

## [1.1.3] - 2026-10-11

### Added
- Battery level on the web top bar and Overview, matching the on-device rules: percentage, charging bolt, full checkmark, and low-battery warning color.

### Changed
- (none)

### Fixed
- On the Color page, selecting TEST keeps focus and the list on the current row.

## [1.1.2] - 2026-10-11

### Added
- (none)

### Changed
- When the RZ clock is out of range, save 1 MHz instead of rejecting the wire mode or rebuilding the strip.
- Rebuild the strip only when wire mode or pixel count changes.
- Start signal-loss timing only after a successful DMX port send.

### Fixed
- After leaving Color, the strip driver no longer turns off when the output target is still RZ Code or DMX + RZ.
- Strip-only output no longer mis-detects DMX signal loss.

## [1.1.1] - 2026-10-11

### Added
- Unactivated units expose an activation serial port (VID:PID `303A:4002`, name **DMXRZ Activate**). It does not burn eFuse; the port closes after activation.
- One-click activation tool waits for and recognizes the activation serial port.
- Updates require a signed image; unsigned images are rejected.
- While unactivated: RDM, Art-Net, web, and OTA are off; DMX, RZ, Color, language, and backlight remain available.

### Changed
- Larger QR on the unactivated screen; device number is no longer shown alone on the display.
- Web opens directly after joining the LAN IP — no login.
- Touch is disabled after the screen sleeps; a key or encoder wake restores touch. Touching a dark screen does not wake it.
- Factory reset clears Wi-Fi and keeps the authorization certificate.
- Chinese prompts use punctuation already in the font.
- Leaving Color outputs black first.
- Help QR omits the URL when the web console is not authorized.
- On boot, invalid output source, output target, or loss action fall back instead of halting.

### Fixed
- After a mid-scan low-battery exit from RDM, discovered fixtures no longer stay muted.
- On-device Color and web Color no longer clear each other's hold when both are active.
- Unactivated units no longer answer Art-Net Poll.
