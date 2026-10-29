# 🌐 PolyGlot Studio - Universal Language Translator

An elegant, real-time language translation web application with support for **Google Translate**, **Microsoft Azure Translator**, **MyMemory API**, and **LibreTranslate**. Features native browser **Text-to-Speech (TTS)**, **Voice Dictation (Speech-to-Text)**, **One-click Copy**, **Translation History**, and **Dark/Light Theme**.

---

## 🚀 Quick Start

You can run PolyGlot Studio in **two easy ways**:

### Option 1: Instant Browser Launch (Zero-Installation)
No terminal or node installation needed!
1. Navigate to the project directory:
   ```
   C:\Users\SIDDU\.gemini\antigravity\scratch\language-translator\
   ```
2. Double-click **`index.html`** or right-click and open it in Google Chrome, Microsoft Edge, Firefox, or Brave.
3. Start typing or speaking to translate immediately!

### Option 2: Run with Local Node.js Server
If you prefer running via a local web server with the optional proxy backend:
1. Open PowerShell or Terminal in the project directory:
   ```powershell
   cd "C:\Users\SIDDU\.gemini\antigravity\scratch\language-translator"
   ```
2. Run the server (zero external dependencies required):
   ```powershell
   node server.js
   ```
3. Open your browser and visit: **`http://localhost:3000`**

---

## ✨ Features

| Feature | Description |
| :--- | :--- |
| **Multi-Provider Engine** | Default zero-config Google Translate (GTX) with automatic fallback to MyMemory API. Also supports official Google Cloud & Microsoft Azure Translator keys. |
| **50+ Languages** | Comprehensive support for world languages, regional Indian languages (Hindi, Bengali, Telugu, Tamil, Marathi, Gujarati, Kannada, Malayalam, Punjabi, Urdu), European, East Asian, and Middle Eastern languages. |
| **Auto-Detect Language** | Automatically identifies the source language as you type. |
| **Real-Time Translation** | Debounced auto-translation triggers smoothly as you type, or press the manual "Translate" button. |
| **Text-to-Speech (TTS)** | Listen to natural pronunciation for both the source text and translated text with customizable speech rate. |
| **Voice Input (Speech-to-Text)** | Click the microphone icon to dictate your text using your voice. |
| **Language Swap** | Easily invert source and target languages and text with a single click or shortcut (`Ctrl + Shift + S`). |
| **Copy & Download** | One-click copy buttons with toast notifications, plus a button to download translations as `.txt` files. |
| **Translation History** | Automatically saves your recent translations locally. Click any history entry to reload it, or copy/delete. |
| **Dark & Light Mode** | Gorgeous themes that respect system preference with manual toggle. |
| **Responsive Design** | Optimized for desktop, tablets, and mobile devices. |

---

## ⌨️ Keyboard Shortcuts

- **`Ctrl + Enter`** (or `Cmd + Enter`): Trigger instant translation
- **`Ctrl + Shift + S`**: Swap source and target languages
- **`Escape`**: Close modals and the history drawer

---

## ⚙️ Translation API Configuration

Click the **API Settings** button (⚙️) or the **Provider Pill** in the top navigation bar to configure providers:

1. **Google Translate (Free & Instant)** *(Default)*:
   - Zero setup required. Uses Google's web translation client.
2. **MyMemory Translation API**:
   - Free collaborative translation memory API. Enabled automatically as a fallback.
3. **Google Cloud Translation API (Official)**:
   - Enter your Google Cloud API key (`AIzaSy...`).
   - Requests are routed to `https://translation.googleapis.com/language/translate/v2`.
4. **Microsoft Azure Cognitive Translator**:
   - Enter your 32-character Azure Translator Key and Region (e.g. `global` or `eastus`).
   - Uses the Azure Cognitive Services Translator API v3.0.
5. **LibreTranslate**:
   - Point to any public or self-hosted LibreTranslate instance URL.

---

## 📂 Project Structure

```
language-translator/
├── index.html        # Main user interface & accessible semantic markup
├── style.css         # Modern styling, responsive grid, animations & theme variables
├── app.js            # Main translation engine, TTS, STT, history & UI event handlers
├── languages.js      # 50+ Language definitions, ISO codes, flags & TTS voice codes
├── server.js         # Optional native Node.js HTTP server & API proxy
├── package.json      # NPM scripts and project metadata
└── README.md         # Comprehensive documentation & guide
```

---

## 🛡️ Privacy & Storage
- Translation history and API settings are stored exclusively in your local browser storage (`localStorage`).
- Your API keys are never transmitted to any third-party server other than the chosen translation provider.
