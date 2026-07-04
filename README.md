# AI Fact Checker for News & Videos

A Chrome extension for fact-checking and analyzing news articles and videos (YouTube/TikTok) using the OpenAI and ClaimBuster APIs.

**How it works:** Articles are extracted directly from the page; for videos, the audio track is recorded, transcribed with OpenAI Whisper, and then — just like articles — analyzed in parallel with GPT-4.1-nano and ClaimBuster for factual accuracy, bias, and manipulation techniques. The results appear in a panel directly on the page.

## Installing the Extension

### Step 1: Download the repository

```bash
git clone https://github.com/ibrahimzarouri/AI-Fact-Checker-for-News-and-Videos.git
```

Or download it as a ZIP (Code → Download ZIP) and extract it.

### Step 2: Configure API keys

1. Copy the file `config.template.js` and rename the copy to `config.js`
2. Open `config.js` in a text editor
3. Insert your API keys:

```javascript
const API_KEYS = {
    OPENAI_API_KEY: 'insert-your-openai-api-key-here',
    CLAIMBUSTER_API_KEY: 'insert-your-claimbuster-api-key-here' // Optional
};
```

4. Save the file

**Getting API keys:**
- OpenAI API (required): https://platform.openai.com/api-keys
- ClaimBuster API (optional): https://idir.uta.edu/claimbuster/api/

> `config.js` is listed in `.gitignore` and is never uploaded — your keys stay local.

### Step 3: Load the Chrome extension

1. Open Google Chrome
2. Go to `chrome://extensions/` (type it into the address bar)
3. Enable **Developer mode** (toggle in the top right)
4. Click **"Load unpacked"**
5. Select the project folder (the folder containing `manifest.json`)

### Step 4: Use the extension

1. Visit a supported news site (e.g. bild.de, spiegel.de, bbc.com) or a video on YouTube/TikTok
2. The analysis starts automatically — open the results via the floating button

## Key Files

| File | Purpose |
|---|---|
| `manifest.json` | Extension configuration (Manifest V3) |
| `background.js` | Core logic and API calls (OpenAI, Whisper, ClaimBuster) |
| `content.js` | Website integration, audio extraction, and results panel |
| `styles.css` | Styling of the analysis panel |
| `config.template.js` | Template for API keys |
| `config.js` | Your API keys (created by you, not in the repository) |
| `ground_truth/` | Evaluation dataset with annotated articles |
| `popup.html` / `popup.js` | Disabled (minimal, direct operation) |

## Requirements

- Google Chrome browser
- OpenAI API key (configure in `config.js`)
- ClaimBuster API key (optional, configure in `config.js`)

---

Developed for educational purposes — Bachelor's thesis by [Ibrahim Zarouri](https://github.com/ibrahimzarouri).
For detailed technical documentation, see [DEVELOPER_GUIDE.md](DEVELOPER_GUIDE.md).
