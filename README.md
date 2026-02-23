# CemiBrainAlpha

CemiBrainAlpha is a single-file, browser-based interactive simulation that blends geometry, graph dynamics, field effects, and adaptive learning into a real-time visual + audio instrument.

It renders **Dₙ/Aₙ Coxeter-plane inspired structures** with GPU-accelerated updates (WebGL2), then layers in:

- Kuramoto-style phase dynamics
- Graph↔field coupling
- Hebbian/STDP-like adaptive edge weights
- Neuromodulatory controls (DA/GLU/GABA style channels)
- Optional ambient sonification of network behavior

The project currently ships as one self-contained HTML app:

- `zimple_modular_lobes-5_audio_ambient_retina_fix16.html`

---

## Features

- **One-file app**: no build step, no external runtime needed
- **WebGL2 simulation pipeline** for high node/edge counts
- **Preset system** for quickly exploring regimes
- **Rich control panel** with searchable parameters
- **Multiple color modes** (phase, weight, coherence, CEMI field, neurotransmitter-style maps, etc.)
- **Hebbian learning controls** (learning rate, decay, STDP asymmetry, reset)
- **Audio engine** with musical scale/root controls and timbral shaping
- **Interactive navigation** (pointer drag, wheel/pinch zoom, panel controls)

---

## Quick Start

### 1) Open the app

You can run it by simply opening the HTML file in a modern desktop browser:

```bash
xdg-open zimple_modular_lobes-5_audio_ambient_retina_fix16.html
```

Or double-click it from your file explorer.

### 2) If local file restrictions appear

Some browser configurations behave better via a lightweight local server:

```bash
python3 -m http.server 8000
```

Then visit:

- `http://localhost:8000/zimple_modular_lobes-5_audio_ambient_retina_fix16.html`

---

## Requirements

- A modern browser with **WebGL2** support
  - Recommended: current Chrome / Edge / Firefox
- Hardware acceleration enabled in browser settings
- Audio requires user interaction first in most browsers (autoplay policy)

---

## Usage Notes

- Click the **gear icon** to show/hide the control panel.
- Use the **search box** (`/` shortcut) to quickly locate parameters.
- Choose a preset and press **Apply** to jump to curated configurations.
- Enable **Audio ON** to sonify network dynamics.
- Toggle **Hebbian ON** to let edge weights adapt over time.

If performance drops:

- Reduce node count / neighborhood complexity
- Lower expensive visual options
- Disable optional systems (audio, heavy overlays)

---

## Project Layout

```text
.
├── README.md
└── zimple_modular_lobes-5_audio_ambient_retina_fix16.html
```

---

## Roadmap Ideas

- Split monolithic HTML into modules (`ui/`, `sim/`, `render/`, `audio/`)
- Add import/export for parameter sets and presets
- Add deterministic benchmark mode and profiling overlay
- Add documentation for model equations and shader passes

---

## License

No license file is currently included in this repository. If you plan to distribute or accept contributions, add an explicit license (e.g., MIT, Apache-2.0, GPL-3.0).
