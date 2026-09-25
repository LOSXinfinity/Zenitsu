# GOD OF THUNDER — 雷の呼吸 · Zenitsu Agatsuma

A button-driven, single-page interactive showcase featuring Zenitsu Agatsuma from *Demon Slayer: Kimetsu no Yaiba*. Experience Thunder Breathing through three cinematic scenes with procedural lightning, spatial audio, and a split-reveal slider.

## 🎬 Scenes

| Scene | Title | Description |
|-------|-------|-------------|
| **I** | **THE FALL** | Zenitsu descends through a light, ethereal sky. Ambient golden lightning flickers, Japanese kanji drift, and the hero title rests behind him. |
| **II** | **THE IMPACT** | He lands — ground cracks propagate, heavy bottom-center thunder strikes roll in intervals, and the horizontal "Godspeed" figure sprints into center with motion-trail ghosts. |
| **III** | **AWAKENING** | The running figure zooms to the bottom-left corner and merges into a **split-reveal slider**: drag the lightning blade to wipe from sleeping Zenitsu to awakened Zenitsu. Fast drags trigger continuous heavy thunder. |

## ✨ Features

- **Procedural Lightning Engine** — Midpoint-displacement fractal bolts with corona, haze, sheath, and core layers; restrike sequences (main flash → dark gap → return strokes).
- **Layered Thunder Audio** — Web Audio API: crack (high-pass snap), rolling body (low-pass sweep), sub-rumble (ultra-low). Gated by first user interaction.
- **Liquid Ether Background** — Cursor-reactive, flowing soft blobs in thunder palette (blue/gold/purple).
- **Blue Thunder Aura** — Procedural bolts orbiting the falling figure (Scene 0).
- **Ground Crack System** — Fractal cracks drawn to a canvas, animated reveal on impact.
- **Split-Reveal Slider** — Tilted lightning blade clips the top image; sparks emit on drag; corner figure slides in sync.
- **Custom Cursor** — Gold-ringed cursor with core glow, hidden on touch.
- **HUD** — Real-time clock, breathing state, form readout (Space Mono / Pirata One / Shippori Mincho).
- **Light Theme (Scene 0)** — Greyish-white gradient sky; Scenes 1–2 stay dark cinematic.
- **Reduced Motion** — Respects `prefers-reduced-motion`; disables all non-essential animation.
- **No Scroll** — Button/keyboard driven navigation (Prev/Next, Arrow keys).

## 🛠️ Tech Stack

- **Vanilla HTML/CSS/JS** — Single `index.html` (≈1200 lines), no build step.
- **GSAP 3.12** — Timeline-driven scene transitions, easing, and scroll-free navigation.
- **Canvas 2D** — Lightning, wind streaks, ether blobs, cracks, split sparks, aura.
- **Web Audio API** — Procedural thunder synthesis (no audio files).
- **Google Fonts** — Bebas Neue, Pirata One, Space Mono, Shippori Mincho.

## 🚀 Quick Start

```bash
# Serve locally (required for Web Audio + ES modules)
npx serve .
# or
python -m http.server 8080
```

Open `http://localhost:8080` (or the port shown). **Interaction required** before audio plays (browser policy).

## 🎮 Controls

| Input | Action |
|-------|--------|
| **Next button / →** | Advance scene |
| **Prev button / ←** | Previous scene |
| **Drag (Scene III)** | Slide the lightning blade to reveal awakened Zenitsu |
| **Mouse move** | Custom cursor + ether blob attraction |

## 📁 Project Structure

```
Zenitsu/
├── index.html          # Complete experience (HTML + CSS + JS)
├── img/
│   ├── top.png         # Sleeping Zenitsu (split reveal bottom layer)
│   ├── bottom.png      # Awakened Zenitsu (split reveal top layer)
│   ├── falling.png     # Large falling figure (Scene 0)
│   └── horizontal-run.png  # Running figure + ghost trails (Scenes 1–2)
└── README.md
```

## 🎨 Visual Language

- **Sky** — Storm-night navy (`#0a0e1c`) → Light gradient (Scene 0 only)
- **Bolt** — Gold `#ffd94a` → Deep `#f0a92e`
- **Core** — Ice white `#eaf6ff` → Blue `#7ec8ff`
- **Typography** — Kanji: Shippori Mincho; Display: Pirata One; UI: Space Mono / Bebas Neue

## ⚡ Performance Notes

- DPR capped at 2× for canvas backing stores.
- `will-change` on animated layers; `mix-blend-mode: screen` for additive lightning.
- `requestAnimationFrame` loops paused when tab hidden (`document.hidden`).
- All heavy work in single JS closure; no external deps beyond GSAP CDN.

## 📜 License

Fan project for *Demon Slayer: Kimetsu no Yaiba*. Characters © Koyoharu Gotouge / Shueisha / Aniplex / Ufotable. Code: MIT — do whatever, credit appreciated.

---

> 「雷の呼吸 壱ノ型 霹靂一閃」 — *Thunder Breathing, First Form: Thunderclap and Flash*