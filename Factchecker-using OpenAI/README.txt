FactChecker Chrome Extension

Eine Chrome-Erweiterung zur Überprüfung von Fakten und Analyse von Artikeln mit OpenAI und ClaimBuster APIs.

Installation der Erweiterung

Schritt 1: Download und Entpacken
1. Laden Sie die Datei `FactChecker.zip` herunter
2. Entpacken Sie die ZIP-Datei in einen Ordner Ihrer Wahl
3. Merken Sie sich den Pfad zum entpackten Ordner

Schritt 2: API-Schlüssel konfigurieren
1. Öffnen Sie den entpackten FactChecker-Ordner
2. Kopieren Sie die Datei `config.template.js` und benennen Sie die Kopie in `config.js` um
3. Öffnen Sie `config.js` mit einem Texteditor (z.B. Notepad)
4. Fügen Sie Ihre API-Schlüssel ein:
   ```javascript
   const API_KEYS = {
     OPENAI_API_KEY: 'hier-ihren-openai-api-schlüssel-einfügen',
     CLAIMBUSTER_API_KEY: 'hier-ihren-claimbuster-api-schlüssel-einfügen' // Optional
   };
   ```
5. Speichern Sie die Datei

API-Schlüssel erhalten:
- OpenAI API (erforderlich): https://platform.openai.com/api-keys
- ClaimBuster API (optional): https://idir.uta.edu/claimbuster/api/

Schritt 3: Chrome-Erweiterung laden
1. Öffnen Sie Google Chrome
2. Gehen Sie zu `chrome://extensions/` (in die Adresszeile eingeben)
3. Aktivieren Sie den Entwicklermodus (Toggle oben rechts)
4. Klicken Sie auf "Ungepackte Erweiterung laden"
5. Wählen Sie den entpackten FactChecker-Ordner aus
6. Die Erweiterung wird nun in Chrome installiert

Schritt 4: Erweiterung verwenden
1. Besuchen Sie eine Nachrichtenseite
2. Die Analyse wird automatisch gestartet

Code in Visual Studio Code öffnen

Schritt 1: VS Code installieren
- Falls noch nicht installiert: "https://code.visualstudio.com"

Schritt 2: Projekt öffnen
1. Öffnen Sie Visual Studio Code
2. Klicken Sie auf "Datei" → "Ordner öffnen"
3. Wählen Sie den entpackten FactChecker-Ordner aus
4. Der gesamte Code wird im VS Code Explorer angezeigt

Wichtige Dateien:
- `manifest.json` - Erweiterungs-Konfiguration
- `background.js` - Hauptlogik und API-Aufrufe
- `popup.html` - Benutzeroberfläche (deaktiviert für minimale, direkte Bedienung)
- `popup.js` - UI-Interaktionen (deaktiviert für minimale, direkte Bedienung)
- `content.js` - Website-Integration
- `config.template.js` - Vorlage für API-Schlüssel
- `config.js` - Ihre API-Schlüssel (wird von Ihnen erstellt)

Anforderungen
- Google Chrome Browser
- OpenAI API Key (in `config.js` konfigurieren)
- ClaimBuster API Key (optional, in `config.js` konfigurieren)

---
Entwickelt für Bildungszwecke