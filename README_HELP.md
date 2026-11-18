<!-- SPDX-License-Identifier: AGPL-3.0-only · Copyright (c) 2026 SBS BiM Consulting, Jordi Subirós -->
# guaitaSOL · User guide

Catalan version: [README_AJUDA.md](README_AJUDA.md) · Back to the [README](README.md)

## Contents

1. What it does
2. Sun chart
3. Camera and sensors
4. Horizon profile
5. Direct sun hours
6. Privacy and security
7. Limits
8. Shortcuts
9. About

## 1. What it does

**guaitaSOL 1.0** computes where the Sun is at any place, date and time, and shows it four ways: **sun chart**, **camera** with the paths over the live image, **horizon profile** and **direct sun hours**. It works offline, in a single file.

## 2. Sun chart

The diagram shows the Sun's altitude and azimuth through the day. The green line is the selected day; dots are clock hours. Yellow, blue and grey mark the summer solstice, the winter solstice and the equinox. Drag along the path to change the time.

- **Stereographic**: the usual architectural projection, zenith at the centre and north up.
- **Equidistant**: altitudes are proportional to distance from the centre.
- **Cylindrical**: azimuth horizontal, altitude vertical.

Hour lines can be **solar time** or **clock time** (analemmas, including daylight saving).

## 3. Camera and sensors

Press **Compass** to enable the sensors and **Camera** to see the image. Solar paths are drawn over the real horizon. It needs **HTTPS** (for example GitHub Pages); from a local file the browser will not open the camera.

- **iPhone**: asks for sensor permission; north comes from the iOS compass.
- **Android**: the absolute compass is used when available; otherwise orientation is relative and you must calibrate with the Sun.
- **No sensors**: the orientation simulator lets you try it on a computer.

Phone sensors typically err by 5° to 10°. Use **Calibrate with the Sun** or adjust the heading by hand.

## 4. Horizon profile

The profile is the line of obstacles (buildings, mountains, trees) seen from your spot. It is defined by (azimuth, altitude) points, interpolated between them. You can add them three ways:

- Aim the camera at the obstacle and press **Centre point**.
- Turn on **Mark** and tap the camera image or the horizon chart.
- Type them in, or import a JSON or CSV file (azimuth,altitude).

The profile is stored on the device and shown in every view.

## 5. Direct sun hours

It computes the day's direct sun hours, the total lost to obstacles, the yearly map (day × time) and the monthly average. CSV export covers the whole year. Results are geometric: clouds are not considered.

## 6. Privacy and security

guaitaSOL sends nothing anywhere. A security policy (`connect-src 'none'`) stops the page from connecting to any server. Position, profile and photos live only on the device. The camera stores no image: it only displays it.

If you install it as an app (PWA), the browser only downloads the app's own files (manifest, icons and service worker) from the same site; never your data or anyone else's.

Preferences are kept in the browser's `localStorage`.

## 7. Limits

- The solar calculation (NOAA algorithm) is within 0.05° in altitude and 0.15° in azimuth of high-precision ephemerides.
- Atmospheric refraction uses a standard model; it may vary at very low horizons.
- The compass depends on magnetic declination; set it in the place dialog.
- Near metal objects or magnets the compass drifts.

## 8. Shortcuts

- `←` `→` previous or next day
- `Space` animate the day
- `N` current date and time
- `L` place
- `M` mark points
- `Z` undo point
- `F1` help

## 9. About

**guaitaSOL 1.0** · Guaita Apps suite.

Copyright (C) 2026 SBS BiM Consulting, Jordi Subirós. AGPL-3.0-only licence. IBM Plex fonts (SIL OFL 1.1) embedded.

---
SBS BIM Consulting 2026 · Copyright © 2026 Jordi Subirós · AGPL-3.0-only

Guaita Apps is distributed “as is”, without any warranty. The tools are designed from research and as technical and educational support; verification of the results and the responsibility arising from their use rest solely with the end user.
