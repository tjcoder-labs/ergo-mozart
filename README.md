# 🎹 Ergo-Mozart

Ergo-Mozart is a "Production Compiler" that transforms high-level musical concepts into professional DAW project files. Instead of generating raw audio, it generates the **instruction set** (MIDI, Track Layout, and Plugin Parameters) required to build a high-production-value track.

## 🚀 The Core Concept
Most AI music tools (like Suno/Udio) generate monolithic .mp3 files. Ergo-Mozart moves **upstream**, treating a song as a structured data object.

**The Pipeline:**
`Conceptual Prompt` $\rightarrow$ `Song-State JSON` $\rightarrow$ `REAPER Lua Script` $\rightarrow$ `DAW Project`

## 🛠️ Quick Start (PoC)

### Prerequisites
- **REAPER DAW** installed on Linux.
- **Python 3.x**
- (Optional) **Yabridge** if using Windows VSTs on Linux.

### Running the PoC
1. Clone the repo:
   ```bash
   git clone https://github.com/tjcoder-labs/ergo-mozart.git
   cd ergo-mozart
   ```
2. Run the compiler:
   ```bash
   python3 reaper_compiler.py
   ```
3. This generates a `build_song.lua` file.
4. Open REAPER $\rightarrow$ Actions $\rightarrow$ Run Script $\rightarrow$ Select `build_song.lua`.

## 📈 Roadmap
- [x] Basic Track/Tempo Layout Generation.
- [ ] **MIDI Generation:** Programmatic creation of "Pop" grids (Kick/Snare/Bass).
- [ ] **Plugin Mapping:** Auto-loading specific VST presets based on sound descriptions.
- [ ] **Automation Engine:** Generating filter sweeps and energy transitions.
