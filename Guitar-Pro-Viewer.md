# Guitar Pro & MusicXML Viewer

  HAYA-TAB includes a powerful score viewer powered by [alphaTab](https://alphatab.net/).

  ## Supported Formats

  **Guitar Pro:**
  - `.gp3`, `.gp4`, `.gp5` (Guitar Pro 3-5)
  - `.gpx` (Guitar Pro 6)
  - `.gp` (Guitar Pro 7+)

  **MusicXML:**
  - `.xml`, `.musicxml` (Uncompressed MusicXML)
  - `.mxl` (Compressed MusicXML)

  ## Opening Files

  1. Right-click a Guitar Pro or MusicXML tab → **"Open with Inner Viewer"**
  2. Wait for SoundFont to load (progress bar shown)

  ---

  ## Playback Controls

  ### Basic Controls
  | Control | Action |
  |---------|--------|
  | **Play/Pause** | `Space` or ▶️ button |
  | **Stop** | ⏹️ button |
  | **Jump to Start** | `I` (default) |

  ### Speed Control
  - Use the **speed slider** (50% - 200%)
  - Or click the BPM display to enter exact tempo

  ### Track Selection
  - Click the **track dropdown** to switch instruments
  - Each track shows: instrument name, tuning info

  ---

  ## Selection & Looping

  ### Select Measures
  1. **Click** on a measure to select it
  2. **Drag** across measures to select a range
  3. **Shift+Drag** to enter Section Playback Mode

  ### Loop Playback
  1. Select a range of measures
  2. Press **`L`** or click **"Loop"** in the context menu
  3. Playback will repeat the selected section
  4. Press **`L`** again to disable loop

  ### Section Playback Mode
  - Activated by **Shift+Drag** or right-click → "Section Playback"
  - Selection is protected from accidental clicks
  - Press **`Esc`** or click "Clear" to exit

  ### Jump to Bar
  1. Press **`J`** (default) or right-click → "Jump to Bar"
  2. Enter the measure number
  3. Playback cursor moves to that position

  ---

  ## Floating Toolbar

  A quick-access toolbar appears when hovering over the score:

  - **Play/Pause**
  - **Loop Toggle**
  - **Speed Adjustment**
  - **Track Selector**

  The toolbar auto-hides after 3 seconds of inactivity or when scrolling.

  ---

  ## Keyboard Shortcuts

  | Action | Default Key | Customizable |
  |--------|-------------|--------------|
  | Play/Pause | `Space` | ✅ |
  | Toggle Loop | `L` | ✅ |
  | Clear Selection | `Esc` | ✅ |
  | Jump to Bar | `J` | ✅ |
  | Jump to Start | `I` | ✅ |

  Customize in **Settings → Key Bindings**.

  ---

  ## SoundFont

  HAYA-TAB uses the **Sonivox SF3** SoundFont for playback. The SoundFont loads automatically when you first open a GP file.        

  **Loading indicator:** A progress bar shows download progress for the SoundFont file.

  ---

  ## Tips

  - **Metronome:** Enable in the toolbar for practice
  - **Slow Practice:** Set speed to 50% for difficult passages
  - **Loop Sections:** Perfect for practicing specific parts
  - **Multi-track:** Switch tracks to hear different instruments

  ---