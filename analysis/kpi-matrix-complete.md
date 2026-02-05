# SBS Pattern - Complete KPI Matrix

**Version:** 1.0  
**Last Updated:** 2026-02-05 18:48:07  
**Total KPIs:** 47

---

## A) STRUKTUR-KPIs (Geometrie)

| KPI ID | Messgröße | Einheit | Beschreibung | Wichtigkeit | Status |
|--------|-----------|---------|--------------|-------------|--------|
| **S1** | MSB → Punkt 1 Distanz | % | Wie viel % über prev. High | 🔴 Kritisch | Zu messen |
| **S2** | MSB Break Stärke | % Fibo | Min 23.6% der Swing-Range? | 🔴 Kritisch | Zu messen |
| **S3** | Prev High → Punkt 2 | Pips | Abstand unter prev. High | 🟡 Medium | Zu messen |
| **S4** | Punkt 2 Retracement | % | Wie tief zieht Punkt 2 zurück (1→2)? | 🟢 Info | Zu messen |
| **S5** | Punkt 1 → Punkt 3 Distanz | % | Wie viel höher ist Punkt 3 vs Punkt 1? | 🔴 Kritisch | Zu messen |
| **S6** | Punkt 3 → Punkt 4 Retracement | % Fibo | Wo liegt Punkt 4? | 🔴 Kritisch | Zu messen |
| **S6a** | Punkt 4 vs 61.8% | Pips | Wie viel tiefer liegt P4 unter Entry? | 🔴 Kritisch | Zu messen |
| **S6b** | Punkt 4 Fibo-Level | % | Wo liegt P4 genau? (70%? 80%? 90%?) | 🔴 Kritisch | Zu messen |
| **S7** | Punkt 4 Position vs Punkt 2 | Pips | Ist Punkt 4 unter Punkt 2? | 🔴 Kritisch | Zu messen |
| **S8** | Punkt 4 vs MSB-Level | % | Abstand zu 100% Fibo | 🟡 Medium | Zu messen |
| **S9** | Entry zu MSB Abstand | % | Sicherheitspolster zum Stop | 🟡 Medium | Zu messen |

---

## B) ZEIT-KPIs (Temporal)

| KPI ID | Messgröße | Einheit | Beschreibung | Wichtigkeit | Status |
|--------|-----------|---------|--------------|-------------|--------|
| **T1** | Bars: MSB → Punkt 1 | Bars | Wie schnell wird Punkt 1 erreicht? | 🟢 Info | Zu messen |
| **T2** | Bars: Punkt 1 → Punkt 2 | Bars | Dauer des ersten Pullbacks | 🟡 Medium | Zu messen |
| **T3** | Bars: Punkt 2 → Punkt 3 | Bars | Dauer der Rally zu Punkt 3 | 🟡 Medium | Zu messen |
| **T4** | Bars: Punkt 3 → Punkt 4 | Bars | Dauer des Retracements | 🟡 Medium | Zu messen |
| **T5** | **Ratio: T4 / T3** | Faktor | "Oft mindestens gleich lang" | 🔴 Kritisch! | Zu messen |
| **T6** | Bars: Punkt 3 → unter Punkt 2 | Bars | Bestätigung von Punkt 3 | 🔴 Kritisch | Zu messen |
| **T7** | Total Pattern Duration | Bars | MSB bis Entry Signal | 🟢 Info | Zu messen |
| **T8** | T4 / T3 Verhältnis Range | Min/Max | Range: 1x bis mehrfaches | 🟡 Medium | Zu messen |

---

## C) MOMENTUM-KPIs (Dynamik)

| KPI ID | Messgröße | Einheit | Beschreibung | Wichtigkeit | Status |
|--------|-----------|---------|--------------|-------------|--------|
| **M1** | Slope 1→2 | Grad/% | Steilheit des Pullbacks | 🟢 Info | Zu messen |
| **M2** | Slope 2→3 | Grad/% | Steilheit der Rally | 🟡 Medium | Zu messen |
| **M3** | Slope 3→4 | Grad/% | Steilheit des Retracements | 🟡 Medium | Zu messen |
| **M4** | Bars ohne Retracement 2→3 | Count | Consecutive bullish bars? | 🟢 Info | Zu messen |
| **M5** | Average Bar Size 2→3 | Pips/ATR | Momentum-Indikator | 🟢 Info | Zu messen |
| **M6** | Average Bar Size 3→4 | Pips/ATR | Retracement-Stärke | 🟢 Info | Zu messen |

---

## D) PIVOT-KPIs (Swing-Struktur)

| KPI ID | Messgröße | Einheit | Beschreibung | Wichtigkeit | Status |
|--------|-----------|---------|--------------|-------------|--------|
| **P1** | Punkt 1 Pivot Strength | Bars L/R | Wie viele Bars links/rechts niedriger? | 🟡 Medium | Zu messen |
| **P2** | Punkt 2 Pivot Strength | Bars L/R | Ist es ein "echter" Pivot Low? | 🟡 Medium | Zu messen |
| **P3** | Punkt 3 Pivot Strength | Bars L/R | Wie stark ist das High? | 🟡 Medium | Zu messen |
| **P4** | Punkt 4 Pivot Strength | Bars L/R | Ist es ein klares Low? | 🟡 Medium | Zu messen |
| **P5** | Wicks at Punkt 4 | % | Rejection Wicks bei Entry-Zone? | 🟢 Info | Zu messen |

---

## E) PUNKT 5 KPIs (Post-Entry Sweep)

| KPI ID | Messgröße | Einheit | Beschreibung | Wichtigkeit | Status |
|--------|-----------|---------|--------------|-------------|--------|
| **P5-1** | Punkt 5 Existenz | Ja/Nein | Gibt es einen Punkt 5? | 🔴 Kritisch | Zu messen |
| **P5-2** | Punkt 5 Fibo-Level | % | Wo liegt P5? (70%? 80%?) | 🔴 Kritisch | Zu messen |
| **P5-3** | P5 vs P4 Distanz | Pips | Ist P5 höher als P4? | 🔴 Kritisch | Zu messen |
| **P5-4** | P5 vs Entry Distanz | Pips | Max Floating Loss | 🟡 Medium | Zu messen |
| **P5-5** | Bars: Entry → P5 | Bars | Wie schnell kommt P5? | 🟡 Medium | Zu messen |
| **P5-6** | P5 vs 100% Abstand | % | Sicherheitspuffer | 🔴 Kritisch | Zu messen |
| **P5-7** | P5 Häufigkeit | % | Wie oft tritt P5 auf? | 🔴 Kritisch | Zu messen |

---

## F) ENTRY-MANAGEMENT KPIs

| KPI ID | Messgröße | Einheit | Beschreibung | Wichtigkeit | Status |
|--------|-----------|---------|--------------|-------------|--------|
| **EM-1** | Entry Level | % Fibo | Wo erfolgte Entry? (50-61.8%) | 🔴 Kritisch | Zu messen |
| **EM-2** | Entry zu P4 | Pips | Abstand Entry → P4 | 🟡 Medium | Zu messen |
| **EM-3** | Initial R:R | Ratio | Risk:Reward bei Entry | 🔴 Kritisch | Zu messen |
| **EM-4** | Optimaler Entry | % Fibo | Was wäre bester Entry gewesen? | 🟢 Info | Zu messen |

---

## G) STOP LOSS KPIs

| KPI ID | Messgröße | Einheit | Beschreibung | Wichtigkeit | Status |
|--------|-----------|---------|--------------|-------------|--------|
| **SL-1** | Stop Placement | % Fibo | Wo liegt SL? (100% + x ATR) | 🔴 Kritisch | Zu messen |
| **SL-2** | ATR Buffer | ATR | Wie viele ATR unter 100%? | 🟡 Medium | Zu messen |
| **SL-3** | SL Hit | Ja/Nein | Wurde SL getroffen? | 🔴 Kritisch | Zu messen |
| **SL-4** | Closest Approach | Pips | Wie nah kam Preis an SL? | 🟢 Info | Zu messen |

---

## H) ERFOLGS-KPIs (Outcome)

| KPI ID | Messgröße | Einheit | Beschreibung | Wichtigkeit | Status |
|--------|-----------|---------|--------------|-------------|--------|
| **O1** | Pattern Outcome | Kategorie | SUCCESS/NO ENTRY/FAILED/PENDING | 🔴 Kritisch | Zu messen |
| **O2** | Entry Triggered | Ja/Nein | Wurde Golden Zone erreicht? | 🔴 Kritisch | Zu messen |
| **O3** | Stop Loss Hit | Ja/Nein | Wurde SL durchbrochen? | 🔴 Kritisch | Zu messen |
| **O4** | TP1 Reached (23.6%) | Ja/Nein | Erstes Target erreicht? | 🔴 Kritisch | Zu messen |
| **O5** | TP2 Reached (0%) | Ja/Nein | Punkt 3 Level erreicht? | 🟡 Medium | Zu messen |
| **O6** | Max Favorable Excursion | % | Wie weit ging es in die richtige Richtung? | 🟢 Info | Zu messen |
| **O7** | Max Adverse Excursion | % | Wie nah kam es an Stop Loss? | 🟢 Info | Zu messen |
| **O8** | R:R Ratio Realized | Faktor | Tatsächliches Risk:Reward bei Exit | 🟡 Medium | Zu messen |

---

## I) KONTEXT-KPIs (Umfeld)

| KPI ID | Messgröße | Einheit | Beschreibung | Wichtigkeit | Status |
|--------|-----------|---------|--------------|-------------|--------|
| **C1** | Timeframe | Min | 1m, 5m, 15m, 1h, etc. | 🔴 Kritisch | Zu messen |
| **C2** | Instrument | Symbol | NQ, ES, etc. | 🟢 Info | Zu messen |
| **C3** | Session | US/EU/Asia | Markt-Session | 🟢 Info | Zu messen |
| **C4** | Trend Context | Up/Down/Range | Übergeordneter Trend | 🟡 Medium | Zu messen |
| **C5** | Volatility (ATR) | Pips | Durchschnittliche Range | 🟢 Info | Zu messen |

---

## Prioritäten-Übersicht

### 🔴 Kritische KPIs (MUSS gemessen werden): 23 KPIs
S1, S2, S5, S6, S6a, S6b, S7, T5, T6, P5-1, P5-2, P5-3, P5-6, P5-7, EM-1, EM-3, SL-1, SL-3, O1, O2, O3, O4, C1

### 🟡 Medium KPIs (SOLLTE gemessen werden): 16 KPIs
S3, S4, S8, S9, T2, T3, T4, T8, M2, M3, P1, P2, P3, P4, P5-4, P5-5, EM-2, SL-2, O5, O8, C4

### 🟢 Info KPIs (KANN gemessen werden): 8 KPIs
T1, T7, M1, M4, M5, M6, P5, O6, O7, C2, C3, C5

---

## Nächste Schritte

1. ✅ Charts hochladen
2. ⏳ Für jeden Chart alle 🔴 Kritischen KPIs messen
3. ⏳ Statistiken erstellen (Median, Mean, Range, Std Dev)
4. ⏳ Regeln ableiten basierend auf Daten
5. ⏳ Expert Review
6. ⏳ Backtesting