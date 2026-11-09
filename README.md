# Zen Blocks — A Minimalist Web Prototype

A mobile-first web puzzle inspired by the core mechanics of *Block Blast!*, engineered with web technologies and zero external dependencies.

🔗 **Live Demo:** https://zen-blocks-mu.vercel.app/

---

## ✨ Features & Architecture

- **Hybrid Input System:** Seamlessly supports both touch/mouse drag-and-drop with real-time snap-to-grid physics and accessible tap-to-select / tap-to-place controls.
- **Procedural Audio (Web Audio API):** Zero audio asset downloads. Generates melodic ascending welcome chimes, placement feedback, and dynamic combo chords directly in browser memory, with persistent sound mute toggle.
- **Dynamic Theming:** Warm Zen Light theme alongside a Midnight Dark mode, persisted via `localStorage`.
- **Predictive Game Over Scan:** Executes an $O(\text{Pieces} \times \text{BoardSize}^2)$ spatial matrix check to prevent deadlocks and detect game-over states in advance.
- **Zero-Dependency Footprint:** Everything is packaged into a single, self-contained `index.html` file optimized for instant web loading.

---

## 🛠️ Tech Stack

- **HTML5 Canvas & DOM** (Particles & UI)
- **CSS3 Variables & Flex/Grid** (Responsive layout & themes)
- **JavaScript (ES6+)** (Matrix collision logic & state management)
- **Web Audio API** (Procedural synthesis)
