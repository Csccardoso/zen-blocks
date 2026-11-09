# 🧩 Zen Blocks - Minimalist Block Puzzle Prototype

A mobile-first web puzzle inspired by the core mechanics of *Block Blast!*, engineered with web technologies and zero external dependencies.

🔗 **Live Demo:** [https://zen-blocks-mu.vercel.app/](https://zen-blocks-mu.vercel.app/)

---

## ⚡ Highlights & Engineering Decisions

- **Hybrid Input Architecture:** Full unified pointer lifecycle (`pointerdown`, `pointermove`, `pointerup`, `pointercancel`) supporting both touch/mouse drag-and-drop with real-time snap-to-grid projection, alongside an accessible tap-to-select fallback.
- **Mobile Touch Ergonomics:** Implements a dynamic vertical touch offset ($70\text{px}$) during mobile drags so the user's thumb does not obstruct placement previews. Employs `setPointerCapture` to eliminate drag tearing during rapid swipes.
- **Procedural Audio Engine (Web Audio API):** Zero network latency or external audio assets. Synthesizes an ascending welcome chime, tactile placement drops, and ascending pentatonic combo chords directly in browser memory, respecting global mute persistence and browser autoplay policies.
- **Predictive Game Over Scanner:** Runs an $O(\text{Pieces} \times N^2)$ spatial matrix check after every state change ($\le 192$ checks per turn) to pre-disable unplayable pieces and detect deadlocks with sub-millisecond execution.
- **Responsive Theme System:** Custom CSS variables delivering a Midnight Dark palette and a warm Sandstone/Linen Zen palette, persisted across sessions via `localStorage`.
- **Zero-Dependency Single-File Delivery:** Fully contained inside one `index.html` file combining semantic HTML, CSS styling, Canvas particle effects, and game loop logic.

---

## 🤖 AI-Assisted Prototyping Workflow

Built as part of an AI-assisted rapid game prototyping challenge:

1. **Scaffolding & Architecture:** Directed AI to establish clean separation between state management, matrix validation math, Canvas particle rendering, and the Web Audio synthesizer.
2. **Iterative Refinement:** Guided iterative feedback loops to solve UX friction points—transitioning from pure click-to-place to a hybrid pointer-captured drag engine with coordinate-snapping projection.
3. **Ergonomics & Polish:** Prompt-engineered precise synthesizer frequency ladders (pentatonic progression for combos) and custom warm palettes to meet "Zen" aesthetic guidelines.
4. **Verification & Code:** Audited generated code for W3C compliance (e.g., multi-browser `background-clip` support), deterministic collision bounds, and efficient DOM footprint.

---

## 🛠️ Tech Stack

- **HTML5 Canvas & DOM** (Particles, board geometry, and UI layering)
- **Modern CSS3** (CSS Custom Properties, CSS Grid, hardware-accelerated transforms)
- **JavaScript (ES6+)** (2D matrix collision algorithms & state loops)
- **Web Audio API** (Procedural synthesis via oscillators and gain envelopes)
- **Deployment:** Vercel (Continuous Deployment via GitHub)

---

## 🚀 Running Locally

Because the prototype is self-contained with no package manager or build step required:

```bash
# Clone the repository
git clone https://github.com/Csccardoso/zen-blocks.git
cd zen-blocks

# Open directly in any modern browser
# On macOS: open index.html
# On Windows: start index.html
# On Linux: xdg-open index.html

# Or run with any local static server (e.g., Live Server or npx serve)
npx serve .
