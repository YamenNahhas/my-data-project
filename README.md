# 📋 Template-Anleitung

> **Für Kursteilnehmer*innen:** Diese Sektion nach dem Setup deines Projekts löschen!

## So verwenden Sie dieses Template:
Dieses Template hilft dir, dein Data Science Projekt effizient zu organisieren und zu dokumentieren. Es bietet eine gängige Struktur, um deine Arbeit zu planen, durchzuführen und zu präsentieren.

### 1. Template verwenden
Templates können in GitHub über den Button **"Use this template" -> "Create a new repository"** in der oberen rechten Ecke in ein eigenes Repository überführt werden. Nutze diese Vorlage als Inspiration und passe sie an dein Projekt an! 

### 2. Projekt klonen
Danach kannst du dein neues Repository direkt über VS Code klonen. Dazu öffnest du in VS Code die Kommando-Palette (Strg+Shift+P) bzw. (Cmd+Shift+P) auf dem Mac und gibst **"Git: Clone"** ein. Wähle dann "Clone from GitHub..." und melde dich ggf. bei GitHub an. Suche nach deinem Repository und wähle einen lokalen Ordner aus, in dem das Projekt gespeichert werden soll.

### 3. Abhängigkeiten installieren
Nachdem du das Repository geklont hast, musst du die Abhängigkeiten installieren. Öffne dazu ein neues Terminal in VS Code über die Menüleiste "Terminal"->"Neues Terminal" und führe die folgenden Befehle aus:

```bash
uv sync
```

### 4. Erweiterungen hinzufügen
Für dieses Projekt empfehlen wir die Installation der folgenden VS Code Erweiterungen:
- **Python** (Microsoft) - Bietet Unterstützung für Python-Entwicklung.
- **Jupyter** (Microsoft) - Ermöglicht das Arbeiten mit Jupyter Notebooks direkt in VS Code.
- **Even Better TOML** (tamasfe) - Verbessert die Bearbeitung von TOML-Dateien.
- **Ruff** (Astral Software) - Ein schneller Linter für Python, der dir hilft, sauberen Code zu schreiben.
- **Material Icon Theme** (PKief) - Verbessert die Dateisymbole in VS Code für eine bessere Übersicht.

Dafür kannst du den Erweiterungs-Tab in VS Code öffnen (Symbol mit den vier Quadraten auf der linken Seitenleiste) und in die Suchleiste `@recommended` eingeben. Danach sollten dir die empfohlenen Erweiterungen angezeigt werden.

### Notebooks ausführen
Im Ordner `notebooks/` findest du ein Jupyter Notebook namens `01_exploration.ipynb`, das als Ausgangspunkt für deine Datenanalyse dient. Öffne das Notebook in VS Code und wähle oben rechts dein virtuelles Environment als Kernel aus. Führe die Zellen nacheinander aus. Wenn alles geklappt hat wird das Notebook einen Datensatz von Kaggle laden und im Ordner `data/` speichern.

Von hier an kannst du mit deinem Projekt starten und die Vorlagen nach belieben anpassen.

Schaue dir für weitere Informationen zum Template die Datei [docs/project.md](./docs/project.md) an.


Für dein Projekt kannst du die folgenden Abschnitte in der `README.md` Datei anpassen, um dein Projekt zu beschreiben und zu präsentieren. Lösche anschließend diese Anleitung.

---

# [DEIN PROJEKTTITEL HIER] 🚀

> Hier geht es um diabetes dataset von kaggle. Dieses Dataset besteht aus 100.000 Zeilen und 32 Spalten inklusiv demographics, lifestyle, medical history und clinical meaurements.

## 📊 Projektübersicht

**Problemstellung:** 
Diese Erkrankung ist hochgradig heterogen. Patienten mit gleicher Diagnose zeigen sehr unterschiedliche metabolische Profile. Klassische Grenzwerte (z. B. HbA1c ≥ 6.5 %) erfassen diese Heterogenität nur unzureichend. Therapieeffekte senken Biomarker, Diagnose bleibt bestehen.

**Ziel:** 
Besser Verständnis von Risikofaktoren. Tieferes Verständnis der metabolischen Heterogenität von Diabetes und ergänzt klassische medizinische Grenzwerte durch probabilistische und clusterbasierte Erkenntnisse.

**Methoden:** 
Cleaning, Exploratory Data Analysis(EDA), Grouppierung, Lineare Regression, Logistische Regression, Clustering, Visualisierung mit matplotlib



## Setup

Klone das Repository
```bash
# Repository klonen
git clone [DEIN-REPO-LINK]
cd [REPO-NAME]
```

Installiere [uv](https://uv.dev) (falls noch nicht installiert) und synchronisiere die Abhängigkeiten
```bash
# Dependencies installieren
uv sync
```

### Ausführung

Notebooks in dieser Reihenfolge ausführen:
1. notebooks/01_exploration.ipynb
2. nootbooks/diabetes.ipynb
3. notebooks/diabetes_preperation_and_processing.ipynb
4. notebooks/diabetes_visualization_and_discussion.ipynb
-->


