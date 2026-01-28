# Slidev Theme: Kanton Luzern (Official 2024)

**Offizielle Slidev-Theme basierend auf dem Corporate Design des Kantons Luzern**

Version 2.0.0 - basierend auf CD Manual v1.00.02 (Januar 2024)

## 🎯 Übersicht

Dieses Theme folgt den offiziellen Corporate Design-Richtlinien des Kantons Luzern:
- **Einfach** - Reduziert auf das Wesentliche
- **Einprägsam** - Hoher Wiedererkennungswert  
- **Zweckmässig** - Funktional und digitaltauglich

## ✨ Features

### Corporate Design Compliance
- ✅ Offizielles Logo (Version 2024)
- ✅ Korrekte Farbpalette (Himmelblau #009FE3)
- ✅ Segoe UI Schriftart (wie im CD Manual vorgeschrieben)
- ✅ Korrekte Logo-Platzierung (oben links)
- ✅ Professionelles, modernes Design

### Layouts
- **cover** - Titelfolie
- **default** - Standard-Inhaltsfolie
- **section** - Kapitelübersicht
- **two-cols** - Zweispaltig
- **image-right** - Bild rechts, Text links
- **end** - Abschlussfolie

### Technisch
- Responsive Design
- Optimiert für Bildschirm und PDF-Export
- Basis: Slidev ≥ 0.48.0
- Node.js ≥ 14.0.0

## 🚀 Installation

### Option 1: Von slidev-theme-noser starten (wie gewünscht)

```bash
# 1. Kanton Luzern Theme klonen
git clone https://github.com/mmgreiner/slidev-theme-lu.git meine-praesentation
cd meine-praesentation

# 2. Dependencies installieren
npm install
# oder
pnpm install

# 4. Entwicklungsserver starten
npm run dev
```

### Option 2: Direkte Verwendung

```bash
# 1. Theme-Verzeichnis kopieren
cp -r slidev-kanton-luzern-2024 meine-praesentation
cd meine-praesentation

# 2. Slidev installieren
npm install -D @slidev/cli
# oder
pnpm add -D @slidev/cli

# 3. Logo ins public-Verzeichnis kopieren
mkdir -p public
cp Logo_Kanton_Luzern_RGB.svg public/

# 4. slides.md erstellen und Server starten
npm run dev
```

## 📝 Verwendung

### Basis-Konfiguration

Erstellen Sie eine `slides.md` Datei:

```markdown
---
theme: ./
title: Ihre Präsentation
subtitle: Untertitel (optional)
author: Ihr Name
date: 28. Januar 2026
department: Ihr Departement
website: https://www.lu.ch
contact: ihre.email@lu.ch
layout: cover
---

# Ihre Präsentation

Untertitel oder Beschreibung

---
layout: default
---

# Erste Folie

Ihr Inhalt hier
```

### Verfügbare Layouts

#### Cover (Titelfolie)

```markdown
---
layout: cover
---

# Haupttitel

Untertitel
```

**Features:**
- Zentrierter Inhalt
- Logo oben links
- Autor, Datum, Departement aus Frontmatter

#### Default (Standard)

```markdown
---
layout: default
---

# Folientitel

Ihr Inhalt:
- Punkt 1
- Punkt 2
```

**Features:**
- Logo oben links
- Fusszeile mit Departement und Seitenzahl
- Optimiert für Text und Listen

#### Section (Kapitelteiler)

```markdown
---
layout: section
---

# Neues Kapitel

## Untertitel
```

**Features:**
- Grosser, zentrierter Titel
- Für visuelle Pausen
- Kapitelübersichten

#### Two-Cols (Zweispaltig)

```markdown
---
layout: two-cols
---

::left::

# Linke Spalte

Inhalt links

::right::

# Rechte Spalte

Inhalt rechts
```

#### Image-Right (Bild rechts)

```markdown
---
layout: image-right
image: /images/foto.jpg
imageAlt: Bildbeschreibung
---

# Titel

Text erscheint links,
Bild rechts
```

#### End (Abschluss)

```markdown
---
layout: end
---

# Vielen Dank

## Fragen?

Kontaktinformationen
```

## 🎨 Corporate Design Farben

Gemäss CD Manual v1.00.02:

```css
/* Primärfarbe */
--kl-himmelblau: #009FE3;

/* Sekundärfarbe */
--kl-mitternachtsblau: #09202C;

/* Akzentfarben */
--kl-puderblau: #94BED4;
--kl-hellblau: #DEF0FA;

/* Basis */
--kl-black: #000000;
--kl-white: #FFFFFF;
--kl-grey: #999999;
```

### Verwendung in Slides

```markdown
<div class="text-blue">
  Text in Himmelblau
</div>

<div class="bg-blue" style="padding: 2rem; border-radius: 4px;">
  Blauer Hintergrund mit weissem Text
</div>
```

## 🔤 Typografie

**Standardschrift:** Segoe UI (wie im CD Manual vorgeschrieben)

```markdown
# H1 - Haupttitel (2.5rem)
## H2 - Zwischentitel (2rem)
### H3 - Untertitel (1.5rem)

**Fett** für Hervorhebungen
*Kursiv* für Betonungen
```

## 🖼️ Bilder verwenden

```bash
# Bilder im public-Ordner ablegen
mkdir -p public/images
cp mein-bild.jpg public/images/

# In slides.md referenzieren
---
layout: image-right
image: /images/mein-bild.jpg
---
```

## 📋 Best Practices

### Gemäss CD Manual

1. **Logo-Verwendung**
   - Immer oben links
   - Einmalig pro Ansicht
   - Organisationshinweis nur wenn nötig

2. **Schriftgrössen**
   - Lesbar auch auf kleinen Bildschirmen
   - Hierarchie beachten (H1 > H2 > H3)

3. **Farben**
   - Himmelblau für Akzente
   - Schwarz für Text
   - Weiss als Hintergrund

4. **Content**
   - Eine Idee pro Folie
   - Maximal 5-7 Bulletpoints
   - Kurze, prägnante Texte

### Präsentations-Struktur

```markdown
1. Cover - Titelfolie
2. Default - Agenda
3. Section - Kapitel 1
4. Default - Inhalt (3-5 Folien)
5. Section - Kapitel 2
6. Default - Inhalt (3-5 Folien)
7. End - Dank/Fragen
```

## 🛠️ Entwicklung

```bash
# Server starten
npm run dev
# Öffnet http://localhost:3030

# PDF exportieren
npm run export
# or
npx slidev export my-slides.md
# or
npx slidev export my-slides.md --format png

# Für Produktion bauen
npm run build
# or
npx slidev build my-slides.md
```

## 📦 Verzeichnisstruktur

```
slidev-kanton-luzern-2024/
├── layouts/
│   ├── cover.vue          # Titelfolie
│   ├── default.vue        # Standard
│   ├── section.vue        # Kapitel
│   ├── two-cols.vue       # Zweispaltig
│   ├── image-right.vue    # Bild rechts
│   └── end.vue           # Abschluss
├── styles/
│   └── index.css          # Hauptstyle
├── Logo_Kanton_Luzern_RGB.svg
├── package.json
└── README.md
```

## 🎯 Keyboard Shortcuts

Während der Präsentation:

- `Space` / `→` - Nächste Folie
- `←` - Vorherige Folie
- `O` - Übersicht
- `F` - Vollbild
- `G` - Gehe zu Folie (Nummer eingeben)
- `D` - Dark Mode (nicht empfohlen für CD)

## 📚 Ressourcen

- [Corporate Design Manual](https://www.lu.ch/cd)
- [Slidev Dokumentation](https://sli.dev)
- [Vue.js Dokumentation](https://vuejs.org)

## 🔗 Unterstützung

Für Fragen zum Corporate Design:

**Staatskanzlei Luzern**  
Kommunikation  
information@lu.ch  
Tel. 041 228 6000

Für technische Fragen zu Slidev:
- [Slidev GitHub](https://github.com/slidevjs/slidev)
- [Slidev Discussions](https://github.com/slidevjs/slidev/discussions)

## 📄 Lizenz

MIT License

**Wichtig:** Die Verwendung muss den offiziellen Corporate Design-Richtlinien des Kantons Luzern entsprechen.

## ✅ Checkliste

Vor der Verwendung:

- [ ] Logo im `public/` Verzeichnis
- [ ] Frontmatter korrekt ausgefüllt
- [ ] Segoe UI installiert (meist vorinstalliert)
- [ ] CD-Richtlinien gelesen
- [ ] Präsentation getestet (Dev-Server)
- [ ] PDF-Export geprüft

## 📌 Version

**Version:** 2.0.0  
**Basis:** Corporate Design Kanton Luzern v1.00.02 (Januar 2024)  
**Erstellt:** Januar 2026  
**Slidev:** ≥ 0.48.0

---

**Bereit für professionelle Präsentationen!** 🎉
