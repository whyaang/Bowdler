<div align="center">

![FAQ](images/faq.png)

</div>

<div align="center">
  <h3>
    <a href="README.md">README</a> · <a>FAQ</a> · <a href="DOCS.md">DOCS</a>
  </h3>
  <p>
    <a href="../../FAQ.md">🇺🇸 English</a> · <a>🇨🇳 中文</a> · <a href="../Spanish/FAQ.md">🇪🇸 Español</a> · <a href="../Arabic/FAQ.md">🇸🇦 العربية</a> · <a href="../Portuguese/FAQ.md">🇧🇷 Português</a> · <a href="../Russian/FAQ.md">🇷🇺 Русский</a>
  </p>
</div>

---

## 💻 系统要求

**Bowdler 需要什么 Mac？**

Bowdler 仅支持搭载 Apple Silicon 的 Mac——M1 及更新版本。不支持 Intel Mac。

**需要哪个 macOS 版本？**

macOS 13.3 Ventura 或更高版本。

**Bowdler 需要多少磁盘空间？**

应用本身约 42 MB。运行所需的库占用 1.23 GB。AI 模型单独下载，存储在 Application Support 文件夹中（/Users/your_username/Library/Application Support/com.whyang.bowdler/models）。模型大小因型号而异。

**Bowdler 需要互联网连接吗？**

仅在激活、下载模型和更新时需要。所有处理均在您的 Mac 本地完成，不使用任何第三方 API。

---

## 🛒 购买与许可证

**在哪里购买 Bowdler？**

Bowdler 在 Gumroad 上销售。访问[产品页面](https://whyaang.gumroad.com/l/bowdler)完成购买。付款后，许可证密钥将立即发送到您的邮箱。

**可以退款吗？**

如果应用在您的 Mac 上无法正常运行且问题无法解决，可在购买后 30 天内通过 Gumroad 申请退款。

**一个许可证可以在几台电脑上使用？**

一个许可证仅限一台 macOS 设备。如需更换绑定设备，请联系 **[whyaang@gmail.com](mailto:whyaang@gmail.com)**（**每 3 个月不超过一次**）。

---

## 🔑 激活

**如何激活 Bowdler？**

首次启动时，Bowdler 将显示激活界面。粘贴购买邮件中的许可证密钥，然后点击 Activate。此步骤需要互联网连接。

**我丢失了许可证密钥，怎么找回？**

请检查来自 Gumroad 的邮件。您也可以使用购买时的邮箱登录 Gumroad，在库中找到密钥。如仍有问题，请联系 **[whyaang@gmail.com](mailto:whyaang@gmail.com)**。

**激活显示"Invalid key"，怎么办？**

请确认已完整复制密钥，没有多余的空格或符号。如问题仍然存在，请联系 **[whyaang@gmail.com](mailto:whyaang@gmail.com)**。

**为什么应用请求访问钥匙串密码？**

Bowdler 将许可证密钥安全存储在 macOS 钥匙串中，并在每次启动时读取。输入 Mac 登录密码并点击**始终允许**，之后将不再提示。

---

## ⚙️ 故障排除

**macOS 提示应用已损坏或无法打开。**

这是 macOS Gatekeeper 对 App Store 以外分发的应用显示的警告。打开终端并运行：

`xattr -cr /Applications/Bowdler.app`

然后再次尝试启动应用。

**应用提示"Python runtime not found"。**

请重新安装应用。确保将 Bowdler.app 复制到应用程序文件夹，并从那里启动，而不是直接从 DMG 启动。

**处理开始后立即失败。**

请检查 AI 模型是否已完整下载。前往 Settings → Models 确认模型已安装，或尝试其他模型。

**Bowdler 运行很慢。**

请使用更小的模型（Whisper tiny 或 base），或尝试 Vosk 引擎。处理时请关闭其他占用内存较多的应用程序。

**我发现了一个 bug，如何反馈？**

点击 macOS 顶部菜单栏中的 **Help** 按钮，选择 **Report a Bug**，描述问题、macOS 版本和 Mac 型号。

---

## 🤖 模型

**应该先下载哪个模型？**

建议从 **Whisper small** 开始，它在速度和准确性之间取得了良好平衡。

**下载模型时可以使用 Bowdler 吗？**

不建议。请等待下载完成后再处理视频。

**Bowdler 支持哪些语言？**

Bowdler 支持 32 种语言：英语、中文、印地语、西班牙语、阿拉伯语、孟加拉语、葡萄牙语、印度尼西亚语、俄语、日语、土耳其语、越南语、法语、韩语、德语、乌尔都语、意大利语、泰语、波兰语、乌克兰语、荷兰语、罗马尼亚语、希腊语、匈牙利语、哈萨克语、塞尔维亚语、瑞典语、捷克语、希伯来语、丹麦语、芬兰语和挪威语。

---

## 🎬 处理

**支持哪些文件格式？**

MP4、MOV、MP3 和 WAV。

**可以同时处理多个文件吗？**

应用内置批量处理功能——只需同时拖入或选择多个文件，它们将依次处理。

**模型遗漏了某些词或误检了。怎么办？**

尝试在设置中降低 Confidence 阈值。如果所需词汇不在词典中，可以在审查模式设置中手动添加。如仍无效，请尝试其他模型。

**可以手动添加模型遗漏的片段吗？**

可以。在 Review 界面使用 Custom Range 按钮手动定义时间范围，或直接在时间轴上选择片段。

---

## 🔇 审查模式

**有哪些审查类型？**

静音（用静默替换词语）、哔声（用音调替换）和自定义音频文件。

**什么是模糊匹配（Fuzzy）？**

模糊匹配可识别故意的错别字和不雅词语的变体写法。数值越低，匹配范围越广。

**可以编辑内置词汇表吗？**

可以。前往 Settings → Custom Dictionaries，选择语言，在 TextEdit 中编辑列表。可以添加或删除词语。若想恢复原始词汇表，点击叉号删除文件即可。

---

## ✂️ 去除静音

**静音检测是如何工作的？**

Bowdler 使用 Silero VAD（AI 语音活动检测模型）识别语音中的停顿。检测到的静音片段显示在时间轴上，您可以审查并删除。

**VAD Threshold 和 Speech Pad 是什么？**

VAD Threshold 控制检测灵敏度。Speech Pad 在语音片段周围添加缓冲，使剪切听起来更自然。

**可以保留部分静音而删除其他吗？**

可以。在 Review 界面，可以在导出前单独开启或关闭各个片段。

---

## 💬 字幕

**Bowdler 支持哪些字幕格式？**

SRT（通用）、VTT（网页）和 FCPXML（Final Cut Pro）。

**Bowdler 可以翻译字幕吗？**

可以。在设置中启用 Translation 并选择目标语言。翻译使用 Google 翻译，需要互联网连接。

**One Word 模式是什么？**

One Word 模式每次显示一个单词，类似 TikTok 风格。

---

## 🎞️ Final Cut Pro 集成

**如何将标记导出到 Final Cut Pro？**

在 Review 界面点击 Export to FCP，保存 FCPXML 文件。在 Final Cut Pro 中选择 File → Import → XML，然后选择该文件。

**FCP 提示片段重叠，怎么办？**

在 Subtitles → Settings → FCPXML Settings 中增大 Minimum Gap Between Captions 的值，然后重新导出。

---

## 🔄 更新

**如何更新 Bowdler？**

Bowdler 启动时会自动检查更新。如有新版本，将显示通知。也可在 Settings → Bowdler → Check for Updates 手动检查。

**更新后需要重新输入许可证密钥吗？**

不需要。许可证安全存储在 Mac 的钥匙串中，更新后自动保留。

---

## 🔒 隐私

**Bowdler 会发送我的数据吗？**

不会。所有处理均在您的 Mac 本地完成（字幕翻译除外，使用 Google 翻译）。视频、音频或文字记录均不会离开您的设备。

**Bowdler 收集哪些数据？**

许可证验证需要联网向 Gumroad 确认密钥。**不收集任何使用数据或分析信息。**
