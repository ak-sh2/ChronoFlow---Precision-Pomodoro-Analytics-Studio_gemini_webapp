# ChronoFlow — Precision Pomodoro & Progress Analytics Studio

A standalone, zero-backend Pomodoro timer and progress intelligence web application built with HTML5, Tailwind CSS, Chart.js, and the Web Audio API.

## Key Features
- **Canonical Pomodoro Cadence**: 25-minute Focus intervals, 5-minute Short Breaks, and 15-minute Long Breaks every 4 Pomodoros (fully customizable in Settings).
- **Animated SVG Radial Countdown**: 60-segment radial tick marks, smooth depleting arc, and orbiting second indicator.
- **Manual Alarm Confirmation**: Looping completion chime and theme-consistent top notification banner that waits for manual confirmation (`Confirm Alarm` or `Start Next`) before silencing.
- **Custom White Voices & Soundscape Bar**: Built-in Deep Brown, Soft Rain, and White Noise generators plus a **+ Add White Voice** modal to create custom formant-filtered vocal/harmonic soundscapes, upload local audio files (`.mp3`, `.wav`, `.ogg`), or stream custom audio URLs.
- **Daily, Weekly & Monthly Analytics**: Interactive hourly, 7-day, and 30-day progress charts, category breakdown doughnut chart, and 30-day consistency heatmap.
- **Multi-Format Export Studio**: Export recorded sessions and summaries as **CSV** (default), **JSON**, **Markdown (`.md`)**, **Plain Text (`.txt`)**, or **Printable PDF** (`Print / Save PDF`), complete with an inline preview and clipboard copy drawer.
- **Dark & Light Mode**: Instant theme toggle in the top header with consistent surface styling across all banners, modals, toasts, and charts.

## Running Locally or Hosting on GitHub Pages
1. **Run Locally**: Double-click `index.html` (or `pomodoro_app.html`) to open it directly in any modern browser.
2. **Host on GitHub Pages**:
   - Upload `index.html` and `README.md` to your GitHub repository.
   - Go to **Settings -> Pages**, select **Deploy from a branch**, and choose `main` (`/root`).
   - Your live app will be available at `https://<your-username>.github.io/<your-repo>/`.
