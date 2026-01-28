# Schnellstart-Anleitung

## 🚀 In 3 Schritten zur Präsentation

### 1. Installation

```bash
# Von slidev-theme-noser starten (wie gewünscht)
git clone https://gitlab.com/31ch/slidev-theme-noser.git meine-praesentation
cd meine-praesentation

# Kanton Luzern Theme-Dateien kopieren
# (Kopieren Sie alle Dateien aus slidev-kanton-luzern-2024)

# Dependencies installieren
npm install
```

### 2. Konfiguration

Erstellen Sie `slides.md`:

```markdown
---
theme: ./
title: Meine Präsentation
subtitle: Untertitel
author: Ihr Name
date: 28.01.2026
department: Ihr Departement
website: https://www.lu.ch
layout: cover
---

# Willkommen

Ihre Präsentation beginnt hier
```

### 3. Starten

```bash
# Entwicklungsserver
npm run dev

# Browser öffnet automatisch: http://localhost:3030
```

## 📋 Verfügbare Layouts

```markdown
---
layout: cover       # Titelfolie
layout: default     # Standard-Inhalt
layout: section     # Kapitelteiler
layout: two-cols    # Zweispaltig
layout: image-right # Bild rechts
layout: end         # Abschluss
---
```

## 🎨 Corporate Design Farben

- **Himmelblau:** `#009FE3` (Primärfarbe)
- **Mitternachtsblau:** `#09202C` (Sekundärfarbe)
- **Puderblau:** `#94BED4` (Akzent)
- **Hellblau:** `#DEF0FA` (Akzent)

## 📝 Wichtige Befehle

| Befehl | Beschreibung |
|--------|--------------|
| `npm run dev` | Entwicklungsserver |
| `npm run build` | Für Produktion bauen |
| `npm run export` | PDF exportieren |

## 🎯 Best Practices

1. **Logo:** Automatisch oben links
2. **Schrift:** Segoe UI (vorinstalliert)
3. **Eine Idee** pro Folie
4. **Max. 5-7** Bulletpoints
5. **Bilder** in `public/images/`

## 🖼️ Bilder verwenden

```bash
# Ordner erstellen
mkdir -p public/images

# Bild kopieren
cp mein-bild.jpg public/images/

# In Folie verwenden
---
layout: image-right
image: /images/mein-bild.jpg
---
```

## 💡 Tipps

- Testen Sie auf dem Präsentations-Display
- Exportieren Sie als PDF als Backup
- Folgen Sie den CD-Richtlinien
- Kurze, prägnante Texte

## 🆘 Hilfe

**Corporate Design:**  
www.lu.ch/cd

**Staatskanzlei:**  
information@lu.ch  
Tel. 041 228 6000

**Slidev Dokumentation:**  
https://sli.dev

---

**Viel Erfolg mit Ihrer Präsentation!** 🎉
