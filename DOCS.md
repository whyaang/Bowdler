<div align="center">

![Bowdler](images/guide.png)

</div>

<div align="center">
  <h3>
    <a href="README.md">README</a> · <a href="FAQ.md">FAQ</a> · <a>DOCS</a>
  </h3>
  <p>
    <a>🇺🇸 English</a> · <a href="languages/Chinese/DOCS.md">🇨🇳 中文</a> · <a href="languages/Spanish/DOCS.md">🇪🇸 Español</a> · <a href="languages/Arabic/DOCS.md">🇸🇦 العربية</a> · <a href="languages/Portuguese/DOCS.md">🇧🇷 Português</a> · <a href="languages/Russian/DOCS.md">🇷🇺 Русский</a>
  </p>
</div>

---

## UI Overview

### Main Screen

![Main Screen](images/screenshots/MainScreen.png)

<div align="center">

| # | Element | Description |
|---|---|---|
| 1 | **Current Mode** | The active tab - Censorship, Silence Removal, or Subtitles. Click to switch modes. |
| 2 | **Settings Button** | Opens the settings panel for the current mode. |
| 3 | **Theme Button** | Toggles between dark and light theme. |
| 4 | **Upload Area / Drop Zone** | Drag & drop your media file here, or click to open a file picker. Accepts MP4 · MOV · MP3 · WAV · AAC. |
| 5 | **Current Model** | Shows the active AI engine and model size. Click to change engine or model. |
| 6 | **Process Button** | Starts detection and opens the Review screen when done. |

</div>

---

### Timeline / Review Screen

![Timeline Screen](images/screenshots/TimelineScreen.png)

<div align="center">

| # | Element | Description |
|---|---|---|
| 1 | **Back Button** | Returns to the main screen. |
| 2 | **Video Visibility** | Shows or hides the inline video preview. |
| 3 | **Timeline** | Visual overview of all detected segments. Click anywhere to jump to that position. |
| 4 | **Segment Selection** | Quickly check All or uncheck None to include or exclude every segment at once. |
| 5 | **Custom Range** | Manually add a time range to censor or remove, independent of detection. |
| 6 | **Speed Controls** | Change playback speed: 1x · 1.25x · 1.5x · 2x. |
| 7 | **Zoom Controls** | Zoom in or out on the waveform to inspect segments more precisely. |
| 8 | **Playback Controls** | Play/pause and skip −10s · −1s · +1s · +10s. |
| 9 | **Segment Mute** | Toggle checkbox - controls whether this segment is included in the export. |
| 10 | **Play Segment** | Previews just this one segment in isolation. |
| 11 | **Detected Word** | The word flagged by the model for this segment. |
| 12 | **Duration** | Start and end timestamp of the detected segment. |
| 13 | **Censor Intensity** | Per-segment mute level from 0% to 150%. |
| 14 | **Export Button** | Applies censorship or silence removal and saves the processed file. |
| 15 | **Timeline Export** | Exports all detected segments to FCPXML/XML file. |

</div>

---

## Modes

### Censorship

Detects swear words using AI and automatically mutes or replaces them with a sound.

![Censorship Settings](images/screenshots/censorship_settings.png)

<div align="center">

| Setting | Description |
|---|---|
| **Censor Type** | Silence = mutes the word with the silence. Beep = replaces it with a tone. |
| **Confidence** | How certain the model must be before flagging a word. Higher = better accuracy, but may miss. Lower = catches more but can flag clean speech. |
| **Fuzzy** | How strictly a word must match the profanity list. Lower values also catch intentional misspellings and transliterations. |
| **Global Mute %** | How much of each flagged word to mute. 100% = fully muted. 0% = untouched. |
| **Export Dir** | Where the processed video file is saved after export. |
| **Reset** | Resets the mode settings to default in the application. |
| **Custom Dictionaries** | Customize the app's built-in dictionaries. Remove or add words as needed. |
| **Automute / Markers** | Export detected segments as an automute timeline, or markers - as FCPXML or XML. Compatible with Final Cut Pro, DaVinci Resolve, and Adobe Premiere. |

</div>

---

### Silence Removal

Detects quiet pauses in speech using Voice Activity Detection (VAD) and marks them as segments you can remove.

![Silence Removal Settings](images/screenshots/silence_removal_settings.png)

<div align="center">

| Setting | Description |
|---|---|
| **VAD Threshold** | Sensitivity of silence detection. Higher = stricter. Lower = more aggressive. |
| **Min Silence Dur** | How long a pause must last before it's flagged. |
| **Speech Pad** | A small buffer added around each speech segment. |
| **Fix click sound** | Adds a short crossfade at each cut point to eliminate the audible click that can occur when silence is removed abruptly. |
| **Export Dir** | Where the processed video file is saved after export. |
| **Reset** | Resets the mode settings to default in the application. |
| **Autocut / Markers** | Export detected segments as an autocut timeline, or markers - as FCPXML or XML. Compatible with Final Cut Pro, DaVinci Resolve, and Adobe Premiere. |

</div>

---

### Subtitles

Transcribes your video using AI and generates an SRT/VTT/FCPXML subtitle file.

![Subtitles Settings](images/screenshots/subtitles_settings.png)

![Subtitles Settings 2](images/screenshots/subtitles_settings2.png)

<div align="center">

| Setting | Description |
|---|---|
| **Chars per Line** | Maximum characters in a single subtitle line. |
| **Lines per Sub** | 1 or 2 lines per subtitle block. |
| **Split at sentences** | Automatically starts a new subtitle at `.` `!` `?` - works regardless of subtitle length. Recommended ON. |
| **Scene Detection** | Detects hard cuts in the video and forces a subtitle break at each scene change. |
| **One Word per subtitle** | Shows one word at a time. |
| **Remove Periods** | Strips sentence-ending periods from subtitle text. |
| **Speaker Dash** | Prepends `- ` to every subtitle line. |
| **Text Case** | Keep original case, convert to ALL CAPS, or all lowercase. |
| **Max Duration** | Maximum display time for a single subtitle block. |
| **Min Pause** | Minimum gap between consecutive subtitle blocks. |
| **Linger** | How long the subtitle stays on screen after the speech ends. Increase to make subtitles overlap into the next - raise it enough and subtitles will display without gaps. |
| **Translation** | Auto-translate subtitles to another language via Google Translate (requires internet). |
| **Formats** | Export as SRT (universal), VTT (web), or FCPXML (Final Cut Pro & Davinci Resolve). |
| **FCPXML Settings** | Frame rate, minimum gap between captions, and style settings for Final Cut Pro & Davinci Resolve. |
| **Export Dir** | Where the processed video file is saved after export. |
| **Reset** | Resets the mode settings to default in the application. |

</div>

---

## Engines

### Whisper

A neural speech recognition model that runs entirely on your Mac - no data ever leaves your computer. Used in Censorship and Subtitles modes for high-accuracy transcription across many languages.

Available in four sizes. Larger = slower but more accurate. These models use MLX, which is compatible with Apple Silicon.

```
tiny   ~2 GB RAM   ·  Fastest   ·  Low accuracy
base   ~3 GB RAM   ·  Fast      ·  Average accuracy
small  ~6 GB RAM   ·  Medium    ·  Medium accuracy
medium ~10 GB RAM  ·  Slow      ·  Great accuracy
```

**Tip:** Use **small** or **medium** for the best balance. Use tiny/base when speed matters more.

---

### Vosk

Another offline speech recognition engine. Used only in Censorship mode. Their models do not require a significant amount of CPU/RAM and are more accurate than Whisper with some languages.

Small Vosk models (~50–150 MB) can be installed inside the app. Large models (400 MB–2 GB) must be downloaded manually:

```
1.  Go to  alphacephei.com/vosk/models
2.  Download the zip for your language
    (e.g. vosk-model-ru-0.42 for large Russian model)
3.  Unzip - you get a folder  vosk-model-*
4.  Censorship → Settings →
    Models → Vosk → Custom Path → 🔍
    Select that folder
5.  The model is now active
```

**Tip:** The folder name must start with `vosk-model`.
