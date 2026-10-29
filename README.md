# Aksharadhara (అక్షరధార)

[![license](https://img.shields.io/badge/license-GPL--3.0-blue)](./LICENSE)
[![live](https://img.shields.io/badge/live-aksharadhara.netlify.app-0a4a85)](https://aksharadhara.netlify.app/)
[![PWA](https://img.shields.io/badge/PWA-installable-5a0fc8)](https://aksharadhara.netlify.app/)
[![XERJ Corpus Hub contributor](https://hub.xerj.org/contributors/sandeepmiriyala03/badge.svg)](https://hub.xerj.org/contributors/sandeepmiriyala03)

**Sanskrit / Telugu OCR & Mantra Manager.** Turn photos of Telugu, Sanskrit, Hindi and English text into editable text, mark Vedic pitch (swara) on mantras, and keep your collection in the browser.

🌐 **Live:** https://aksharadhara.netlify.app/

Runs in your browser as an installable app (PWA). Images are read on your device; nothing is uploaded.

---

## Features

| | Feature | What it does |
|---|---|---|
| 📷 | **Image to text (OCR)** | Reads Telugu, Sanskrit, Hindi and English from an image using [Tesseract.js](https://github.com/naptha/tesseract.js) |
| 🎵 | **Pitch marking** | Marks a syllable as high (**స్వరితం**, a vertical line above) or low (**అనుదాత్తం**, a horizontal line below) |
| 💾 | **Saved in your browser** | Mantras and their pitch marks stay in local storage between visits |
| 📝 | **Mantra manager** | Save, view, edit and delete mantras |
| ⬇️ | **Export** | "Download" saves your whole collection as JSON in `all_mantras.txt` |
| ✍️ | **Handwriting (experimental)** | Telugu handwriting OCR with TensorFlow.js models (`HandWrite.html`) |
| ♿ | **Accessibility** | Accessibility settings by [YuktAI](https://www.npmjs.com/package/@yuktishaalaa/yuktai) |

## Pages

| Page | File |
|---|---|
| Home | `index.html` |
| Mantra OCR + pitch marking | `aksharadhara.html` |
| Sanskrit OCR | `sanskrit.html` |
| Telugu OCR | `Telugu.html` |
| Hindi OCR | `Hindi.html` |
| English OCR | `english.html` |
| Shukla Yajurveda | `ShuklaYajurveda.html` |
| Krishna Yajurveda (Shruti Sankalanam) | `shruti-sankalanam.html` |
| Telugu handwriting OCR | `HandWrite.html` |

## How to use

1. Open **Mantra OCR** (`aksharadhara.html`).
2. Click **Upload Image** and choose a photo of the mantra.
3. Click **Start OCR**. The text appears in the box below.
4. Fix any mistakes. Select a syllable and click **High Pitch** or **Low Pitch**.
5. Add a title and description, then click **Save New Mantra**.
6. Your saved mantras appear under **View & Edit Mantras**. Use **Edit Mantra** to change one, or delete it.
7. Click **Download** to keep a copy of everything (`all_mantras.txt`).

> Clearing your browser data deletes saved mantras. Download a copy first.

## Run locally

```bash
git clone https://github.com/sandeepmiriyala03/Aksharadhara.git
cd Aksharadhara
npm install
npm start          # serves the folder, then open the address it prints
```

Open the pages through a local server (not as a `file://` path), so the app and OCR can load.

## Built with

HTML, CSS and JavaScript · [Tesseract.js](https://github.com/naptha/tesseract.js) (open-source OCR) · TensorFlow.js · Google Fonts (`Noto Sans Telugu`, `Roboto`) · [YuktAI](https://www.npmjs.com/package/@yuktishaalaa/yuktai) · Netlify

## Credits

The text recognition comes from the open-source Tesseract.js project and its language data. Aksharadhara adds the Indic pages, pitch marking and mantra management on top.

## License

[GPL-3.0](./LICENSE) © Sandeep Miriyala. You may use, change and share this project; changed versions you share must stay open under GPL-3.0.

Third-party parts keep their own licences: Tesseract.js and TensorFlow.js (Apache-2.0), YuktAI (GPL-3.0), Google Fonts (SIL Open Font License).
