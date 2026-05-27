**Project: `1+1` — Mental Math Speed Trainer PWA**
Built by Claude, live at [hexpredator1-boop.github.io/1p1](https://hexpredator1-boop.github.io/1p1/)  
*Dart version:* Available at [github.com/hexpredator1-boop/1p1-dart](https://github.com/hexpredator1-boop/1p1-dart)

---

**What it is:** A mobile-first Progressive Web App (installable on iOS/Android) for drilling arithmetic at speed. Four operations — addition, subtraction, multiplication, division — each with 5 difficulty levels.

**How it works:**
- Each session picks 15 questions from a shuffled pool matched to the selected op + difficulty
- The player taps a numeric keypad to answer; correct answers auto-advance instantly
- A live timer runs throughout; wrong answers add a **penalty** (300ms per mistake) and trigger a shake animation + haptic vibration
- A **score (0–100%)** is calculated as `idealTime / (actualTime + penalties)`, capped at 100%
- Scores are saved to `localStorage`; perfect 100% scores get logged to a trophy cabinet

**File breakdown:**

| File | Role |
|---|---|
| `index.html` | Entire app — HTML, CSS, and JS in one self-contained file (~1100 lines) |
| `manifest.json` | PWA manifest — makes it installable as a standalone app |
| `sw.js` | Service worker — caches all assets for offline use (cache key: `mathsprint-v6`) |
| `icon.png` | 1024×1024 app icon (the "1+1" logo you shared) |
| `README.md` | core documentation |

**Tech stack:** Vanilla JS, no frameworks. Google Fonts (DM Mono + Space Grotesk). CSS custom properties for theming. `localStorage` for persistence. `requestAnimationFrame` for the live timer.
