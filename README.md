# AI Fact Checker for News & Videos

Eine Chrome-Erweiterung zur Überprüfung von Fakten und Analyse von Nachrichtenartikeln und Videos (YouTube/TikTok) mit OpenAI und ClaimBuster APIs.

**Funktionsweise:** Artikel werden direkt von der Seite extrahiert; bei Videos wird die Tonspur aufgenommen, mit OpenAI Whisper transkribiert und anschließend – wie bei Artikeln – parallel mit GPT-4.1-nano und ClaimBuster auf Faktentreue, Bias und Manipulationstechniken analysiert. Die Ergebnisse erscheinen in einem Panel direkt auf der Seite.

## Installation der Erweiterung

### Schritt 1: Repository herunterladen

```bash
git clone https://github.com/ibrahimzarouri/AI-Fact-Checker-for-News-and-Videos.git
```

Oder als ZIP herunterladen (Code → Download ZIP) und entpacken.

### Schritt 2: API-Schlüssel konfigurieren

1. Kopieren Sie die Datei `config.template.js` und benennen Sie die Kopie in `config.js` um
2. Öffnen Sie `config.js` mit einem Texteditor
3. Fügen Sie Ihre API-Schlüssel ein:

```javascript
const API_KEYS = {
    OPENAI_API_KEY: 'hier-ihren-openai-api-schlüssel-einfügen',
    CLAIMBUSTER_API_KEY: 'hier-ihren-claimbuster-api-schlüssel-einfügen' // Optional
};
```

4. Speichern Sie die Datei

**API-Schlüssel erhalten:**
- OpenAI API (erforderlich): https://platform.openai.com/api-keys
- ClaimBuster API (optional): https://idir.uta.edu/claimbuster/api/

> `config.js` steht in der `.gitignore` und wird niemals mit hochgeladen – Ihre Schlüssel bleiben lokal.

### Schritt 3: Chrome-Erweiterung laden

1. Öffnen Sie Google Chrome
2. Gehen Sie zu `chrome://extensions/` (in die Adresszeile eingeben)
3. Aktivieren Sie den **Entwicklermodus** (Toggle oben rechts)
4. Klicken Sie auf **"Ungepackte Erweiterung laden"**
5. Wählen Sie den Projektordner aus (der Ordner mit der `manifest.json`)

### Schritt 4: Erweiterung verwenden

1. Besuchen Sie eine unterstützte Nachrichtenseite (z.B. bild.de, spiegel.de, bbc.com) oder ein Video auf YouTube/TikTok
2. Die Analyse wird automatisch gestartet – Ergebnisse über den schwebenden Button öffnen

## Wichtige Dateien

| Datei | Zweck |
|---|---|
| `manifest.json` | Erweiterungs-Konfiguration (Manifest V3) |
| `background.js` | Hauptlogik und API-Aufrufe (OpenAI, Whisper, ClaimBuster) |
| `content.js` | Website-Integration, Audio-Extraktion und Ergebnis-Panel |
| `styles.css` | Styling des Analyse-Panels |
| `config.template.js` | Vorlage für API-Schlüssel |
| `config.js` | Ihre API-Schlüssel (von Ihnen erstellt, nicht im Repository) |
| `ground_truth/` | Evaluationsdatensatz mit annotierten Artikeln |
| `popup.html` / `popup.js` | Deaktiviert (minimale, direkte Bedienung) |

## Anforderungen

- Google Chrome Browser
- OpenAI API Key (in `config.js` konfigurieren)
- ClaimBuster API Key (optional, in `config.js` konfigurieren)

---

Entwickelt für Bildungszwecke — Bachelorarbeit von [Ibrahim Zarouri](https://github.com/ibrahimzarouri).
Ausführliche technische Dokumentation: siehe [DEVELOPER_GUIDE.md](DEVELOPER_GUIDE.md).
