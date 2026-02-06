# USERB_RULEBOOK.md (Orion – Kompaktes Regelwerk)

## 1. Einleitung & Philosophie

Orion (User_B in der Analyse) setzt die Swing Breakout Sequence (SBS) auf eine hochstrukturierte, methodische Weise um, die sich durch Präzision, Regelbewusstsein und striktes Fokus auf Marktstruktur auszeichnet. Das folgende Regelwerk fasst sämtliche beobachteten Muster, Vorgehensweisen und Abweichungen systematisch zusammen. Ziel ist es, die Essenz von Orions Trading-Ansatz replizierbar und nachvollziehbar zu machen.

**Kernprinzip:**  
_Struktur schlägt Intuition_ – Jede Trade-Entscheidung basiert auf objektiv messbaren Kriterien im Chartverlauf.

**Prägnante Alleinstellungsmerkmale:**  
- **Strikte Anwendung des SBS-Frameworks** (5+1 Schritte, siehe StoicEdge-Definition)  
- **Pivot-/Swing-Bildung nach klarer Regel** (siehe unten)  
- **Kombination von klassischen Fib-Retracements und Extensions**  
- Systematische visuelle Kennzeichnung (Farbsystem, „blaue Linien“ für Struktur, grüner Entry etc.)  
- Fokus auf Top-Down-Multi-Zeitebenen (MTF)

---

## 2. SBS Pattern (Orion-spezifisch)

Orion nutzt die SBS-Logik (Swing Breakout Sequence) in allen Märkten und Zeiteinheiten nach dem folgenden Schema:

1. Break of Structure (BOS) durch einen starken Impuls (z.B. nach News/Opening Bell)  
2. Nach Pullback: erstes signifikantes Hoch/Tief (P1/P2)  
3. Bildung eines neuen Extremums (P3)  
4. Retracement in die 50–61.8% Zone (Fibonacci)  
5. „Sweep-Trigger-Entry“ (Reversal-Flip: Liquidität/Stopfishing, Trigger-Kerze, Entry)  
6. Rausstellung eines neues Extremums (P6: Zielbereich, i.d.R. Extension/Fib-Target)

**Orion-Akzentuierung:**  
- _Explizite Trennung zwischen „Structure-First“ (Struktur-Pivot entsteht, dann erst Orderflow) – bevorzugt!_  
- _Manche Trades MSB-First (erst Schlüsselimpuls, dann Struktur pivotiert)_

---

## 3. Pivot- und Swing-Regeln

Orion definiert Pivots/Swings folgendermaßen:

- **Standard:**  
  - Ein Peak („Pivot-Hoch“) benötigt mindestens _8–15 Bars_ (Summe Bars links und rechts).  
  - _Minimum_: Oft wurden auch Swings mit 5–7 Bars gewertet, wenn sie durch Struktur (z.B. BOS) validiert werden.  
  - _Maximum_: Bei großen Bewegungen manchmal bis zu 20+ Bars möglich.

- **Rangordnung:**  
  - _Strukturell signifikante Pivots_ schlagen zeitlich kürzere: Wenn ein BOS oder markantes Fib-Level im Spiel, darf der Pivot weniger als 8 Bars haben.  
  - Visualisierung: Orions „blaue Linien“ unterstreichen immer den _wichtigsten_ Swing, unabhängig von Zeitfenster.  
  - Nur _eindeutige_ Swings werden für SBS Phasenzählung genutzt.

_Note: Bei prägnanten Nachrichtenmoves (FOMC, Arbeitsmarkt etc.) werden die Timeframes selektiv angepasst!_

---

## 4. Structure-First vs. MSB-First

- **Structure-First:** Ideale Ordnung – Zuerst entsteht ein sauberer Pivot (markantes Hoch/Tief). Erst danach kommt der starke Impuls („Break of Structure“). Orion bevorzugt diese Variante, da sie objektiver im Backtest prüfbar ist.  
- **MSB-First:** In Ausnahmefällen (z.B. News, große Volatilität) führt der Markt zuerst einen MSB/Impulse aus, danach kristallisiert sich aus dem „Chaos“ ein neuer Pivot. Orion handelt solche Setups, ist jedoch deutlich vorsichtiger.

**Praxis:** Immer prüfen, ob ein Strukturpunkt schon „fertig“ ist, bevor man auf den Impuls reagiert!

---

## 5. Fibonacci-Anwendung bei Orion

**Kernelemente:**  
- Elliot-typische Retracements (0.5, 0.618, seltener 0.786) für Pullback-Entries  
- Extensions (1.0, 1.618, 2.0, 2.618, 4.236) zur Zielzonendefinition

**Entry-Zone:**  
- Zwischen 50 % und 61.8 % des vorherigen Expansionsimpulses (P3-P4).  
- Idealerweise Coincidenz mit markanten Strukturleveln, Orderblöcken, Vortagestiefs/-hochs, VWAP, SMA 200/20 etc.

**Target-Zone:**  
- Teilverkäufe häufig bereits bei 1.0–1.618 Extension  
- Restpositionen laufenlassen bis 2.618 oder dynamische Umkehr erkennbar

**Besonderheiten:**  
- „Geo Fib“ = geometrische Ableitung der Retracement/Extension-Flächen (optional, eher für Feintuning/Scalping)

---

## 6. Entry-Strategien

Grundsätzlich wird jeder Entry systematisch bewertet nach dem „Sweep → Trigger → Entry“-Schema:

1. **Sweep:** Liquidity-Grabbing unter/über einem lokalen Extrem (oft P2, seltener P4)  
2. **Trigger:** Bullische oder bärische Reversal-Kerze im Entrybereich  
3. **Entry:** Orderauslösung mit vorher definiertem Risiko (häufig Stopp unter/über „Sweep“-Level oder Strukturtief/-hoch)

**Risk-Management:**  
- Meist initial Risk ca. 0,25–0,33 % (Relation zum Gesamtkapital)  
- Stopp nach Partial-Take auf Break-Even (Aggressive Variante)  
- Target immer nach Extension, aber mit variabler Ausstiegsstrategie

**Beispiel: 9.3RR-Trade:**  
- Einstieg bei 0.618 Retracement, Stopp ≤ T1 (Origin)  
- Erstes Teilziel (TP1) = High/Low der Expansion, Rest laufen lassen bis Extension

---

## 7. Multi-TF Kombination (Top-Down-Prinzip)

- Analyse beginnt stets im höheren Timeframe (z.B. 1h/4h/Day), um Hauptstruktur und Range, übergeordnete Liquidity-Targets, Sweep-Potentiale und Key-Zonen zu bestimmen.  
- Entry-Trigger auf „subjektiv optimalem“ Intraday-Chart – meist 5min, 1min oder 15sek.  
- **Downfilter:** Entry nur, wenn das Setup sowohl im Small- als auch im Big-Picture logisch und strukturell sauber eingebettet ist.  
- Zwischen den Zeitebenen werden Farben und Linien konsequent zugeordnet, um Visibilität von Struktur, Entry und Target-Zonen zu maximieren (Orions legendäres Farbsystem im TradingView-Style).

---

## 8. Orion's visuelles System: Farben und Linien

- **Struktur:** Dicke, kräftig-blaue Linien (meist für Swings/Pivots/BOS)  
- **Entry-Zonen (Fib, OB etc.):** Grüne Box/Zone  
- **Stop-Loss:** Dünne rote horizontale Linie unter bzw. über Extrempunkten  
- **Teilziele:** Orange/gelbe Markierung für TP1, TP2 etc.  
- **Final Target/Extension:** Lila oder pink  
- **Multitimeframe-Kontext:** Zonen aus höherem TF stärker ausgeprägt dargestellt, Lower-TF wird nie mit Overlays „überdeckt“

---

## 9. Pattern-Variationen (Orion)

- **Standard-SBS:** Siehe Block I  
- **Geo-Fib Variation:** Zusätzliche Fibonacci-Clusters projiziert, um Entry/Exit punktgenauer zu machen (z.B. 0.702 Retracement, 1.272 Extension)  
- **Double/Triple-Sweep:** Nach BOS werden erst zwei-/dreimal Lows (Longs) oder Highs (Shorts) „gesweept“, erst dann Trigger/Entry  
- **Event-Timed SBS:** Setups, bei denen Entry/Explosion zeitlich mit z.B. Opening Bell, News-Release oder Marktschluss zusammenfallen – Risiko und Reward meist erhöht

---

## 10. Checkliste: Vor jedem Trade

1. Strukturelles Setup im Big-Picture vorhanden?  
2. Pivot-Bedingungen erfüllt (8+ Bars etc.)?  
3. BOS mit Volumen und Orderflow bestärkt?  
4. Fib-Level sauber markiert?  
5. Entry-Zone stimmt (Sweep-Trigger-Entry-Logik)?  
6. Chancen-/Risikoverhältnis angemessen (>2,5:1)?  
7. SMA/MAs, VWAP, Orderblock berücksichtigt?  
8. Support/Resistance von höherem TF einbezogen?  
9. Visual Setup klar (Farben/Linien stimmen)?  
10. Dokumentation & Screenshot für Auswertung erstellt?

---

## 11. Unterschied User_A und User_B

- **User_A:** Tendenziell intuitiver, experimentiert teils mit aggressiverem Entry, verlässt sich stärker auf Patternwiederholung und Gefühl für Marktfluss.  
- **User_B (Orion):** Strikt regelbasiert, alle Entries/Exits konsequent nach System, alles ist im Chart nachvollziehbar markiert und lückenlos dokumentiert. Klare Regel-Abweichungen sind die Ausnahme und werden mit Begründung vermerkt.