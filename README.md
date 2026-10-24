# DailyVibe: iOS Aesthetic Studio

A production-ready, **single-file Progressive Web App** with an iOS-inspired aesthetic studio experience.

**Live-ready for mobile browsers & Web-to-APK packaging.**

---

## Features

### iOS-Inspired UI
- Dynamic Island / status bar (time, Wi-Fi, battery)
- Deep OLED dark mode + glassmorphism cards (`backdrop-filter: blur`)
- Smooth micro-interactions & mobile-first layout
- Safe-area aware (notch / home indicator)

### Theme Studio (24 themes)
- **12 Free** + **12 Pro** themes
- Instant live theme switcher via CSS variables (no page reload)
- Easy to expand from 24 → 40+ themes (clean `THEMES` array)

### Monetization Hooks
- Pro themes show a lock badge
- Unlock modal simulates **Rewarded Ad** or **$1.99 Pro Pass**
- Ready for AdMob / Stripe / Google Play Billing integration

### Wallpaper Download
- One-tap “Save Wallpaper” generates a high-res PNG and downloads it

### Daily Engagement
- **Streak engine** (LocalStorage) — increments when you open the app daily
- **Daily quote** rotates by UTC date
- **Mood check-in** (Calm / Focused / Energetic) with personalized message

---

## How to Run / Test

### Option 1 — Browser
1. Download or clone this repo
2. Open `index.html` directly in Chrome / Safari / Edge (mobile or desktop with DevTools device mode)

### Option 2 — Mobile IDE (Acode, etc.)
1. Copy `index.html` into Acode or any mobile code editor
2. Open / preview the file in the built-in browser or WebView

### Option 3 — Local server (recommended for PWA testing)
```bash
npx serve .
# or
python3 -m http.server 8080
```
Then open the URL on your phone (same Wi-Fi) or use Chrome remote debugging.

### Option 4 — Web-to-APK
Use any WebView wrapper (e.g. PWA Builder, Capacitor, Cordova, or online Web-to-APK tools) pointing at `index.html` or a hosted URL.

---

## Expanding Themes

Open `index.html` and find the `THEMES` array near the top of the `<script>` block.

Each theme object looks like:

```js
{
  id: 'my-new-theme',
  name: 'My New Theme',
  free: true, // or false for Pro
  vars: {
    '--bg-primary': '#000000',
    '--bg-secondary': '#0a0a0a',
    '--card-bg': 'rgba(255,255,255,0.08)',
    '--card-border': 'rgba(255,255,255,0.12)',
    '--accent': '#0A84FF',
    '--accent-soft': 'rgba(10,132,255,0.25)',
    '--text-primary': '#ffffff',
    '--text-secondary': 'rgba(255,255,255,0.65)'
  },
  wallpaper: 'linear-gradient(160deg, #000000 0%, #111111 100%)'
}
```

Add as many as you like — the grid and count badge update automatically.

---

## Tech Stack

- Single HTML file
- Tailwind CSS (CDN)
- Vanilla ES6+ JavaScript
- LocalStorage for streaks, mood, unlocked themes, and active theme
- Canvas API for wallpaper generation

---

## License

MIT — feel free to use, modify, and ship.
