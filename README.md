# 🎙️ Echo Live Transcribe

A **browser-based speech-to-text transcriber** with **real-time phonetic (IPA) conversion**. Runs entirely in-browser using the Web Speech API. Chrome/Chromium required.

![License](https://img.shields.io/badge/license-MIT-blue) ![Status](https://img.shields.io/badge/status-active-green)

## ✨ Features

- 🎤 **Live microphone input** with real-time transcription
- 🔤 **Dual transcripts**: Literal English + IPA phonetic conversion
- 📊 **Live statistics**: Word count, character count, duration tracking
- 💾 **Multiple export formats**: TXT, JSON, CSV
- 🎨 **Dark theme UI** with gradient accents
- ⏸️ **Pause/resume** functionality for interrupted speech
- 📱 **Responsive design** (desktop & mobile-friendly)
- 🔒 **Privacy-first**: All processing happens in-browser; nothing is sent to servers

## 🚀 Quick Start

1. **Open the app:** https://skinkmonk.github.io/Echo-Live-Transcribe-
2. **Allow microphone access** when prompted by your browser
3. **Click "Start Listening"** and speak clearly
4. **Watch both transcripts update** in real-time
5. **Export** when done (TXT, JSON, or CSV)

## 📋 Supported Browsers

- ✅ **Google Chrome** (recommended)
- ✅ **Chromium-based browsers** (Edge, Brave, Opera, Vivaldi)
- ❌ Firefox, Safari (Web Speech API not available)

## 🔄 How Phonetic Conversion Works

The app converts English text to **International Phonetic Alphabet (IPA)** notation:

| English | Phonetic |
|---------|----------|
| the | θə |
| shook | ʃʊk |
| chair | tʃɛɹ |
| think | θɪŋk |
| choose | tʃuːz |

Examples:
- "hello" → "hɛloʊ"
- "phonetic" → "foʊnɛtɪk"
- "transcribe" → "tɹænskriːb"

## 📥 Export Options

### TXT Export
Plain text with both transcripts and metadata. Copy-paste ready.

### JSON Export
Structured data with metadata:
```json
{
  "metadata": {
    "generated": "2026-09-07T10:30:00.000Z",
    "duration": "00:45",
    "wordCount": "150",
    "characterCount": "1250"
  },
  "transcripts": {
    "literal": "hello world",
    "phonetic": "hɛloʊ wɜld"
  }
}
```

### CSV Export
Spreadsheet-friendly format with word-by-word phonetic mapping.

## 🛠️ Installation & Development

### Clone the Repository
```bash
git clone https://github.com/skinkmonk/Echo-Live-Transcribe-.git
cd Echo-Live-Transcribe-
```

### Local Development
Simply open `index.html` in Chrome:
```bash
# Option 1: Direct file open
open index.html

# Option 2: Use a local server (recommended)
python3 -m http.server 8000
# Visit: http://localhost:8000
```

### GitHub Pages Setup
This repo is **already configured for GitHub Pages** using the `main` branch.

1. Go to **Settings** → **Pages**
2. Ensure **Source** is set to `Deploy from a branch`
3. Select `main` branch
4. Site is live at: `https://skinkmonk.github.io/Echo-Live-Transcribe-`

## 🔍 Troubleshooting

### "Microphone access denied"
- Check browser permissions for microphone
- Try an incognito/private window
- Ensure your device has a working microphone

### "Web Speech API not supported"
- Use Google Chrome or Chromium-based browser
- Firefox and Safari are not supported by this API

### No text appearing
- Speak clearly and closer to microphone
- Check microphone levels in system settings
- Try reloading the page

### Export not working
- Clear browser cache
- Try a different browser (still Chrome-based)
- Check available disk space

## 🏗️ Architecture

```
index.html (single-file app)
├── HTML structure with semantic sections
├── CSS (dark theme, responsive grid layout)
└── JavaScript
    ├── PhoneticConverter class (IPA mapping engine)
    ├── Speech Recognition API integration
    ├── Real-time transcript update system
    ├── Statistics tracker
    └── Export utilities (TXT/JSON/CSV)
```

## 📈 Tech Stack

- **Frontend**: Vanilla HTML5, CSS3, JavaScript (ES6+)
- **Speech Recognition**: Web Speech API (Chrome)
- **Phonetic Engine**: Custom IPA character mapping
- **Export**: Blob + File Download API
- **Hosting**: GitHub Pages

## 🎓 IPA Reference

### Consonants
| Symbol | Example |
|--------|---------|
| θ | th**i**nk |
| ð | **th**is |
| ʃ | **sh**e |
| ʒ | plea**s**ure |
| tʃ | **ch**eck |
| dʒ | **j**udge |
| ŋ | si**ng** |
| ɹ | **r**ed |

### Vowels
| Symbol | Example |
|--------|---------|
| æ | tr**a**p |
| ɛ | dr**e**ss |
| ɪ | k**i**t |
| ɑ | l**o**t |
| ʌ | str**u**t |
| aɪ | pr**i**ce |
| eɪ | f**a**ce |
| ɔɪ | ch**oi**ce |
| oʊ | g**oa**t |
| aʊ | m**ou**th |

## 🤝 Contributing

Found a bug or have a feature request? [Open an issue](https://github.com/skinkmonk/Echo-Live-Transcribe-/issues)

## 📄 License

MIT License - feel free to use, modify, and distribute.

## 🔗 Resources

- [Web Speech API Docs](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API)
- [IPA Chart](https://www.internationalphoneticassociation.org/IPAcharts/IPA_chart_consonants/chart_consonants_2020.html)
- [GitHub Pages Docs](https://docs.github.com/en/pages)

---

**Made with ❤️ by [skinkmonk](https://github.com/skinkmonk)**

Built for linguistics, speech analysis, and accessibility.
