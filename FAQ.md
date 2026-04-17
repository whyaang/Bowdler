<div align="center">

![FAQ](images/faq.png)

</div>

---

## 💻 System Requirements

**What Mac does Bowdler require?**

Bowdler requires a Mac with Apple Silicon - M1 or later. It does not run on Intel Macs.

**What macOS version is required?**

macOS 13.3 Ventura or later.

**How much disk space does Bowdler need?**

The app itself is about 42 MB. The libraries required for work take up 1.23 GB. AI models are downloaded separately and stored in the Application Support folder (`/Users/your_username/Library/Application Support/com.whyang.bowdler/models`). Model sizes vary depending on which ones you download.

**Does Bowdler need an internet connection?**

Only for activation, downloading models, subtitle translation, and updates. All processing happens entirely on your Mac without third-party APIs.

---

## 🛒 Purchase & License

**Where can I buy Bowdler?**

Bowdler is sold on Gumroad. Visit the [product page](https://whyaang.gumroad.com/l/bowdler) and complete the purchase. You will receive a license key by email immediately after payment.

**How much does Bowdler cost?**

$49 - one-time payment, lifetime license. No subscription, no media limits, no recurring fees. All future updates are included.

**Can I get a refund?**

Refunds are handled through Gumroad within 30 days of purchase if the app does not work on your machine and the issue cannot be resolved.

**How many computers can I use the license on?**

One license covers one device. You can transfer the license to a different Mac **(no more than once every 3 months)** by contacting me at **[whyaang@gmail.com](mailto:whyaang@gmail.com)**.

---

## 🔑 Activation

**How do I activate Bowdler?**

On the first launch, Bowdler will show an activation screen. Paste your license key from the purchase email and click Activate. An internet connection is required for this step.

**I lost my license key. How do I find it?**

Check your email for a message from Gumroad. You can also log into Gumroad with the email you used to purchase and find your key in your library. If this does not help, contact me at **[whyaang@gmail.com](mailto:whyaang@gmail.com)**.

**Activation says "Invalid key". What do I do?**

Make sure you copied the full key without extra spaces or symbols. If the problem persists, contact me at **[whyaang@gmail.com](mailto:whyaang@gmail.com)**.

**Why does the app ask for my Keychain password?**

Bowdler stores your license key in the macOS Keychain and reads it on every launch. Enter your Mac login password and click Always Allow - the app will not ask again.

---

## ⚙️ Troubleshooting

**macOS says the app is damaged or can't be opened.**

This is a macOS Gatekeeper warning that appears for apps distributed outside the App Store. Open Terminal and run:

```
xattr -cr /Applications/Bowdler.app
```

Then try launching again.

**The app says "Python runtime not found".**

Try reinstalling the app. Make sure you copied Bowdler.app to your Applications folder and launched it from there, not from the DMG.

**Processing starts but immediately fails.**

Check that the AI model is fully downloaded. Go to Settings → Models and verify the model shows as installed, or try a different one.

**Bowdler is slow on my Mac.**

Use a smaller model (Whisper tiny or base) or try the Vosk engine. Close other memory-heavy applications while processing.

**I found a bug. How do I report it?**

Click **Help** in the macOS menu bar, select **Report a Bug**, and send a description of the issue along with your macOS version and Mac model.

---

## 🤖 Models

**Which model should I download first?**

Start with **Whisper small**. It gives a good balance of speed and accuracy for most use cases.

**What models does Bowdler use?**

Bowdler uses Whisper for transcription (used in Transcript Edit, Subtitles, Censorship, and Silence Removal), and a separate model for bad take detection. All models run locally on your Mac.

**Can I use Bowdler while a model is downloading?**

This is not recommended. Wait for the download to complete before processing a video.

**What languages does Bowdler support?**

Bowdler supports 32 languages across all modes: English, Chinese, Hindi, Spanish, Arabic, Bengali, Portuguese, Indonesian, Russian, Japanese, Turkish, Vietnamese, French, Korean, German, Urdu, Italian, Thai, Polish, Ukrainian, Dutch, Romanian, Greek, Hungarian, Kazakh, Serbian, Swedish, Czech, Hebrew, Danish, Finnish, and Norwegian.

---

## 🎬 Processing

**What file formats are supported?**

Video: MP4, MOV. Audio: MP3, WAV, AAC.

**What export formats are available?**

Bowdler can export processed video directly as MP4 or MOV in the original codec - no re-encoding, no quality loss, up to 4K. For timeline-based workflows, it exports FCPXML (Final Cut Pro), XML (DaVinci Resolve, Adobe Premiere), SRT, and VTT.

**Can I process multiple files at once?**

Yes. Bowdler has built-in batch processing - drag or select multiple files and they will be processed one by one with the same settings.

**The detection missed some words or detected wrong words. What can I do?**

Try lowering the Confidence threshold in Settings. If the words you need are not in the dictionary, add them manually in Censorship settings. If accuracy is still low, try a different or larger model.

**Can I manually add segments the model missed?**

Yes. On the Review screen, use the Custom Range button to manually define a time range, or select a segment directly on the timeline.

---

## ✏️ Transcript Edit

**What is Transcript Edit?**

Transcript Edit is Bowdler's main editing mode. It transcribes your video and shows the result as an editable document. You can select words or sentences and cut them, mute profanity, remove filler words, delete bad takes, and generate subtitles - all from a single view without switching modes.

**How does multi-speaker detection work?**

Bowdler detects different speakers in your video and highlights each one in a different color in the transcript. Subtitles can be generated with per-speaker color tracks.

**Can I remove silence in Transcript Edit?**

Yes. Silence gaps are shown inline in the transcript and can be removed directly without switching to Silence Removal mode.

**Can I remove filler words in Transcript Edit?**

Yes. Filler words are detected and highlighted. You can remove them individually or in bulk.

---

## 🔇 Censorship Mode

**What censor types are available?**

Silence (replaces the word with silence), Beep (replaces it with a tone), and Custom audio files.

**What is Fuzzy matching?**

Fuzzy matching catches intentional misspellings and alternate spellings of profanity. Lower values catch more variants.

**Can I edit the built-in word list?**

Yes. Go to Settings → Custom Dictionaries, select your language, and edit the list. You can add or remove any words. To restore the default list, delete the file by clicking the cross.

---

## ✂️ Silence Removal

**How does silence detection work?**

Bowdler uses Silero VAD, an AI voice activity detection model, to identify pauses in speech. Detected silences appear as segments on the timeline that you can review before removing.

**What do VAD Threshold and Speech Pad do?**

VAD Threshold controls detection sensitivity. Speech Pad adds a small buffer around speech so cuts don't feel abrupt.

**Can I keep some silences and remove others?**

Yes. On the Review screen you can toggle individual segments on or off before exporting.

---

## 💬 Subtitles

**What subtitle formats does Bowdler export?**

SRT (universal), VTT (web), and FCPXML (Final Cut Pro).

**Can Bowdler translate subtitles?**

Yes. Enable Translation in Settings and select a target language. Translation uses Google Translate and requires an internet connection. 32 languages supported.

**Can I edit subtitles before exporting?**

Yes. After transcription, you can edit subtitle text, adjust timing, and customize appearance directly in the app. Changes are reflected on the video preview in real time.

**What is the One Word mode?**

One Word mode shows a single word at a time, TikTok-style.

**Can I assign different subtitle colors per speaker?**

Yes. When multi-speaker detection is enabled in Transcript Edit, each speaker gets a unique subtitle color track.

---

## 🔄 Updates

**How do I update Bowdler?**

Bowdler checks for updates automatically on launch. If a new version is available, a notification will appear. You can also check manually in Settings → Bowdler → Check for Updates.

**Do I need to re-enter my license key after updating?**

No. Your license is stored securely in the macOS Keychain and carries over automatically.

---

## 🔒 Privacy

**Does Bowdler send my data anywhere?**

No. All processing runs locally on your Mac. The only exceptions are subtitle translation (Google Translate) and license activation (Gumroad). No video, audio, or transcript data ever leaves your device.

**What data does Bowdler collect?**

License validation requires an internet connection to verify your key with Gumroad. **No usage data, analytics, or crash reports are collected.**
