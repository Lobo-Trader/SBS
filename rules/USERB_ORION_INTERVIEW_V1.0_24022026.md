# ORION INTERVIEW – 24.02.2026
## Fallbeispiel-Analyse: SBS Long Setup NQ

*Gesprächspartner: Orion (User_B) · Dokumentiert von: Wolfgang · Analyse: Nova (Claude)*  
*Status: Rohdokument – Charts werden manuell eingefügt*

---

## TEIL 1: ORIONS TOP-DOWN-PROZESS (Original-Aussagen)

### 1H Chart – Move Origins

> *"When I get to the charts, I look at the 1 hour chart first. I look for my move origins."*

**→ CHART EINFÜGEN: 1H Chart ohne Markierungen**

> *"Here I look at the move origins on this chart."*

**→ CHART EINFÜGEN: 1H Chart mit grauen Move Origin Zonen**

---

### 5min Chart – Richtungsentscheidung

> *"For me, I have 2 options. Short or long. I can see a 5min short SBS possibility."*

**→ CHART EINFÜGEN: 5min Chart Short SBS Möglichkeit**

> *"The long SBS is this. I need to enter within the 1hour move origins."*

**→ CHART EINFÜGEN: 5min Chart Long SBS Setup markiert**

---

### Entry-Filter: 1H Move Origin als harte Grenze

> *"I won't enter outside of them, because I don't know where price wants to go exactly and I like to know my risk and I like risk to be as small as I can."*

> *"After the bell, price dropped, never entered the higher 1hr move origin. So I look for my long SBS setup."*

---

### Frühe Chart-Markierung (Pre-Entry)

> *"I drew all of this on the chart at 8am EST when 3 was visible but not 4 nor 5."*

> *"I see my 1 and 2 within the move origin that look good. Now I need to find my entry."*

---

### 5min Move Origin (blaue Linie) – P5 Zielzone

> *"This blue line is the 5min move origin within the 1hour move origin there. This is where I wanted to see price tap and hold."*

**→ CHART EINFÜGEN: 5min Chart mit blauer Move Origin Linie**

---

### P4-Definition

> *"4 is formed as soon as it goes lower than 2."*

**→ Mechanisch:** P4 ist kein Swing im klassischen Sinne – es reicht ein einziger Tick unter P2. Sobald Preis P2 unterschreitet, ist P4 definiert. Keine Mindestanzahl an Bars erforderlich.

---

### Entry-Strategie und P5-Logik

> *"Most cases I will place a limit order at that blue line. But with PDL just below it, I wasn't sure if it was going to retest it, which would have stopped me out. My stop was only 27 points. So I waited for it to hold and then entered on a buy stop order."*

> *"5 doesn't have to take out 4 in the SBS sequence. But I prefer it to. Doesn't matter to me how much it sweeps it by but I prefer it to go lower. The only reason for this is risk. Risk is the game. Profit is just a byproduct of the process. Minimize the risk as much as possible."*

> *"Backtesting, I have found that I like to have 5 sweep 4. It doesn't always, but when it does it gives it a strong setup and minimizes my risk."*

> *"An entry on 5 gets me closer to my stop loss than entering on 4 does. I don't need to wait for any pattern for it. Just want to get a sweep of 4."*

---

### Kernphilosophie – Move Origins als primärer Filter

> *"The 1hour move origins are the most important to me for my strategy. I don't like to participate in price unless price has reached those zones. If I find a great setup I can sometimes enter in between those zones and target the move origin, but those are not my preferred setups as the moves are smaller and with the origins, I know where my stop is 100% of the time."*

---

## TEIL 2: MECHANISCHE BESCHREIBUNG (Nova-Analyse)

### Schritt 1 – 1H Chart: Move Origins definieren
Orion beginnt **immer** auf dem 1H Chart. Er identifiziert dort "Move Origins" – Zonen, die als Startpunkte vorheriger impulsiver Bewegungen dienen (graue Boxen im Chart). Diese Zonen sind sein primärer Rahmen. Außerhalb dieser Zonen nimmt er grundsätzlich **nicht** am Markt teil.

**Ausnahme:** Bei sehr klarem Setup ist Einstieg zwischen den Zonen möglich – aber nur mit Move Origin als Target (kleinerer Move, kein bevorzugtes Setup).

---

### Schritt 2 – 5min Chart: Richtung und SBS-Setup wählen
Auf dem 5min Chart prüft Orion **beide Richtungen** (Long UND Short SBS) als gleichwertige Optionen. Er wählt das Setup, das sich **innerhalb** der 1H Move Origin befindet. P1–P3 werden **bereits um 8 Uhr EST** markiert – also vor P4 und P5.

---

### Schritt 3 – 5min Move Origin (blaue Linie): Präziser Entry-Level
Innerhalb der 1H Move Origin Zone definiert Orion eine engere **5min Move Origin** (blaue Linie). Das ist die Zone, in der er P5 erwartet und in der sein Entry liegt.

---

### Schritt 4 – Entry-Entscheidung (kontextabhängig)

| Situation | Entry-Typ |
|---|---|
| Normalfall | Limit-Order direkt an der blauen Linie (5min Move Origin) |
| Kritisches Level darunter (z.B. PDL) | Warten auf Bestätigung → dann Buy-Stop-Order |

**Regel:** Wenn ein signifikantes Level (PDL, PWL, Session-Level) knapp **unterhalb** des geplanten Entry liegt, kein blindes Limit – stattdessen auf Bestätigung warten.

---

### Schritt 5 – P4 und P5 Logik

**P4-Definition:**
- P4 ist gebildet sobald Preis **einen Tick unter P2** fällt (Long-Setup)
- Kein Mindest-Bar-Kriterium – rein preisbasiert

**P5-Präferenz (Backtesting-basiert):**
- P5 muss P4 **nicht** zwingend unterbieten, wird aber **stark bevorzugt**
- Backtesting-Erkenntnis: P5 sweept P4 → stärkeres Setup + kleineres Risiko
- Je tiefer P5 unter P4, desto **näher am Stop** = kleineres Risiko
- Stop liegt immer **jenseits der Move Origin** (5min Move Origin als Grenze)
- In diesem Beispiel: **27 Punkte Stop** (NQ)
- Kein Warten auf Candlestick-Pattern – nur Sweep von P4 genügt

---

## TEIL 3: NOVA-REFLEXION – Was möglicherweise übersehen wurde

### 1. "Move Origin" ≠ UMO im aktuellen Rulebook
Der Begriff UMO (Unmitigated Order) im USERB_RULEBOOK ist konzeptuell **verwandt, aber nicht identisch** mit Orions "Move Origin". Ein Move Origin ist der **Startpunkt einer impulsiven Bewegung** – ein institutioneller Bereich, von dem aus Preis zuletzt stark accelerierte. Das sollte im Rulebook präziser differenziert werden.

### 2. Harte Regel fehlt: "Kein Trade außerhalb 1H Move Origin"
Dies ist Orions **wichtigste Einzelregel** – und sie fehlt als expliziter mechanischer Filter im Rulebook. Die Formulierung sollte lauten:  
*"Kein Trade-Einstieg, wenn Preis nicht innerhalb einer 1H Move Origin Zone ist."*

### 3. Doppelte Move Origin Hierarchie (1H + 5min)
Orion nutzt **zwei übereinanderliegende Move Origins**: die 1H Zone als Makro-Filter und die 5min Linie als präzisen Entry-Level. Diese Hierarchie ist im Rulebook bisher nicht beschrieben.

### 4. Frühzeitige Chart-Markierung als fester Prozessschritt
P1–P3 werden um **8 Uhr EST** markiert – das ist ein fester Pre-Market-Routine-Schritt, kein reaktives Vorgehen. Das hat Implikationen für Backtesting (Markierung muss zu diesem Zeitpunkt möglich gewesen sein).

### 5. Kontextabhängige Entry-Wahl als Regel
Die Umschaltlogik Limit → Buy-Stop ist klar definiert: **Wenn relevantes Level knapp unterhalb des geplanten Entry → kein Limit, auf Bestätigung warten.** Das ist eine eigene Entscheidungsregel, keine Ausnahme.

### 6. P5-Philosophie: Risk First, Pattern Second
Orions P5-Logik ist primär **risikogetrieben**, nicht strukturgetrieben. Er wartet nicht auf ein Pattern, sondern nur auf den Sweep von P4 – weil jeder Tick tiefer seinen Stop kleiner macht. Das ist ein wichtiger Unterschied zur üblichen SBS-Logik.

### 7. "Risk is the game. Profit is just a byproduct."
Diese Aussage ist nicht nur Philosophie – sie hat direkte Auswirkungen auf Regeldesign: Jede Regel bei Orion lässt sich auf **Risikoreduktion** zurückführen, nicht auf Gewinnmaximierung. Das sollte als Leitmotiv explizit im Rulebook stehen.

---

## OFFENE FRAGEN FÜR FOLGE-INTERVIEW (optional)

1. Wie definiert Orion eine Move Origin **exakt** – welches Candlemuster / welcher Mindestimpuls macht eine Zone zur Move Origin?
2. Wie viele Move Origins hat er typischerweise auf dem 1H Chart gleichzeitig aktiv?
3. Gibt es Ablaufdaten für Move Origins – wann verliert eine Zone ihre Gültigkeit?
4. Wie geht er vor, wenn mehrere Move Origins auf demselben Level liegen (1H und 5min konvergent)?
5. Nutzt er ausschließlich NQ oder auch andere Instrumente?

---

*ORION_INTERVIEW_24022026.md · Wolfgang · Nova (Claude) · Februar 2026*  
*Nächster Schritt: Sichtung alter Charts aus dem Repo → Abgleich mit neuem Wissen*
