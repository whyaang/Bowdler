<div align="center">

![FAQ](images/faq.png)

</div>

<div align="center">
  <h3>
    <a href="README.md">README</a> · <a>FAQ</a> · <a href="DOCS.md">DOCS</a>
  </h3>
  <p>
    <a>🇺🇸 English</a> · <a href="languages/Chinese/FAQ.md">🇨🇳 中文</a> · <a href="languages/Spanish/FAQ.md">🇪🇸 Español</a> · <a href="languages/Arabic/FAQ.md">🇸🇦 العربية</a> · <a href="languages/Portuguese/FAQ.md">🇧🇷 Português</a> · <a href="languages/Russian/FAQ.md">🇷🇺 Русский</a>
  </p>
</div>

---

## 💻 System Requirements

**What Mac does Bowdler require?**

Bowdler requires a Mac with Apple Silicon - M1 or later. It does not run on Intel Macs.

**What macOS version is required?**

macOS 13.3 Ventura or later.

**How much disk space does Bowdler need?**

The app itself is about 42 MB. The libraries required for work take up 1.23GB. AI models are downloaded separately and stored in Application Support folder (/Users/your_username/Library/Application Support/com.whyang.bowdler/models). The sizes of the models may vary.

**Does Bowdler need an internet connection?**

Only for activation, downloading models and update. All processing happens entirely on your Maс without third-party APIs.

---

## 🛒 Purchase & License

**Where can I buy Bowdler?**

Bowdler is sold on Gumroad. Visit the [product page](https://whyaang.gumroad.com/l/bowdler) and complete the purchase. You will receive a license key by email immediately after payment.

**Can I get a refund?**

Refunds are handled through Gumroad within 30 days of purchase if the app does not work on your machine and the issue cannot be resolved.

**How many computers can I use the license on?**

One license covers only 1 device with MacOS. You can change the device to which the license key is linked **(no more than once every 3 months)** by contacting me - **[whyaang@gmail.com](mailto:whyaang@gmail.com)**.

---

## 🔑 Activation

**How do I activate Bowdler?**

On the first launch, Bowdler will show an activation screen. Paste your license key from the purchase email and click Activate. An internet connection is required for this step.

**I lost my license key. How do I find it?**

Check your email for a message from Gumroad. You can also log into Gumroad with the email you used to purchase and find your key in your library. If this does not help, please contact me - **[whyaang@gmail.com](mailto:whyaang@gmail.com)**.

**Activation says "Invalid key". What do I do?**

Make sure you copied the full key without extra spaces or symbols. If the problem persists, contact me - **[whyaang@gmail.com](mailto:whyaang@gmail.com)**.

**Why does application ask for my Keychain password?**

Bowdler stores your license key in the macOS Keychain and reads it on every launch. Enter your Mac login password and click Always Allow - this way the app will not ask again.

---

## ⚙️ Troubleshooting

**macOS says the app is damaged or can't be opened.**

This is a macOS Gatekeeper warning that appears for apps distributed outside the App Store. Open Terminal and run `xattr -cr /Applications/Bowdler.app` Then try launching again.

**The app says "Python runtime not found".**

Try reinstalling the app. Make sure you copied Bowdler.app to your Applications folder and launched it from there, not from the DMG.

**Processing starts but immediately fails.**

Check that the AI model is fully downloaded. Go to Settings → Models and verify the model shows as installed or try another one.

**Bowdler is slow on my Mac.**

Use a smaller model (Whisper tiny or base) or try Vosk Engine. Close other heavy applications that using RAM while processing.

**I found a bug. How do I report it?**

Click **Help** button located at the top of the screen in macOS, select **Report a Bug** and send a description of the issue, your macOS version and the Mac model you are using.

---

## 🤖 Models

**Which model should I download first?**

Start with **Whisper small**. It gives a good balance of speed and accuracy for most use cases.

**Can I use Bowdler while a model is downloading?**

This is not recommended. Wait for the download to complete before processing a video.

**What languages does Bowdler support?**

Bowdler supports 32 languages: English, Chinese, Hindi, Spanish, Arabic, Bengali, Portuguese, Indonesian, Russian, Japanese, Turkish, Vietnamese, French, Korean, German, Urdu, Italian, Thai, Polish, Ukrainian, Dutch, Romanian, Greek, Hungarian, Kazakh, Serbian, Swedish, Czech, Hebrew, Danish, Finnish and Norwegian.

---

## 🎬 Processing

**What file formats are supported?**

MP4, MOV, MP3, and WAV.

**Can I process multiple files at once?**

The application has a built-in Batch processing function - simply transfer or select multiple files at once. They will be processed one by one.

**The detection missed some words/detected wrong words. What can I do?**

Try lowering the Confidence threshold in Settings. There may be cases where the words you need aren't in the dictionary. You can add them manually in the Censorship settings. If this is not the case, then try other models.

**Can I manually add segments the model missed?**

Yes. On the Review screen, use the Custom Range button to manually define a time range or manually select a segment on the timeline.

---

## 🔇 Censorship Mode

**What censor types are available?**

Silence (replaces the word with silence), Beep (replaces it with a tone) and Custom audio-files.

**What is Fuzzy matching?**

Fuzzy matching catches intentional misspellings and alternate spellings of profanity. Lower values catch more variants.

**Can I edit the built-in word list?**

Yes. Go to Settings → Custom Dictionaries, select your language, and edit the list in TextEdit. You can add or remove any words. If you want to return it to how it was, delete the file by clicking the cross.

---

## ✂️ Silence Removal

**How does silence detection work?**

Bowdler uses Silero VAD, an AI voice activity detection model, to identify pauses in speech. Detected silences are shown as segments on the timeline that you can review and remove.

**What do VAD Threshold and Speech Pad do?**

VAD Threshold controls how sensitive detection is. Speech Pad adds a small buffer around speech so cuts don't feel abrupt.

**Can I keep some silences and remove others?**

Yes. On the Review screen you can toggle individual segments on or off before exporting.

---

## 💬 Subtitles

**What subtitle formats does Bowdler export?**

SRT (universal), VTT (web), and FCPXML (Final Cut Pro).

**Can Bowdler translate subtitles?**

Yes. Enable Translation in Settings and select a target language. Translation uses Google Translate and requires an internet connection.

**What is the One Word mode?**

One Word mode shows a single word at a time, TikTok-style.

---

## 🎞️ Final Cut Pro Integration

**How do I export markers to Final Cut Pro?**

On the Review screen, click Export to FCP. This saves an FCPXML file. In Final Cut Pro, go to File → Import → XML and select the file.

**FCP says clips are overlapping. What do I do?**

In Subtitles → Settings → FCPXML Settings, increase the Minimum Gap Between Captions value and re-export.

---

## 🔄 Updates

**How do I update Bowdler?**

Bowdler checks for updates automatically on launch. If a new version is available, a notification will appear. You can also check manually in Settings → Bowdler → Check for Updates.

**Do I need to re-enter my license key after updating?**

No. Your license is stored securely on your Mac using Keychain and carries over automatically.

---

## 🔒 Privacy

**Does Bowdler send my data anywhere?**

No. All processing is done locally (except for subtitle translation, which uses Google Translate) on your Mac. No video, audio, or transcript data ever leaves your device.

**What data does Bowdler collect?**

License validation requires an internet connection to verify your key with Gumroad. **No usage data or analytics are collected.**
