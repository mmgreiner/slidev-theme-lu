---
theme: ./
title: IT-Sicherheit und Datenschutz
subtitle: Schulung für Mitarbeitende 2026
author: Thomas Weber
date: 28. Januar 2026
department: Dienststelle Informatik
website: https://www.informatik.lu.ch
contact: thomas.weber@lu.ch
layout: cover
---

# IT-Sicherheit und Datenschutz

Schulung für Mitarbeitende 2026

---
layout: default
---

# Agenda

1. **E-Mail-Sicherheit** - Phishing erkennen und vermeiden
2. **Datenschutz-Grundlagen** - DSGVO und kantonale Vorgaben
3. **Prozesse und Workflows** - Sichere Arbeitsabläufe
4. **Incident Response** - Was tun bei Sicherheitsvorfällen?
5. **Best Practices** - Tipps für den Alltag

---
layout: section
---

# E-Mail-Sicherheit

## Phishing erkennen und vermeiden

---
layout: default
---

# Beispiel: Verdächtige E-Mail

<div class="email-component">
  <div class="email-header">
    <div class="email-from"><strong>Von:</strong> support@kantoon-luzern.ch</div>
    <div class="email-to"><strong>An:</strong> mitarbeiter@lu.ch</div>
    <div class="email-subject"><strong>Betreff:</strong> DRINGEND: Passwort zurücksetzen erforderlich!</div>
    <div class="email-date"><strong>Datum:</strong> 27. Januar 2026, 23:47</div>
  </div>
  <div class="email-body">
    <p>Sehr geehrte/r Mitarbeiter/in,</p>
    <p>Aus Sicherheitsgründen müssen Sie Ihr Passwort sofort zurücksetzen. Ihr Konto wird in 24 Stunden gesperrt!</p>
    <p><a href="#" class="suspicious-link">Klicken Sie hier zum Zurücksetzen →</a></p>
    <p>IT-Abteilung Kanton Luzern</p>
  </div>
</div>

<style>
.email-component {
  border: 2px solid #999;
  border-radius: 8px;
  overflow: hidden;
  margin: 2rem 0;
  font-size: 0.9rem;
}
.email-header {
  background: #f5f5f5;
  padding: 1rem;
  border-bottom: 1px solid #999;
}
.email-header > div {
  margin-bottom: 0.25rem;
}
.email-body {
  padding: 1.5rem;
  background: white;
}
.suspicious-link {
  color: #d32f2f;
  text-decoration: underline;
  font-weight: bold;
}
</style>

---
layout: default
---

# Warnsignale erkennen

<div class="info-box warning">
  <div class="info-icon">⚠️</div>
  <div class="info-content">
    <h3>Typische Phishing-Merkmale</h3>
    <ul>
      <li><strong>Falsche Absenderadresse:</strong> "kantoon" statt "kanton"</li>
      <li><strong>Zeitdruck:</strong> "DRINGEND", "in 24 Stunden"</li>
      <li><strong>Verdächtige Links:</strong> Nie direkt auf Links klicken!</li>
      <li><strong>Späte Uhrzeit:</strong> 23:47 Uhr - ungewöhnlich</li>
      <li><strong>Unpersönliche Anrede:</strong> Kein Name genannt</li>
    </ul>
  </div>
</div>

<div class="info-box success">
  <div class="info-icon">✅</div>
  <div class="info-content">
    <h3>Richtig reagieren</h3>
    <p><strong>Nicht antworten, nicht klicken!</strong> Melden Sie verdächtige E-Mails sofort an: <strong>security@lu.ch</strong></p>
  </div>
</div>

<style>
.info-box {
  display: flex;
  gap: 1rem;
  padding: 1.25rem;
  border-radius: 8px;
  margin: 1.5rem 0;
  border-left: 4px solid;
}
.info-box.warning {
  background: #fff3e0;
  border-color: #f57c00;
}
.info-box.success {
  background: #e8f5e9;
  border-color: #2e7d32;
}
.info-box.info {
  background: #e3f2fd;
  border-color: #1976d2;
}
.info-icon {
  font-size: 2rem;
  flex-shrink: 0;
}
.info-content h3 {
  margin: 0 0 0.75rem 0;
  font-size: 1.25rem;
}
.info-content p {
  margin: 0;
}
.info-content ul {
  margin: 0;
  padding-left: 1.25rem;
}
.info-content li {
  margin-bottom: 0.5rem;
}
</style>

---
layout: section
---

# Datenschutz-Grundlagen

## DSGVO und kantonale Vorgaben

---
layout: default
---

# Datenklassifikation

```mermaid
graph TB
    A[Daten im Kanton Luzern] --> B[Öffentlich]
    A --> C[Intern]
    A --> D[Vertraulich]
    A --> E[Streng vertraulich]
    
    B --> B1["Pressemitteilungen<br/>Website-Inhalte"]
    C --> C1["Interne Mitteilungen<br/>Sitzungsprotokolle"]
    D --> D1["Personaldaten<br/>Finanzdaten"]
    E --> E1["Gesundheitsdaten<br/>Strafrechtliche Daten"]
    
    style A fill:#009FE3,stroke:#000,stroke-width:2px,color:#fff
    style B fill:#DEF0FA,stroke:#009FE3,stroke-width:2px
    style C fill:#94BED4,stroke:#009FE3,stroke-width:2px
    style D fill:#f57c00,stroke:#000,stroke-width:2px,color:#fff
    style E fill:#d32f2f,stroke:#000,stroke-width:2px,color:#fff
```

---
layout: two-cols
---

::left::

## Öffentlich & Intern

<div class="info-box success">
  <div class="info-icon">📄</div>
  <div class="info-content">
    <h4>Öffentlich</h4>
    <p>Keine besonderen Schutzmassnahmen</p>
  </div>
</div>

<div class="info-box info">
  <div class="info-icon">🏢</div>
  <div class="info-content">
    <h4>Intern</h4>
    <p>Nur für Mitarbeitende</p>
    <ul>
      <li>Passwortschutz</li>
      <li>Keine externe Weitergabe</li>
    </ul>
  </div>
</div>

::right::

## Vertraulich & Streng vertraulich

<div class="info-box warning">
  <div class="info-icon">🔒</div>
  <div class="info-content">
    <h4>Vertraulich</h4>
    <ul>
      <li>Verschlüsselung erforderlich</li>
      <li>Need-to-know Prinzip</li>
      <li>Zugriffsprotokollierung</li>
    </ul>
  </div>
</div>

<div class="info-box" style="background: #ffebee; border-color: #c62828;">
  <div class="info-icon">🔐</div>
  <div class="info-content">
    <h4>Streng vertraulich</h4>
    <ul>
      <li>Höchste Schutzstufe</li>
      <li>Spezielle Genehmigung</li>
      <li>Separate Systeme</li>
    </ul>
  </div>
</div>

---
layout: section
---

# Prozesse und Workflows

## Sichere Arbeitsabläufe

---
layout: default
---

# E-Mail-Verschlüsselung: Wann und wie?

```mermaid
flowchart TD
    Start([E-Mail senden]) --> Check{Enthält vertrauliche Daten?}
    Check -->|Nein| Normal[Normale E-Mail senden]
    Check -->|Ja| Classify{Datenklassifikation?}
    
    Classify -->|Intern| Option1{Empfänger intern?}
    Option1 -->|Ja| Internal[Normale interne E-Mail]
    Option1 -->|Nein| Encrypt1[Verschlüsselt senden]
    
    Classify -->|Vertraulich| Encrypt2[Verschlüsselt senden]
    Classify -->|Streng vertraulich| Secure["Sichere Plattform nutzen<br/>KEINE E-Mail!"]
    
    Normal --> End([Gesendet])
    Internal --> End
    Encrypt1 --> End
    Encrypt2 --> End
    Secure --> End
    
    style Start fill:#009FE3,stroke:#000,stroke-width:2px,color:#fff
    style End fill:#2e7d32,stroke:#000,stroke-width:2px,color:#fff
    style Check fill:#fff3e0,stroke:#f57c00,stroke-width:2px
    style Classify fill:#fff3e0,stroke:#f57c00,stroke-width:2px
    style Secure fill:#ffebee,stroke:#c62828,stroke-width:2px
```

---
layout: default
---

# Passwort-Richtlinien

<div class="info-box info">
  <div class="info-icon">🔑</div>
  <div class="info-content">
    <h3>Sichere Passwörter erstellen</h3>
    <ul>
      <li><strong>Mindestens 12 Zeichen</strong> (besser 16+)</li>
      <li><strong>Kombination:</strong> Gross-/Kleinbuchstaben, Zahlen, Sonderzeichen</li>
      <li><strong>Keine persönlichen Daten</strong> (Namen, Geburtsdaten, etc.)</li>
      <li><strong>Keine Wörter aus dem Wörterbuch</strong></li>
      <li><strong>Passphrasen nutzen:</strong> "Blau€Baum!Kaffee#2026"</li>
    </ul>
  </div>
</div>

## Passwort-Manager nutzen

✅ **Empfohlen:** KeePass, 1Password, Bitwarden  
✅ **Vorteil:** Ein Masterpasswort merken, alle anderen sicher gespeichert  
✅ **Kanton-Lösung:** Kontaktieren Sie die Dienststelle Informatik

---
layout: default
---

# Umgang mit Datenträgern

```mermaid
graph LR
    A[Datenträger] --> B{Typ?}
    B --> C[USB-Stick]
    B --> D[Externe Festplatte]
    B --> E[Cloud-Speicher]
    
    C --> C1{Verschlüsselt?}
    D --> D1{Verschlüsselt?}
    E --> E1{Genehmigte Cloud?}
    
    C1 -->|Ja| OK1["✓ OK"]
    C1 -->|Nein| NO1["✗ Nur für unkritische Daten"]
    
    D1 -->|Ja| OK2["✓ OK"]
    D1 -->|Nein| NO2["✗ Nur für unkritische Daten"]
    
    E1 -->|Ja| OK3["✓ OK"]
    E1 -->|Nein| NO3["✗ Verboten!"]
    
    style A fill:#009FE3,stroke:#000,stroke-width:2px,color:#fff
    style OK1 fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px
    style OK2 fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px
    style OK3 fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px
    style NO1 fill:#ffebee,stroke:#c62828,stroke-width:2px
    style NO2 fill:#ffebee,stroke:#c62828,stroke-width:2px
    style NO3 fill:#ffebee,stroke:#c62828,stroke-width:2px
```

<div class="info-box warning">
  <div class="info-icon">⚠️</div>
  <div class="info-content">
    <p><strong>Wichtig:</strong> Private Cloud-Dienste (Dropbox, Google Drive, etc.) dürfen NICHT für kantonale Daten verwendet werden!</p>
  </div>
</div>

---
layout: section
---

# Incident Response

## Was tun bei Sicherheitsvorfällen?

---
layout: default
---

# Incident Response Prozess

```mermaid
flowchart TD
    Incident(["🚨 Sicherheitsvorfall erkannt"]) --> Assess{Schweregrad einschätzen}
    
    Assess -->|Gering| Report1["ServiceDesk melden<br/>041 228 69 99"]
    Assess -->|Mittel/Hoch| Report2["Sofort melden:<br/>security@lu.ch<br/>+ ServiceDesk anrufen"]
    
    Report1 --> Document[Vorfall dokumentieren]
    Report2 --> Immediate[Sofortmassnahmen]
    
    Immediate --> I1[Betroffenes System isolieren]
    Immediate --> I2[Passwörter ändern]
    Immediate --> I3[Keine Daten löschen!]
    
    I1 --> Document
    I2 --> Document
    I3 --> Document
    
    Document --> Investigation[IT-Sicherheit untersucht]
    Investigation --> Resolution[Lösung und Wiederherstellung]
    Resolution --> Review[Lessons Learned]
    Review --> End([Abgeschlossen])
    
    style Incident fill:#d32f2f,stroke:#000,stroke-width:3px,color:#fff
    style Report2 fill:#f57c00,stroke:#000,stroke-width:2px,color:#fff
    style Immediate fill:#fff3e0,stroke:#f57c00,stroke-width:2px
    style End fill:#2e7d32,stroke:#000,stroke-width:2px,color:#fff
```

---
layout: default
---

# Beispiele für Sicherheitsvorfälle

<div class="info-box" style="background: #ffebee; border-color: #c62828;">
  <div class="info-icon">🚨</div>
  <div class="info-content">
    <h3>Kritisch - Sofort melden!</h3>
    <ul>
      <li>Ransomware-Angriff / Verschlüsselung von Daten</li>
      <li>Gestohlener/verlorener Laptop mit sensiblen Daten</li>
      <li>Unbefugter Zugriff auf System erkannt</li>
      <li>Datenleck nach aussen</li>
    </ul>
  </div>
</div>

<div class="info-box warning">
  <div class="info-icon">⚠️</div>
  <div class="info-content">
    <h3>Mittel - Zeitnah melden</h3>
    <ul>
      <li>Verdächtige E-Mail geklickt</li>
      <li>Unsichere Website besucht</li>
      <li>Verdächtiges Verhalten am PC</li>
      <li>Unbekannte Software installiert</li>
    </ul>
  </div>
</div>

---
layout: two-cols
---

::left::

## ✅ DO - Richtig handeln

- **Ruhe bewahren**
- **Sofort melden**
- **System isolieren** (Netzwerk trennen)
- **Screenshots machen** (Beweise sichern)
- **Passwörter ändern** (andere Geräte)
- **IT-Anweisungen folgen**
- **Dokumentieren** (Was, Wann, Wie)

::right::

## ❌ DON'T - Vermeiden

- **Nicht in Panik geraten**
- **Nichts löschen!** (Beweise)
- **Nicht selbst "reparieren"**
- **Nicht ignorieren**
- **Nicht warten** ("Vielleicht geht's weg")
- **Niemandem die Schuld geben**
- **Nicht verschweigen** (keine Angst!)

---
layout: section
---

# Best Practices

## Tipps für den sicheren Alltag

---
layout: default
---

# Checkliste: Tägliche IT-Sicherheit

<div class="info-box info">
  <div class="info-icon">📋</div>
  <div class="info-content">
    <h3>Jeden Tag</h3>
    <ul>
      <li>✅ Bildschirm sperren beim Verlassen (Windows + L)</li>
      <li>✅ E-Mails kritisch prüfen (Absender, Links, Anhänge)</li>
      <li>✅ Nur genehmigte Software nutzen</li>
      <li>✅ Updates installieren (wenn aufgefordert)</li>
    </ul>
  </div>
</div>

<div class="info-box success">
  <div class="info-icon">📅</div>
  <div class="info-content">
    <h3>Regelmässig</h3>
    <ul>
      <li>✅ Passwörter alle 90 Tage ändern</li>
      <li>✅ Nicht benötigte Daten löschen</li>
      <li>✅ Zugriffsrechte prüfen</li>
      <li>✅ Schulungen besuchen</li>
    </ul>
  </div>
</div>

---
layout: default
---

# Clean Desk Policy

```mermaid
graph TD
    A[Arbeitsplatz verlassen] --> B{Computer gesperrt?}
    B -->|Nein| C["✗ Windows + L drücken!"]
    B -->|Ja| D{Vertrauliche Dokumente sichtbar?}
    
    C --> D
    D -->|Ja| E["✗ Dokumente wegsperren"]
    D -->|Nein| F{USB-Sticks/Datenträger am Platz?}
    
    E --> F
    F -->|Ja| G["✗ In verschliessbaren Schrank legen"]
    F -->|Nein| H{Post-its mit Passwörtern?}
    
    G --> H
    H -->|Ja| I["✗✗✗ NIEMALS! Sofort entfernen"]
    H -->|Nein| J["✓ Arbeitsplatz sicher!"]
    
    style A fill:#009FE3,stroke:#000,stroke-width:2px,color:#fff
    style J fill:#2e7d32,stroke:#000,stroke-width:2px,color:#fff
    style C fill:#ffebee,stroke:#c62828,stroke-width:2px
    style E fill:#ffebee,stroke:#c62828,stroke-width:2px
    style G fill:#ffebee,stroke:#c62828,stroke-width:2px
    style I fill:#d32f2f,stroke:#000,stroke-width:3px,color:#fff
```

---
layout: default
---

# Kontakte und Ressourcen

<div class="info-box info">
  <div class="info-icon">📞</div>
  <div class="info-content">
    <h3>Dienststelle Informatik</h3>
    <p><strong>ServiceDesk:</strong> 041 228 69 99 | servicedesk@lu.ch</p>
    <p><strong>IT-Sicherheit:</strong> security@lu.ch</p>
    <p><strong>Montag bis Freitag:</strong> 07:00 - 12:00, 13:00 - 17:30</p>
  </div>
</div>

<div class="info-box success">
  <div class="info-icon">🌐</div>
  <div class="info-content">
    <h3>Intranet-Ressourcen</h3>
    <p><strong>IT-Sicherheitsrichtlinien:</strong> intranet.lu.ch/sicherheit</p>
    <p><strong>Schulungsunterlagen:</strong> intranet.lu.ch/schulungen</p>
    <p><strong>FAQ:</strong> intranet.lu.ch/it-faq</p>
  </div>
</div>

---
layout: default
---

# Zusammenfassung

## Die wichtigsten Punkte

✅ **E-Mail-Sicherheit:** Phishing erkennen, Links prüfen, bei Verdacht melden

✅ **Datenschutz:** Datenklassifikation beachten, vertrauliche Daten schützen

✅ **Starke Passwörter:** Mindestens 12 Zeichen, Passwort-Manager nutzen

✅ **Clean Desk:** Bildschirm sperren, Dokumente wegsperren

✅ **Im Zweifel:** Lieber einmal zu viel melden als zu wenig!

<div class="info-box" style="background: #e3f2fd; border-color: #1976d2; margin-top: 2rem;">
  <div class="info-icon">💡</div>
  <div class="info-content">
    <p style="font-size: 1.25rem;"><strong>Denken Sie daran:</strong> IT-Sicherheit ist Teamarbeit. Jede/r trägt Verantwortung!</p>
  </div>
</div>

---
layout: end
---

# Vielen Dank!

## Fragen und Diskussion

**Kontakt:**  
Thomas Weber  
Dienststelle Informatik  
thomas.weber@lu.ch  
Tel. 041 228 50 00

**ServiceDesk:** 041 228 69 99