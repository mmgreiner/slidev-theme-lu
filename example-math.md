---
theme: ./
title: Finanzmathematik
subtitle: Zinsrechnung und Investitionen
author: Dr. Andreas Fischer
date: 28. Januar 2026
department: Finanzdepartement
website: https://www.lu.ch
layout: cover
---

# Finanzmathematik

Zinsrechnung und Investitionen

---
layout: default
---

# Zinseszinsrechnung

## Grundformel

Das Endkapital $K_n$ nach $n$ Jahren bei anfänglichem Kapital $K_0$ und Zinssatz $p$ berechnet sich:

$$
K_n = K_0 \cdot \left(1 + \frac{p}{100}\right)^n
$$

## Beispiel

Bei einer Investition von **CHF 100'000** zu **2.5% Jahreszins** über **10 Jahre**:

$$
K_{10} = 100'000 \cdot \left(1 + \frac{2.5}{100}\right)^{10} = 100'000 \cdot 1.025^{10}
$$

$$
K_{10} = 100'000 \cdot 1.2801 = \textbf{CHF 128'010}
$$

<div class="info-box info">
  <div class="info-icon">💡</div>
  <div class="info-content">
    <p><strong>Interpretation:</strong> Nach 10 Jahren hat sich das Kapital um <strong>CHF 28'010</strong> (28.01%) erhöht.</p>
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
</style>

---
layout: two-cols
---

::left::

## Barwert-Berechnung

Der **heutige Wert** einer zukünftigen Zahlung:

$$
PV = \frac{FV}{(1 + i)^n}
$$

**Legende:**
- $PV$ = Present Value (Barwert)
- $FV$ = Future Value (Zukunftswert)
- $i$ = Zinssatz (dezimal)
- $n$ = Anzahl Perioden

## Beispiel

Wie viel ist eine Zahlung von **CHF 50'000** in **5 Jahren** heute wert? (Zinssatz: 3%)

$$
PV = \frac{50'000}{(1 + 0.03)^5} = \frac{50'000}{1.159} = \textbf{CHF 43'136}
$$

::right::

## Annuitätenrechnung

Regelmässige Zahlung bei konstantem Zins:

$$
A = K_0 \cdot \frac{i \cdot (1+i)^n}{(1+i)^n - 1}
$$

**Legende:**
- $A$ = Annuität (jährliche Zahlung)
- $K_0$ = Darlehensbetrag
- $i$ = Zinssatz
- $n$ = Laufzeit

## Beispiel: Darlehen

Kredit von **CHF 200'000** über **20 Jahre** zu **2%**:

$$
A = 200'000 \cdot \frac{0.02 \cdot 1.02^{20}}{1.02^{20} - 1}
$$

$$
A = 200'000 \cdot 0.0612 = \textbf{CHF 12'240/Jahr}
$$