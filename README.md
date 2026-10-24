# ChronoFlow — Precision Pomodoro & Analytics Studio

A complete single-file Pomodoro & Deep Work web application (`index.html` / `pomodoro_app.html`) paired with a background Service Worker (`sw.js`) and PWA manifest (`manifest.json`) for reliable OS banner & lock-screen push notifications.

## 4-Layer Push Notification Architecture (Banner, Lock Screen, Background, Pinned & Closed Chrome)
1. **Persistent OS Banner & Lock-Screen Alerts (`sw.js` + `Notification` API)**: Uses `requireInteraction: true`, `renotify: true`, `vibrate`, and interactive action buttons (`✓ Confirm Alarm`, `▶ Start Next`).
2. **Background & Pinned Tab Anti-Throttling**: Combines a dedicated **Blob Web Worker** (250ms tick thread) with a sub-audible **Silent Web Audio Keep-Alive** stream + `navigator.mediaSession` + `navigator.wakeLock` so Chrome never throttles or freezes the countdown when minimized or pinned.
3. **Service Worker Timer Offload (`SCHEDULE_TIMER_NOTIFICATION` + `TimestampTrigger`)**: Pre-schedules the exact completion timestamp inside `sw.js` via `event.waitUntil` and `TimestampTrigger` so the notification fires even if the tab is closed (keep *"Continue running background apps when Google Chrome is closed"* enabled in `chrome://settings/system`).
4. **Closed-Browser Cloud Push Relay (`ntfy.sh` Scheduled Delivery)**: Built-in zero-signup Cloud Push Relay (`X-In` header) in the **⚡ Test & Lock-Screen Setup** modal—schedules the alert in the cloud as soon as a Pomodoro starts so your phone/desktop lock screen still receives the notification even if Chrome is completely quit.
