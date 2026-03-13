```
 ██████╗ ██████╗  ██████╗ ██╗  ██╗██╗███████╗     ██████╗██████╗  █████╗ ███████╗██╗  ██╗
██╔════╝██╔═══██╗██╔═══██╗██║ ██╔╝██║██╔════╝    ██╔════╝██╔══██╗██╔══██╗██╔════╝██║  ██║
██║     ██║   ██║██║   ██║█████╔╝ ██║█████╗      ██║     ██████╔╝███████║███████╗███████║
██║     ██║   ██║██║   ██║██╔═██╗ ██║██╔══╝      ██║     ██╔══██╗██╔══██║╚════██║██╔══██║
╚██████╗╚██████╔╝╚██████╔╝██║  ██╗██║███████╗    ╚██████╗██║  ██║██║  ██║███████║██║  ██║
 ╚═════╝ ╚═════╝  ╚═════╝ ╚═╝  ╚═╝╚═╝╚══════╝    ╚═════╝╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝
```

<div align="center">

### 🍪 Match. Swap. Crash. Repeat. 🍪

*A gravity-powered match-3 browser game — no installs, no nonsense, just cookies.*

[![Play Now](https://img.shields.io/badge/▶%20Play%20Now-Open%20in%20Browser-facc15?style=for-the-badge&labelColor=1a0a2e)](#)
[![Version](https://img.shields.io/badge/Version-1.0.0-ec4899?style=for-the-badge&labelColor=1a0a2e)](#)
[![License](https://img.shields.io/badge/License-MIT-4ade80?style=for-the-badge&labelColor=1a0a2e)](#)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-3b82f6?style=for-the-badge&labelColor=1a0a2e)](#)

</div>

---

## 🌌 What Is This?

Somewhere between a bakery and a black hole, **Cookie Crash** was born.

It started as a **C++ OpenGL** experiment — raw pixels, raw frustration, raw fun. Then it evolved into a sleek, zero-dependency browser game that runs anywhere HTML does. You swap colorful cookies, create matches of 3 or more, and watch gravity pull everything down in a beautiful cascade of chaos.

**You have 60 seconds. Make them count.**

---

## 🎮 How to Play

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│   1. 👆  Click any cookie to SELECT it                  │
│                                                         │
│   2. 👆  Click an ADJACENT cookie to SWAP them          │
│                                                         │
│   3. 💥  Match 3 or more in a row / column = POINTS     │
│                                                         │
│   4. 🌊  Gravity pulls cookies DOWN automatically       │
│                                                         │
│   5. ⛓️   Chain reactions earn BONUS POINTS              │
│                                                         │
│   6. ⏱️   60 seconds on the clock — GO!                 │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

> 💡 **Pro tip:** Invalid swaps (ones that don't create a match) are automatically reversed. No penalty — the game's fair like that.

---

## 🍪 The Cookie Roster

| Cookie | Color | Personality |
|:------:|-------|-------------|
| 🔴 | **Crimson** | Bold. Fearless. Always shows up first. |
| 🟢 | **Emerald** | Cool, calm, always in the mix. |
| 🔵 | **Cobalt** | Rare. Mysterious. Worth chasing. |
| 🟡 | **Amber** | Sweet like honey. Sneaks up on you. |
| 🩷 | **Magenta** | The wildcard. Pure chaos energy. |

---

## ✨ Features

```
✅  Smart swap detection    — only valid moves accepted; bad swaps undo instantly
✅  Real gravity            — cookies fall and fill gaps just like the original C++ version
✅  Chain reactions         — cascading matches score automatically in sequence
✅  Score system            — +10 points per matched cookie
✅  Best score tracking     — persists across rounds within your session
✅  Countdown timer         — color bar shifts green → yellow → red as time runs out
✅  Score popups            — satisfying floating +points on every combo
✅  Zero dependencies       — pure HTML + CSS + JS, no libraries, no frameworks
✅  Single file             — the entire game lives in one index.html
```

---

## 🚀 Getting Started

**Option 1 — Just open it:**
```
Download index.html → Double-click → Play
```

**Option 2 — GitHub Pages:**
```bash
git init
git add index.html README.md
git commit -m "🍪 initial cookie crash release"
git push origin main
# Enable Pages: Settings → Pages → Source: main → Save
# Live at: https://yourusername.github.io/your-repo/
```

**Option 3 — Local server:**
```bash
python -m http.server 8080
# Open: http://localhost:8080
```

> ⚠️ **GitHub Pages note:** The file **must** be named `index.html` at the repo root, otherwise you'll get a 404.

---

## 📊 Scoring

```
┌──────────────┬────────────────────────────┐
│  Match 3     │  30 points                 │
│  Match 4     │  40 points                 │
│  Match 5     │  50 points                 │
│  Match N     │  N × 10 points             │
│  Cascade     │  Each wave scores fresh    │
└──────────────┴────────────────────────────┘

Stack cascades → maximum cookie carnage → highest score wins.
```

---

## 🏗️ Architecture

```
index.html
│
├── 🎨  CSS
│   ├── Deep space background (radial gradients + star field)
│   ├── Cookie cells  (hover / selected / clearing / falling states)
│   ├── Animated score popups
│   └── Game-over overlay
│
├── 🧩  HTML
│   ├── Stats bar  (Score · Timer · Best)
│   ├── Animated timer progress bar
│   ├── 10 × 10 grid container
│   └── Game-over screen with restart button
│
└── ⚙️  JavaScript Engine
    ├── initGrid()               → fills grid, resolves starting matches
    ├── resolveInitialMatches()  → prevents pre-existing matches on load
    ├── findMatches()            → horizontal + vertical 3-or-more detection
    ├── applyGravity()           → drops cookies down, spawns new from top
    ├── processMatches()         → recursive cascade handler with animation
    ├── onCellClick()            → selection + swap + validation logic
    ├── renderGrid()             → full DOM render, optional fall animation
    ├── startTimer()             → interval countdown with visual bar
    └── startGame()              → complete reset and game initialisation
```

---

## 🧬 Origin Story

This game began as a **C++ / OpenGL desktop app** using GLEW and FreeGLUT:

```cpp
// The original grid — rendered with raw OpenGL triangle fans
void DrawCircle(float x, float y, float r, float* c) {
    glColor3fv(c);
    glBegin(GL_TRIANGLE_FAN);
    for (int i = 0; i <= 360; i += 10)
        glVertex2f(x + r * cos(i * M_PI / 180),
                   y + r * sin(i * M_PI / 180));
    glEnd();
}
```

The web version keeps the **exact same core logic** — same 10×10 grid, same gravity algorithm, same match detection — translated from C++ to JavaScript and dressed up for the browser age.

---

## 🛠️ Customization

All config is at the top of the `<script>` tag:

```javascript
const ROWS      = 10;   // Grid height
const COLS      = 10;   // Grid width
const GAME_TIME = 60;   // Seconds per round

// Change to rand6() and add .cookie-5 CSS for a 6th colour
function rand5() { return Math.floor(Math.random() * 5); }
```

Want a harder game? Change `GAME_TIME = 30`. Want a bigger grid? Change `ROWS = 12, COLS = 12`. It's that clean.

---

## 🗺️ Roadmap

```
□  High score leaderboard  (localStorage)
□  Special cookies         (bomb · rainbow · row-clear)
□  Difficulty levels       (more colours = harder)
□  Sound effects
□  Mobile touch support
□  Combo multiplier display
□  Animated background particles
```

---

## 📁 File Structure

```
your-repo/
├── 📄  index.html    ← The entire game (one file, ships everything)
└── 📄  README.md     ← You are here 👈
```

---

## 📜 License

**MIT** — do whatever you want with it. Fork it, remix it, ship it, sell it.  
Just don't blame us when you lose three hours of your afternoon to it.

---

<div align="center">

designed by Um e Habiba.

*"One more swap." — everyone, always*

</div>
