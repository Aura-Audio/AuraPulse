# AuraPulse ⚡

A powerful, browser-based multi-band rhythm and pulse generator with real-time LFO modulation and audio visualization. Built entirely with vanilla HTML, CSS, and JavaScript using the Web Audio API.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Web Audio API](https://img.shields.io/badge/API-Web_Audio-orange.svg)
![Zero Dependencies](https://img.shields.io/badge/dependencies-zero-brightgreen.svg)

---

## Overview

PulseForge generates rhythmic pulses and beats across 5 customizable frequency bands. Rather than static tempos, each band's pulse frequency is continuously shaped by a Low-Frequency Oscillator (LFO), sweeping between your defined low and high endpoints over a set duration. 

Whether you're exploring binaural/isochronic tones, designing complex polyrhythmic textures, creating meditative soundscapes, or just need a highly customizable metronome on the fly—PulseForge runs entirely in your browser with zero backend requirements.

## Features

### 🎵 Core Audio Engine
- **Web Audio API:** Low-latency, high-precision audio scheduling directly in the browser.
- **Dynamic Compression:** Built-in master compressor prevents clipping when layering multiple loud bands.
- **Real-time Modulation:** All parameters (frequency, volume, LFO) update seamlessly in real-time without audio glitches using `setTargetAtTime`.

### 🎛️ Multi-Band Architecture (5 Bands)
- **Delta (0.5–4 Hz):** Deep, slow pulses. Carrier: 55 Hz (Sine)
- **Theta (4–8 Hz):** Dreamy, hypnotic rhythms. Carrier: 110 Hz (Sine)
- **Alpha (8–14 Hz):** Relaxed, flowing beats. Carrier: 220 Hz (Triangle)
- **Beta (14–30 Hz):** Active, driving pulses. Carrier: 440 Hz (Triangle)
- **Gamma (30–50 Hz):** Rapid, buzzing tremolo. Carrier: 880 Hz (Sine)

### 🌊 LFO Modulation
- **Sweep Controls:** Define the `Low` and `High` Hz values for the LFO to sweep between.
- **Duration:** Set the loop length (1–60 seconds) for one full LFO cycle.
- **3 LFO Shapes:**
  - *Ramp:* Sawtooth style, jumps from High back to Low.
  - *Triangle:* Smooth, linear ascent and descent.
  - *Sine:* Smooth, logarithmic-style curve.

### 🎚️ Per-Band Controls
- **Enable/Disable:** Toggle bands independently.
- **Carrier Frequency & Waveform:** Change the pitch (20–2000 Hz) and tone (Sine, Triangle, Sawtooth, Square).
- **Volume:** Independent amplitude control.
- **Sharpness:** Morph pulses from gentle volume swells (low sharpness) to tight, clicky beats (high sharpness).

### 🎨 Visualization
- **Concentric Ring Visualizer:** Each band is represented by a glowing, pulsing ring that expands and contracts with the audio amplitude.
- **Particle System:** Particles emit from the rings on pulse peaks.
- **Waveform Display:** Real-time oscilloscope of the master audio output.
- **LFO Mini-Maps:** Visual display of the LFO curve and current playback position per band.

---

## Roadmap

### Phase 1: Core Enhancements
- [ ] **Preset System:** Save and load custom configurations (Local Storage).
- [ ] **Tap Tempo:** Tap a button to automatically set the pulse Hz based on tapping speed.
- [ ] **BPM Mode:** Toggle UI from Hz to BPM (Beats Per Minute) for musical context.
- [ ] **Phase Offset:** Control the starting phase of each band's LFO to create syncopated polyrhythms.

### Phase 2: Audio Expansion
- [ ] **Audio Export:** Record and download the generated output as `.wav` or `.mp3`.
- [ ] **Binaural Mode:** Route alternating bands to Left/Right ears for binaural beat generation.
- [ ] **Custom LFO Drawing:** Draw custom LFO curves directly on the mini-map canvas.
- [ ] **Sample Integration:** Replace oscillator carriers with uploaded audio samples (e.g., drum hits, vocal chops).

### Phase 3: Visual & UX Upgrades
- [ ] **WebGL / Three.js Visualizer:** Upgrade the 2D canvas to a 3D reactive environment.
- [ ] **Full-Screen Mode:** Distraction-free visualization mode.
- [ ] **Color Themes:** Alternative UI themes (e.g., Light mode, Cyberpunk, Pastel).
- [ ] **MIDI Integration:** Map band controls to physical MIDI controllers via the Web MIDI API.

### Phase 4: Collaboration
- [ ] **Shareable URLs:** Encode current settings into URL parameters for instant sharing.
- [ ] **WebRTC Sync:** Link multiple browsers together to sync pulse sessions over the internet.

---

## Getting Started

No build tools, bundlers, or servers required.

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/pulseforge.git
   ```
2. Open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari).

*Note: Browsers require a user interaction (like clicking "START") before allowing audio playback due to autoplay policies.*

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
