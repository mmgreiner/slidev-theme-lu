# Installations- und Verwendungsanleitung

## Kanton Luzern Slidev Theme (Offiziell 2024)

Basierend auf Corporate Design Manual v1.00.02 (Januar 2024)

---

## 📦 Was Sie erhalten haben

Dieses Theme-Paket enthält:

### Hauptdateien
- `package.json` - Theme-Konfiguration
- `Logo_Kanton_Luzern_RGB.svg` - Offizielles Logo
- `README.md` - Vollständige Dokumentation
- `SCHNELLSTART.md` - Kurzanleitung
- `example-slides.md` - Vollständiges Beispiel

### Layouts (`layouts/`)
- `cover.vue` - Titelfolie
- `default.vue` - Standard-Inhaltsfolie
- `section.vue` - Kapitelteiler
- `two-cols.vue` - Zweispaltiges Layout
- `image-right.vue` - Bild rechts, Text links
- `end.vue` - Abschlussfolie

### Styles (`styles/`)
- `index.css` - Vollständiges Corporate Design CSS

---

## 🚀 Installation

### Voraussetzungen

Stellen Sie sicher, dass installiert ist:
- **Node.js** ≥ 14.0.0 ([Download](https://nodejs.org/))
- **npm** oder **pnpm**
- **Code-Editor** (VS Code empfohlen)

### Methode 1: Von slidev-theme-noser starten

Wie in Ihrer Anfrage gewünscht:

```bash
# 1. Noser Theme klonen
git clone https://gitlab.com/31ch/slidev-theme-noser.git meine-praesentation
cd meine-praesentation

# 2. Kanton Luzern Theme-Dateien kopieren
# Kopieren Sie alle Dateien aus dem slidev-kanton-luzern-2024 Ordner
# in Ihr Projektverzeichnis (überschreiben Sie die bestehenden Dateien)

# 3. Dependencies installieren
npm install
# oder mit pnpm
pnpm install

# 4. Logo ins public-Verzeichnis kopieren
mkdir -p public
cp Logo_Kanton_Luzern_RGB.svg public/

# 5. Entwicklungsserver starten
npm run dev
```

### Methode 2: Neues Projekt erstellen

```bash
# 1. Neues Verzeichnis erstellen
mkdir meine-praesentation
cd meine-praesentation

# 2. Alle Theme-Dateien kopieren
cp -r /pfad/zu/slidev-kanton-luzern-2024/* .

# 3. Slidev installieren
npm install -D @slidev/cli
# oder
pnpm add -D @slidev/cli

# 4. Logo vorbereiten
mkdir -p public
cp Logo_Kanton_Luzern_RGB.svg public/

# 5. slides.md erstellen (siehe nächster Abschnitt)

# 6. Server starten
npm run dev
```

---

## 📝 Erste Präsentation erstellen

### Basis-Template

Erstellen Sie eine Datei `slides.md`:

```markdown
---
theme: ./
title: Digitale Transformation
subtitle: Strategie und Umsetzung 2026
author: Dr. Maria Muster
date: 28. Januar 2026
department: Staatskanzlei
website: https://www.lu.ch
contact: maria.muster@lu.ch
layout: cover
---

# Digitale Transformation

Strategie und Umsetzung 2026

---
layout: default
---

# Agenda

1. Ausgangslage
2. Vision und Ziele
3. Massnahmen
4. Zeitplan

---
layout: section
---

# Ausgangslage

## Wo stehen wir heute?

---
layout: default
---

# Aktueller Stand

- **Status Punkt 1:** Details hier
- **Status Punkt 2:** Weitere Informationen
- **Status Punkt 3:** Zusätzliche Punkte

---
layout: end
---

# Vielen Dank

## Fragen?

Kontaktinformationen
```

---

## 🎨 Layout-Übersicht

### 1. Cover (Titelfolie)

```markdown
---
layout: cover
---

# Haupttitel

Untertitel oder Kurzbeschreibung
```

**Verwendung:**
- Erste Folie der Präsentation
- Zeigt Titel, Untertitel, Autor, Datum
- Logo automatisch oben links

### 2. Default (Standard-Inhalt)

```markdown
---
layout: default
---

# Folientitel

Ihr Inhalt:
- Punkt 1
- Punkt 2
- Punkt 3
```

**Verwendung:**
- Hauptlayout für Inhaltsfolien
- Text, Listen, Tabellen
- Fusszeile mit Departement und Seitenzahl

### 3. Section (Kapitelteiler)

```markdown
---
layout: section
---

# Neues Kapitel

## Untertitel des Kapitels
```

**Verwendung:**
- Visuelle Pause zwischen Kapiteln
- Grosser, zentrierter Titel
- Strukturierung der Präsentation

### 4. Two-Cols (Zweispaltig)

```markdown
---
layout: two-cols
---

::left::

# Linke Spalte

Inhalt für links

::right::

# Rechte Spalte

Inhalt für rechts
```

**Verwendung:**
- Vergleiche
- Gegenüberstellungen
- Parallele Informationen

### 5. Image-Right (Bild rechts)

```markdown
---
layout: image-right
image: /images/foto.jpg
imageAlt: Beschreibung des Bildes
---

# Titel

Text erscheint links,
Bild wird rechts angezeigt
```

**Verwendung:**
- Text mit unterstützendem Bild
- Visualisierungen
- Fotos und Grafiken

### 6. End (Abschlussfolie)

```markdown
---
layout: end
---

# Vielen Dank

## Fragen?

Kontaktinformationen hier
```

**Verwendung:**
- Letzte Folie
- Dank und Kontaktinfo
- Website-Link wird automatisch angezeigt

---

## 🖼️ Bilder verwenden

### Bilder hinzufügen

```bash
# 1. Verzeichnis erstellen
mkdir -p public/images

# 2. Bilder kopieren
cp mein-bild.jpg public/images/
cp grafik.png public/images/
```

### In Slides referenzieren

```markdown
# Methode 1: In Layout
---
layout: image-right
image: /images/mein-bild.jpg
imageAlt: Beschreibung
---

# Methode 2: Im Text
![Bildbeschreibung](/images/grafik.png)
```

### Externe Bilder

```markdown
---
layout: image-right
image: https://example.com/bild.jpg
---
```

---

## 🎨 Farben verwenden

### Offizieller Kanton Luzern Farbpalette

```css
Himmelblau:         #009FE3 (Primärfarbe)
Mitternachtsblau:   #09202C (Sekundärfarbe)
Puderblau:          #94BED4 (Akzentfarbe)
Hellblau:           #DEF0FA (Akzentfarbe)
Schwarz:            #000000
Weiss:              #FFFFFF
Grau:               #999999
```

### In Slides verwenden

```markdown
---
layout: default
---

# Folie mit Farben

<div class="text-blue">
  Dieser Text ist in Himmelblau
</div>

<div class="bg-blue" style="padding: 2rem; border-radius: 4px;">
  Blauer Hintergrund mit weissem Text
</div>

<div class="bg-light" style="padding: 1rem; border-radius: 4px;">
  Hellblauer Hintergrund
</div>
```

---

## 📋 Best Practices

### Gemäss Corporate Design Manual

1. **Logo:**
   - Immer oben links (automatisch)
   - Nicht ändern oder verschieben
   - Einmalig pro Folie

2. **Schrift:**
   - Segoe UI wird automatisch verwendet
   - Nicht andere Schriften verwenden
   - Hierarchie beachten (H1 > H2 > H3)

3. **Farben:**
   - Himmelblau für Akzente
   - Schwarz für Text
   - Weiss als Hintergrund
   - Sparsam mit Farben umgehen

4. **Content:**
   - Eine Hauptidee pro Folie
   - Maximal 5-7 Bulletpoints
   - Kurze, prägnante Sätze
   - Genug Weissraum

### Präsentations-Struktur

```
1. Cover       - Titel und Einführung
2. Default     - Agenda
3. Section     - Kapitel 1
4. Default     - Inhalt (3-5 Folien)
5. Section     - Kapitel 2
6. Default     - Inhalt (3-5 Folien)
7. End         - Dank und Fragen
```

---

## 🛠️ Entwicklung und Export

### Während der Entwicklung

```bash
# Server starten
npm run dev
# Öffnet http://localhost:3030

# Server mit anderem Port
npx slidev --port 3333

# Server mit Auto-Open Browser
npx slidev --open
```

### PDF Export

```bash
# Standard-Export
npm run export

# Mit eigenem Dateinamen
npx slidev export --output meine-praesentation.pdf

# Mit Dark Mode (nicht empfohlen für CD)
npx slidev export --dark
```

### Für Produktion bauen

```bash
# SPA Build für Web-Hosting
npm run build

# Output in dist/ Ordner
# Kann auf Webserver deployed werden
```

---

## ⌨️ Keyboard Shortcuts

Während der Präsentation:

| Taste | Funktion |
|-------|----------|
| `Space` / `→` | Nächste Folie |
| `←` | Vorherige Folie |
| `O` | Übersicht aller Folien |
| `F` | Vollbildmodus |
| `G` | Zu Folie springen (Nummer eingeben) |
| `D` | Dark Mode umschalten |
| `?` | Hilfe anzeigen |
| `Esc` | Übersicht / Vollbild beenden |

---

## 🔧 Fehlerbehebung

### Problem: Port bereits belegt

```bash
# Anderen Port verwenden
npx slidev --port 3333
```

### Problem: Theme lädt nicht

```bash
# Cache löschen
rm -rf .slidev
rm -rf node_modules/.vite

# Neu starten
npm run dev
```

### Problem: Logo wird nicht angezeigt

```bash
# Prüfen, ob Logo vorhanden
ls Logo_Kanton_Luzern_RGB.svg
ls public/Logo_Kanton_Luzern_RGB.svg

# Logo kopieren
cp Logo_Kanton_Luzern_RGB.svg public/

# Server neu starten
```

### Problem: Segoe UI Schrift nicht verfügbar

**Windows:** Normalerweise vorinstalliert  
**macOS:** Normalerweise vorinstalliert  
**Linux:** Installieren Sie `ttf-mscorefonts-installer`

```bash
# Ubuntu/Debian
sudo apt install ttf-mscorefonts-installer
```

---

## 📚 Zusätzliche Ressourcen

### Kanton Luzern

- **Corporate Design Manual:** [www.lu.ch/cd](https://www.lu.ch/cd)
- **Logos und Vorlagen:** [www.lu.ch/cd](https://www.lu.ch/cd) → Logos und Vorlagen
- **Staatskanzlei Kommunikation:** information@lu.ch, Tel. 041 228 6000

### Slidev

- **Offizielle Dokumentation:** [sli.dev](https://sli.dev)
- **GitHub:** [github.com/slidevjs/slidev](https://github.com/slidevjs/slidev)
- **Community:** [GitHub Discussions](https://github.com/slidevjs/slidev/discussions)

### Weitere Tools

- **Vue.js Dokumentation:** [vuejs.org](https://vuejs.org)
- **Markdown Guide:** [markdownguide.org](https://www.markdownguide.org)

---

## ✅ Checkliste vor Präsentation

Vor der Präsentation prüfen:

- [ ] Logo im `public/` Verzeichnis
- [ ] Alle Frontmatter-Felder ausgefüllt
- [ ] Segoe UI Schrift verfügbar
- [ ] Alle Bilder vorhanden und korrekt referenziert
- [ ] Präsentation im Dev-Server getestet
- [ ] Auf Präsentations-Display getestet
- [ ] PDF als Backup exportiert
- [ ] Corporate Design Richtlinien befolgt
- [ ] Rechtschreibung geprüft
- [ ] Präsentation geprobt

---

## 📧 Support

### Für Corporate Design Fragen

**Staatskanzlei Luzern**  
Kommunikation  
Bahnhofstrasse 15  
6002 Luzern

information@lu.ch  
Tel. 041 228 6000

### Für technische Slidev-Fragen

- [Slidev GitHub Issues](https://github.com/slidevjs/slidev/issues)
- [Slidev Discussions](https://github.com/slidevjs/slidev/discussions)
- [Slidev Discord](https://chat.sli.dev)

---

## 📄 Lizenz und Verwendung

**Lizenz:** MIT

**Wichtige Hinweise:**
- Verwendung muss Corporate Design-Richtlinien entsprechen
- Logo ist geschütztes Hoheitszeichen
- Nur für offizielle Zwecke des Kantons Luzern
- Bei Unsicherheiten: Staatskanzlei kontaktieren

---

## 📌 Version und Updates

**Theme Version:** 2.0.0  
**CD Manual Basis:** v1.00.02 (Januar 2024)  
**Erstellt:** Januar 2026  
**Letzte Aktualisierung:** Januar 2026

**Updates prüfen:**  
Kontaktieren Sie die Staatskanzlei für Updates des Corporate Designs.

---

**Viel Erfolg mit Ihren Präsentationen für den Kanton Luzern!** 🎉

Bei Fragen oder Problemen stehen wir gerne zur Verfügung.
