# Club Negotiator – Agentensystem zur Spielertauschverhandlung

Ein intelligentes Multi-Agenten-System zur Simulation von Transferverhandlungen im Profifußball, entwickelt im Rahmen der Lehrveranstaltung **„Intelligente Systeme“**.

---

## Voraussetzungen

* **Python** ≥ 3.9  
* **pip** (wird i. d. R. mit Python installiert)  
* **Git** (optional, zum Klonen des Repositories)  

---

## Installation

> **Hinweis:** Befehle in einer aktivierten (venv)-Umgebung ausführen.  
> Windows-Pfade verwenden `\`, macOS/Linux `/`.

### 1 · Projektdateien beziehen

```bash
git clone <URL_des_Projekts>
```

*Alternativ: ZIP-Archiv herunterladen und entpacken.*

### 2 · Projektverzeichnis öffnen

```bash
cd pfad\zum\projekt          # Windows
# oder
cd /pfad/zum/projekt         # macOS/Linux
```

### 3 · Virtuelle Umgebung erstellen & aktivieren

**Windows**

```bash
python -m venv venv
.\venv\Scripts\activate
```

**macOS / Linux**

```bash
python3 -m venv venv
source venv/bin/activate
```

*(Nach Aktivierung erscheint `(venv)` vor der Eingabeaufforderung.)*

### 4 · Abhängigkeiten installieren

```bash
pip install -r requirements.txt
```

---

## Ausführung der Anwendung

### Web-Interface (empfohlen)

```bash
streamlit run app.py
```

*Öffnet automatisch `http://localhost:8501` im Browser.*

### Kommandozeilen-Interface (Alternative)

```bash
python main.py
```

---

## Erste Schritte

1. **Daten laden**: Sidebar → *Daten laden / Daten neu laden*  
2. **Navigation** wählen:  
   * *Datenübersicht* – Statistiken zu Vereinen & Spielern  
   * *Vereinsanalyse* – Detailanalysen  
   * *Transfer-Verhandlungen* – Hauptfunktion  
3. **Verhandlung konfigurieren**:  
   * Zwei Vereine wählen  
   * Strategie: *offensive*, *defensive*, *balanced*, *technical*, *custom*  
   * Bei *custom*: Attribute per Slider gewichten  
   * Parameter: Runden-Anzahl, Start-Temperatur  
4. **Verhandlung starten** und Live-Updates beobachten  

---

## Projektstruktur (Auszug)

```
├─ app.py              # Streamlit Web-Interface
├─ main.py             # CLI-Interface
├─ config.py           # Zentrale Konfiguration
├─ PlayerAgent.py      # Spieler-Klassen
├─ ClubAgent.py        # Vereins-Agenten mit Strategien
├─ FootballMediator.py # Neutraler Vermittler
├─ PlayerDataLoader.py # CSV-Import & Verarbeitung
├─ TransferTracker.py  # Transfer-Protokollierung
└─ data_class.py       # Hilfsfunktionen
```

---

## Projekt-Abhängigkeiten (`requirements.txt`)

```text
streamlit==1.45.1
pandas==2.2.3
numpy==2.2.5
matplotlib==3.10.3
seaborn==0.13.0
plotly==5.18.0
altair==5.5.0
attrs==25.3.0
blinker==1.9.0
cachetools==5.5.2
certifi==2025.4.26
charset-normalizer==3.4.2
click==8.2.0
contourpy==1.3.2
cycler==0.12.1
fonttools==4.58.0
gitdb==4.0.12
GitPython==3.1.44
idna==3.10
Jinja2==3.1.6
jsonschema==4.23.0
jsonschema-specifications==2025.4.1
kiwisolver==1.4.8
MarkupSafe==3.0.2
narwhals==1.39.0
packaging==24.2
pillow==11.2.1
protobuf==6.31.0
pyarrow==20.0.0
pydeck==0.9.1
pyparsing==3.2.3
python-dateutil==2.9.0.post0
pytz==2025.2
referencing==0.36.2
requests==2.32.3
rpds-py==0.25.0
six==1.17.0
smmap==5.0.2
tenacity==9.1.2
toml==0.10.2
tornado==6.4.2
typing_extensions==4.13.2
tzdata==2025.2
urllib3==2.4.0
```

---

## Fehlerbehebung

| Problem | Lösung |
|---------|--------|
| **ModuleNotFoundError** | Virtuelle Umgebung aktivieren, anschließend `pip install -r requirements.txt`. |
| **FileNotFoundError: player_stats.csv** | CSV liegt nicht im Hauptverzeichnis oder Dateiname falsch. |
| **UnicodeDecodeError** | CSV muss im `ISO-8859-1` Encoding vorliegen (ggf. `config.py` anpassen). |
| **Leere Vereinsliste / keine Vereine** | CSV-Format prüfen: Semikolon-getrennt, mind. 11 Spieler pro Verein, Spaltenüberschriften korrekt. |

---

## Konfiguration anpassen

* **Strategien**: `STRATEGY_CONFIG` in `config.py`  
* **Simulated Annealing**: `SA_CONFIG` (Temperaturverlauf)  
* **System-Parameter**: `SYSTEM_CONFIG` (Dateipfade, Limits)

---
