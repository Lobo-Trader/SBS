# Standard-SBS1-Pattern – Zeit- und Preisverhältnisse (mit Varianzen)

Dieses Regelwerk beschreibt das klassische SBS1-Muster in Markttechnik, inklusive empirisch gemessener Durchschnittswerte und deren Varianzen (Standardabweichung/Sigma), basierend auf den bisherigen Repo-Auswertungen (UserA, UserB, UserD).

---

## Schritt-für-Schritt Ablauf

1. **P0 (Voringerschwingung/swing low/high)**  
   - Referenzpunkt, von dem der erste Impuls ausgeht.

2. **MSB (Market Structure Break)**  
   - MSB entsteht typischerweise nach _X1_ Bars ab P0  
   - _Zahl empirisch für den Start nicht explizit erfasst._

3. **Punkt 1 (P1)**
   - P1 entsteht im Schnitt nach **2.5–3.2 Bars** (links/rechts) nach dem MSB  
     - UserA: 2.57/2.71 (σ 0.50/0.65)
     - UserD: 3.2/3.7 (σ 0.9/0.8)
   - **P1 liegt im Schnitt** **x %** über dem MSB  
     - Wert x% im Repo textlich als "über prev. High" angegeben, präzise % noch zu ergänzen.
   - _Varianz_: ±0.5 bis ±0.9 Bars je nach User
   - _Kommentar_: P1 bestätigt das Breakout-Level.

4. **Punkt 2 (P2)**
   - P2 folgt durchschnittlich **2.1–2.9 Bars** nach P1  
     - UserA: 2.14/2.71 (σ 0.68/0.76)
     - UserB: 1.89/2.32 (σ 0.44)
     - UserD: 2.4/2.9 (σ 1.2/1.1)
   - **P2 liegt** im Schnitt bei **41,7%** (σ 11.2%) der Distanz P0→P1 (UserB; oft niedrigster Wert im unteren Drittel der Swing-Range)
   - _Varianz_: ±0.7 bis ±1.2 Bars; Wert kann 27–61% der Spanne annehmen
   - _Kommentar_: P2 ist das markante Pullback-Low nach P1.

5. **Punkt 3 (P3)**
   - P3 entsteht **after 2.0–3.2 Bars** nach P2  
     - UserA: 2.85/3.29 (σ 0.56/0.78)
     - UserB: 2.05/1.87 (σ 0.39)
     - UserD: 2.9/3.1 (σ 1.0/1.2)
   - **P3 liegt typischerweise x% über P1**, Wert variiert je nach Volatilität (im Repo als "höher als Punkt 1“)
   - _Varianz_: ±0.4 bis ±1.2 Bars
   - _Kommentar_: Der wichtige „Sweep“-Impuls, ggf. mit Liquiditätsjagd.

6. **Punkt 4 (P4)**
   - P4 tritt meist **2.5–3.3 Bars** nach P3 auf  
     - UserA: 2.57/3.14 (σ 0.52/0.86)
     - UserD: 3.3/2.7 (σ 0.8/1.2)
   - **P4 liegt im Bereich von ca. 65–90%** Retracement von P3 (oft unter P2)  
   - _Varianz_: ±0.5 bis ±1.2 Bars
   - _Kommentar_: Geduldsphase, noch kein Entry! Manchmal Konsolidierung/W-Formation.

7. **Punkt 5 (P5)**
   - P5 folgt im Mittel **1.5–2.4 Bars** nach P4  
     - UserA: 1.57/2.00 (σ 0.49/0.30)
     - UserD: 2.1/2.4 (σ 1.2/0.7)
   - **P5 tritt** typischerweise im Bereich von **61,8–75%** Fibo-Retracement („goldene Zone“) auf.
   - _Varianz_: ±0.3 bis ±1.2 Bars
   - _Kommentar_: Das ist der eigentliche Entry, oft nach W-Formation.

8. **Ausbruch zu neuem Hoch ("Post-P5 Rally")**
   - Nach P5 erfolgt in der Regel der deutliche Ausbruch über P3 hinaus
   - Entry/Exit-Zonen, SL & TP werden anhand der vorherigen Fibo‐ und Pivot-Level gemessen.

---

## Übersicht – Pivot-Bar-Abstände & Varianz (σ) je User

| Pivot | UserA (Avg, σ)   | UserB (Avg, σ)     | UserD (Avg, σ)   |
|-------|------------------|--------------------|------------------|
| P1    | 2.57/2.71, 0.50/0.65 | —                | 3.2/3.7, 0.9/0.8 |
| P2    | 2.14/2.71, 0.68/0.76 | 1.89/2.32, 0.44  | 2.4/2.9, 1.2/1.1 |
| P3    | 2.85/3.29, 0.56/0.78 | 2.05/1.87, 0.39  | 2.9/3.1, 1.0/1.2 |
| P4    | 2.57/3.14, 0.52/0.86 | —                | 3.3/2.7, 0.8/1.2 |
| P5    | 1.57/2.00, 0.49/0.30 | —                | 2.1/2.4, 1.2/0.7 |

## Übersicht – Preisrelationen (SBS1-Basismuster)

- **MSB:**
  - Bricht das vorherige High/Low (i. d. R. ca. 23,6% Move)
- **P1:**
  - x% über MSB (konkrete empirische % steht in der Analyse noch aus)
- **P2:**
  - 41,7% (σ 11.2%) der P0→P1-Strecke, min/max ca. 27–61%
- **P4:** 
  - 65–90% Retracement von P3
- **P5:**
  - 61,8–75% Fibo-Level, eigentliche Entry-Zone

## Typische Abweichungen (Varianz)

- **Abstands-Bars (alle Pivots):** Schwanken je nach Pattern und User ungef. ±0.3 bis ±1.2 Bars
- **Positionsprozent P2:** ca. 41,7% ±11,2% (UserB)
- **SBS bleibt adaptiv:** Einzelmärkte, Timeframes und User unterscheiden sich statistisch etwas – extremwerte („Overshoot", „Mini-Pivot") gibt es <10–15% der Fälle.

---

## Zielformat für Indikator/Code

Die o. g. Mittelwerte und Abweichungen können als Richt- und Toleranzwerte für die automatische Erkennung eines SBS1-Musters genutzt werden.  
**Eine Kodierung könnte wie folgt arbeiten:**  
- Pivot-Treffer akzeptieren, wenn sie ±Sigma um den Mittelwert liegen.
- Entry-Vorschläge generieren, falls MSB, P1–P5 in Zeit-/Preisrelationen und Varianz passen.

---

*Alle Werte sind auf Basis von Repo-Statistiken (Stand Feb 2026, UserA, B, D). Die Spanne kann bei weiterem Dateninput noch feiner justiert werden.*