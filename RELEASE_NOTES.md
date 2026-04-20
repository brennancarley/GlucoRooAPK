<!--
  GlucoRoo — Hammerhead Karoo Extension
  Copyright (c) 2026 Brenchris, Inc. All rights reserved.

  This source code is proprietary and confidential. Unauthorized copying,
  modification, distribution, or use of this file, via any medium, is
  strictly prohibited. See the LICENSE file in the project root for full
  terms.
-->

# GlucoRoo Release Notes

## Version 0.2 (Beta) — 2026-04-20

GlucoRoo is a Hammerhead Karoo extension that polls the Dexcom Share API and
displays real-time blood glucose data on your Karoo 2 or Karoo 3 cycling
computer.

### Features

- **22 customizable data tiles** — Value, Trend, Value & Trend, Zone (Circle
  and Box), Dots, Change (5m and 15m), Rainbow, and Graph tiles, each available
  in standard, color, and 15-minute average variants.

- **Real-time CGM polling** — 3-state adaptive polling engine (Discovery,
  Synchronization, Steady-State) that locks onto the CGM's 5-minute cadence
  using monotonic clock scheduling. Typical data latency ~20-25 seconds.

- **Zone alerts** — Visual (InRideAlert) and audio (PlayBeepPattern) alerts
  when glucose crosses zone boundaries during a ride. Descending tones for
  falling glucose, ascending for rising. Per-zone visual and audio toggles.

- **Color modes** — Three-color (red/yellow/green) and Full Color (smooth
  gradient) background options for supported tiles. Rainbow gradient tiles
  with per-mg/dL color interpolation.

- **Dark and light mode** — Automatic theme detection with dark zone color
  variants for readability in light mode.

- **FIT recording** — Optional glucose data recording to the ride FIT file
  for post-ride analysis in third-party tools.

- **Settings Activity** — CGM account configuration with 3-step validation
  (authenticate, login, data probe). Display and log settings for units,
  zone thresholds, graph scale, color backgrounds, and message toggles.

- **10 languages** — English, German, Spanish, French, Italian, Japanese,
  Korean, Portuguese, Simplified Chinese, Traditional Chinese.

- **Alert queue** — Sequential alert dispatch with resolution rules that
  prevent contradictory or redundant messages during a ride.

- **Rolling log files** — Up to 5 rotating log files for diagnostics,
  with glucose values and credentials masked for privacy.

- **Sensor gap handling** — Automatic buffer maintenance (180-minute sliding
  window), continuous-sequence dot display, and 15-minute average minimum
  reading requirements for accurate data after sensor warmup.

### Known Limitations

- InRideAlerts are only visible during active ride recording on Karoo 2.
  Pre-ride alerts are queued and flushed when the ride starts.

- Dexcom Share API only — Dexcom Web API and LibreLinkUp are defined in the
  data model but not yet implemented.


---

*GlucoRoo is not a medical device. See the LICENSE file for full terms.*
