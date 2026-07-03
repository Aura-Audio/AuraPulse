<p align="center">
  <img src="https://img.shields.io/badge/Web_Audio_API-Synthesizer-FF5252?style=flat-square&logo=webaudio" />
  <img src="https://img.shields.io/badge/TailwindCSS-Utility--First-38BDF8?style=flat-square&logo=tailwindcss" />
  <img src="https://img.shields.io/badge/Vanilla_JS-ES6+-F7DF1E?style=flat-square&logo=javascript" />
  <img src="https://img.shields.io/badge/Status-Active-3DFFA2?style=flat-square" />
</p>

<h1 align="center">🌌 PulseForge</h1>
<p align="center">
  <strong>A generative, multi-band spatial rhythm synthesizer built for the modern browser.</strong><br>
  <em>Explore the intersection of psychoacoustics, ambient sound design, and reactive visual art.</em>
</p>

---

## 📖 Overview

**PulseForge** is a browser-based ambient and rhythmic sound design tool. Unlike traditional step-sequencers, PulseForge generates complex, evolving polyrhythms through the interference of independent, modulated frequency bands. 

Inspired by brainwave states (Delta, Theta, Alpha, Beta, Gamma), each band operates as an autonomous synthesizer voice featuring deep amplitude modulation, resonant filtering, and spatial panning. The application pairs a high-performance **Web Audio API** engine with a custom **HTML5 Canvas** visualizer, creating a lush, immersive audio-visual experience with zero external dependencies or backend requirements.

---

## ✨ Core Features

### 🎛️ Advanced Audio Engine
* **5 Independent Synth Voices:** Spanning sub-bass (Delta) to high-frequency textures (Gamma).
* **Dual-LFO Modulation System:** 
  * *Amplitude LFO:* Shapes the rhythmic pulse using Sine, Triangle, and Ramp waveforms.
  * *Filter LFO:* Modulates the Biquad Filter cutoff frequency to create "wobble", "sweep", and "talking" synth textures.
* **Biquad Filters & Resonance:** Per-band Low-Pass, High-Pass, and Band-Pass filters with adjustable Q (resonance) for squelchy or smooth tonal shaping.
* **Spatial Audio:** Per-band Stereo Panning with visual feedback, allowing users to carve out a wide, immersive stereo field.
* **Master Bus Processing:** A global `DynamicsCompressor` prevents clipping and "glues" the mix together when all bands overlap.
* **Anti-Aliasing & Smoothing:** Uses `setTargetAtTime` for all parameter changes to eliminate zipper noise and audio clicks.

### 🎨 Reactive Visualizer
* **Spatial Radial Canvas:** Visual rings represent each frequency band. Panning a sound left or right physically shifts its visual representation on the canvas.
* **Particle Emission System:** Particles burst from the rings during amplitude peaks, with decay physics tied to the audio envelope.
* **Real-Time Oscilloscope:** A dedicated waveform monitor displays the summed audio output of the master bus.
* **Mini-LFO Scopes:** Dedicated visual feedback for every modulation envelope, displaying the exact phase and shape of the LFOs.

### 💻 UI / UX Design
* **Dark-Mode Aesthetic:** A carefully calibrated color palette designed for long sound-design sessions.
* **Responsive Grid Layout:** Fully adaptive UI that scales beautifully from mobile devices to ultrawide monitors.
* **Zero-Latency Interactivity:** Decoupled animation loops (`requestAnimationFrame`) from the audio rendering thread to ensure 60FPS visuals without audio dropouts.

---

## 🛠️ Tech Stack

| Technology | Usage |
| :--- | :--- |
| **Web Audio API** | Core synthesis, routing, Biquad Filters, Panning, and Compression. |
| **HTML5 Canvas API** | High-performance 2D rendering for the radial visualizer and oscilloscope. |
| **Vanilla JavaScript** | ES6+ architecture, state management, and DOM manipulation. |
| **Tailwind CSS** | Utility-first styling for rapid, responsive UI development. |

---

## 🚀 Getting Started

PulseForge runs entirely in the browser. No build step or server is strictly required, though a local server is recommended to avoid CORS issues if you decide to load external audio samples in the future.

1. **Clone the repository:**
```bash
   git clone https://github.com/yourusername/pulseforge.git
   cd pulseforge
```
2. **Run the application:**
   Simply open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari).
   *Alternatively, use a local server:*
```bash
   npx serve
```
3. **Initialize Audio:**
   Click the **START** button. *(Note: Modern browsers require a user gesture to initialize the Web Audio API context).*

---

## 🗺️ Roadmap

PulseForge is continuously evolving. Below is the planned roadmap for future feature additions:

### Phase 1: Time & Space (Global Effects)
- [ ] **Global Delay Bus:** Tempo-synced delay with feedback and ping-pong routing.
- [ ] **Convolution Reverb:** Algorithmic and impulse-response based spatial reverberation.
- [ ] **Send/Return Routing:** Per-band "FX Send" knobs to route audio into the global delay/reverb buses.

### Phase 2: Rhythm & Groove (Sequencing)
- [ ] **Euclidean Rhythms:** Algorithmic generation of complex, organic polyrhythms (e.g., 5 hits distributed over 16 steps).
- [ ] **Step Sequencer Grid:** A toggleable 16-step grid per band to trigger discrete ADSR envelopes instead of continuous LFOs.
- [ ] **Microtiming / Swing:** Global swing parameters to delay off-beats and inject "human groove" into the generative patterns.

### Phase 3: Timbre Expansion
- [ ] **Noise Generators:** White, Pink, and Brown noise toggles for hi-hats, snares, and atmospheric textures.
- [ ] **Sample Playback:** Drag-and-drop `.wav`/`.mp3` support using `AudioBufferSourceNode` for custom one-shot triggers.
- [ ] **Waveshaper (Saturation):** Per-band distortion and tape saturation curves for harmonic warmth.

### Phase 4: Pro Workflows
- [ ] **MIDI Mapping:** Web MIDI API integration to map hardware synth knobs and faders to PulseForge parameters.
- [ ] **Preset Management:** Save and load custom soundscapes to browser `LocalStorage`.
- [ ] **Offline Audio Export:** Render and export the current generative session as a `.wav` file using the `OfflineAudioContext`.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! 
If you have an idea for a new Web Audio API node integration or a visual optimization, feel free to fork the repo and submit a Pull Request.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="center">
  <sub>Built with 🎧 and the Web Audio API. No data leaves your browser.</sub>
</p>
