# Scientific Dashboard Prank App (v4.2 Mobile Edition)

This is a single-page web application designed to look like a sophisticated physics simulation tool. It serves as a prank that triggers a visual and auditory "glitch" event upon user interaction.

## Features

- **Realistic "Decoy" Interface**: 
  - Dark mode scientific dashboard aesthetics.
  - Live particle system with connection lines (constellations).
  - Dummy data readouts (CPU, GPU, Entropy) that update in real-time.
  - Interactive-looking sliders that do nothing but update numbers.

- **Mobile First Redesign**:
  - Full-screen "app" experience on mobile.
  - Sidebar hidden by default (slide-up panel).
  - HUD overlays for stats.
  - Large, centered "INITIALIZE SYSTEM" button.

- **The Prank**:
  - Clicking "INITIALIZE SYSTEM" triggers chaos.
  - **Sticky Mode**:
    - Attempts to enter Fullscreen and traps the mouse cursor (desktop).
    - Persistent vibration pattern sequences (mobile).
    - **Volume Lock**: Aggressively loops volume to 100% every 50ms to resist user attempts to lower it via software controls.
    - Prevents tab closing via `beforeunload` dialogs and history state pushing.
  - Visuals distort (color shifts, shaking, strobing).
  - Audio plays: Checks for `prank_sound.mp3` locally first, or falls back to synthesized noise.

## Usage

1. **Setup**:
   - Ensure `prank_sound.mp3` is in the same directory as `index.html`.
   - Open `index.html` in any modern web browser (Chrome, Firefox, Edge).

2. **Configuration** (Hidden):
   - Move your mouse/tap to the bottom-right corner of the screen.
   - Click the faint, barely visible white dot (or pixel).
   - A hidden modal will appear.
   - You can override the default audio by entering a URL.
   - **Adjust the "Output Gain" slider** (defaults to 100%).
   - Click "SAVE & DISARM".

3. **Execution**:
   - Ask the "victim" to monitor the simulation.
   - Tell them to click "INITIALIZE SYSTEM" when the entropy stabilizes.
   - Enjoy the reaction.

## Technical Details

- **Stack**: Pure HTML5, CSS3, Vanilla JavaScript.
- **Audio**: Uses Web Audio API for fallback noise generation and HTML5 Audio for the main file.
- **Portability**: Single file (`index.html`) contains all logic, plus one external audio asset (`prank_sound.mp3`).

## Disclaimer

This tool is for educational and entertainment purposes only. Ensure audio volume is at a safe level before deployment, as the software attempts to override volume controls.
