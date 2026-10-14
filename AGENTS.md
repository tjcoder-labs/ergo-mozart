# 🎭 The Ergo-Mozart Production Crew

This project uses an agentic orchestration pattern to decompose music production into modular, specialized roles.

## 🏗️ Agent Hierarchy

### 1. Ergo-Mozart (The Orchestrator)
- **Role:** Creative Director.
- **Responsibilities:** 
  - Maintains the `song_state.json`.
  - Manages the "Energy Map" (Tension/Release).
  - Delegates tasks to the specialists.
- **Primary Goal:** Ensure the final project matches the high-level "Sonic North Star."

### 2. The Analyst (The Spec Writer)
- **Role:** Musicologist / Deconstructor.
- **Responsibilities:** 
  - Analyzes reference tracks.
  - Extracts BPM, Key, and Arrangement (Intro, Verse, Chorus).
  - Defines the "Required Elements" for the track.

### 3. The Sequencer (The MIDI Coder)
- **Role:** Rhythmic and Harmonic Architect.
- **Responsibilities:** 
  - Generates the MIDI patterns.
  - Manages the "Pocket" (Swing, Velocity, Quantization).
  - Focuses on the foundation: Kick, Snare, and Bass.

### 4. The Librarian (The Patch Matcher)
- **Role:** Sound Designer.
- **Responsibilities:** 
  - Maps "Sound Descriptions" (e.g., "Sharp Lead") to VST Presets.
  - Manages the frequency spectrum (Sub, Mid, Top).
  - Specifies plugin parameters (Cutoff, Resonance).

### 5. The Assembler (The DAW Driver)
- **Role:** Technical Implementation.
- **Responsibilities:** 
  - Translates the Song-State into the REAPER API.
  - Automates the creation of tracks and clips.
  - Executes the final "build" of the project.

## 🛠️ Tooling & Integration
- **Compiler:** `reaper_compiler.py` (Python $\rightarrow$ Lua).
- **Host:** REAPER DAW (Linux).
- **Bridge:** Yabridge (Windows VST $\rightarrow$ Linux).
- **Communication:** JSON-based Song-State.
