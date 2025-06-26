# Agentensystem zur Spielertauschverhandlung

Dieses Projekt implementiert ein agentenbasiertes System zur Simulation von Spielertransferverhandlungen im Profifußball. Die Anwendung ermöglicht es, Verhandlungen zwischen Vereinen mit unterschiedlichen Strategien zu simulieren und zu visualisieren.

## Voraussetzungen

Stellen Sie sicher, dass die folgende Software auf Ihrem System installiert ist:

* **Python**: Version 3.9 oder neuer.  
* **pip**: Der Python Package Installer (wird in der Regel mit Python installiert).  
* **Git**: Optional, zum Klonen des Repositories.  

## Installation (Anleitung für Windows)

Führen Sie die folgenden Schritte im Windows Terminal (Eingabeaufforderung oder PowerShell) aus.

### 1. Projektdateien beziehen

Klone Sie das Repository mit Git:

```bash
git clone <URL_des_Projekts>
```

*Alternativ können Sie die Projektdateien als ZIP-Archiv herunterladen und manuell entpacken.*

### 2. Projektverzeichnis öffnen

Navigieren Sie in das Hauptverzeichnis des Projekts:

```bash
cd pfad\zum\projekt
```

### 3. Virtuelle Umgebung erstellen und aktiviere

```bash
# Erstellen der virtuellen Umgebung (der Name "venv" ist eine Konvention)
python -m venv venv

# Aktivieren der virtuellen Umgebung
.\venv\Scripts\activate
```

Nach der Aktivierung sollte `(venv)` am Anfang Ihrer Kommandozeile erscheinen.

### 4. Abhängigkeiten installieren

Installieren Sie alle für das Projekt erforderlichen Python-Bibliotheken:

```bash
pip install -r requirements.txt
```

## Datenquelle einrichten

Die Anwendung benötigt eine Datengrundlage zur Analyse.

* **CSV-Datei**: Für die Ausführung wird eine CSV-Datei mit Spielerdaten benötigt.  
* **Dateiname und Speicherort**: Stellen Sie sicher, dass die Datei `player_stats.csv` heißt und sich direkt im Hauptverzeichnis des Projekts befindet.  
* *Hinweis*: Die ursprüngliche Datengrundlage für dieses Projekt stammt von Plattformen wie Kaggle.  

## Ausführung der Anwendung

Nach erfolgreicher Installation kann die interaktive Webanwendung gestartet werden.

1. Stellen Sie sicher, dass Ihre virtuelle Umgebung noch aktiv ist (`(venv)` wird angezeigt).  
2. Führen Sie den folgenden Befehl im Hauptverzeichnis des Projekts aus:

```bash
streamlit run app.py
```

Dieser Befehl startet einen lokalen Webserver und öffnet die Anwendung automatisch in Ihrem Standard-Webbrowser. Nun können Sie die Simulationen durchführen.

## Projekt-Abhängigkeiten (`requirements.txt`)

```text
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
matplotlib==3.10.3
narwhals==1.39.0
numpy==2.2.5
packaging==24.2
pandas==2.2.3
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
streamlit==1.45.1
tenacity==9.1.2
toml==0.10.2
tornado==6.4.2
typing_extensions==4.13.2
tzdata==2025.2
urllib3==2.4.0
```