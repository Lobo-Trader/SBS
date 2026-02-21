# Market Structure Regelwerk — Version 1.1

> Grundlage für den Market Structure Indikator als Basis für SBS (Swing Breakout Sequence)
> v1.0: Februar 2026 | v1.1: Februar 2026 — Chart-Validierung NQ Monthly/Weekly/Daily/1H/15m

---

## Das Universalprinzip

> **Kaufe niedrig — verkaufe hoch.**
> Finde Protected High & Low → spanne Fib → kaufe bei 50%/61,8% (Discount) → verkaufe bei 50%/61,8% (Premium).
> Gilt auf **jedem TF**. **Immer wieder.** Keine Ausnahmen.

Diese Technik ist die Grundlage für SBS und viele andere Strategien. Es geht IMMER darum, die **relevanten** Highs und Lows zu kennen.

---

## 1. Grundprinzipien

**Fraktalität:** Market Structure Regeln gelten identisch in allen Timeframes. TF ändert Granularität, nicht die Regel. Validiert auf Monthly, Weekly, Daily, 1H, 15m. ✅

**Zeitliche Sequenz:** Signale sind nur valide wenn sie in Echtzeit bestätigbar sind — kein Repainting. Protected Highs/Lows und UMOs werden immer erst **rückwirkend durch den Bruch** bestätigt.

**BOS-Bestätigung:** Input Variable, Default = **Close** über/unter dem Strukturpunkt.

---

## 2. Pivot-Definition

**Minimum:** 3 abgeschlossene Bars im jeweiligen TF.

**Pivot Low:** Muster HL/LL/HL — mittlerer Bar ist das Low.

**Pivot High:** Muster LH/HH/LH — mittlerer Bar ist das High.

**Klassifizierung:** Immer relativ zum vorherigen relevanten Swingpoint Px — nicht absolut.

**Signifikanz** (Anzahl Bars drumherum): In diesem Projekt sekundär — Preis-Level relativ zu Px ist entscheidend. In anderen Anwendungen (z.B. Extrempunkte suchen) kann Signifikanz zur primären Priorität werden.

---

## 3. X-Pivot Filter

Pivots die **innerhalb der aktuellen Fib-Extreme** (zwischen aktivem Px/Py) liegen werden ignoriert — sie sind **X-Pivots** und keine validen Strukturpunkte.

Filter ist dynamisch — aktualisiert sich mit jedem neuen Swingpoint-Paar.

---

## 4. Order Flow & Protected Highs/Lows

**Bullish Order Flow:**
P2 High → erzeugt P3 Low → Preis steigt und bricht P2 in P4 → **erst durch diesen Bruch** wird P3 zum **Protected Low** ✅

**Bearish Order Flow:**
P7 Low → erzeugt P6 High → Preis fällt und bricht P7 in P8 → **erst durch diesen Bruch** wird P6 zum **Protected High** ✅

**Invalidierung:** Bullish Order Flow wird invalidiert wenn Protected Low nach unten gebrochen wird — und umgekehrt.

### Potential vs. Confirmed (NEU v1.1)

**Potential Protected Low/High** = vorläufige Markierung sobald ein neues Hoch/Tief entsteht.

**Confirmed Protected Low/High** = erst bestätigt durch den nachfolgenden BOS.

Indikator-Darstellung: Potential = gestrichelte Linie / Confirmed = durchgezogene Linie.

### Zykluswechsel (NEU v1.1)

Ein Bullisher Zyklus wechselt zu Bearish **erst wenn** das Protected Low der aktuellen Bullish-Struktur gebrochen wird — und vice versa. Ein "zu tiefes Retracement" allein reicht nicht — es braucht den bestätigten Bruch.

---

## 5. UMO — Unmitigated Move Origin

**Bullish UMO:** Letzte Abwärtsbewegung bevor Preis nach oben bricht → aktive Kaufzone.

**Bearish UMO:** Letzte Aufwärtsbewegung bevor Preis nach unten bricht → aktive Verkaufszone.

**Unmitigated:** Preis noch nicht zur Zone zurückgekehrt → Zone bleibt aktiv als POI.

**Mitigated:** Preis kehrt zur Zone zurück → UMO verliert Primärfunktion. Ein **Wick** in die Zone reicht zur Mitigation — der Preis "war da", wartende Orders wurden wahrscheinlich ausgeführt.

**Mitigation Statistik:** Erster Retest = hohe Zuverlässigkeit für Fortsetzung. Zweiter Retest = deutlich unsicherer.

**Invalidierter UMO:** Bearish UMO der invalidiert wird → wird zu Support. Bullish UMO der invalidiert wird → wird zu Resistance.

**P3 als UMO:** Bleibt aktiv als Protected Low UND UMO bis aktiv gebrochen — auch wenn übergeordnet bereits Short läuft.

---

## 6. Fibonacci & Golden Fib Rule

**Bezugspunkte:** Aktuelles Swingpoint-Paar Px (Protected Low) → Py (Protected High).

**Discount Zone (Long):** Preis > 50% Fib → günstig, kaufen.

**Premium Zone (Short):** Preis < 50% Fib → teuer, verkaufen.

**Golden Zone:** 61,8% — stärkster POI innerhalb Discount/Premium.

### Golden Fib Rule (NEU v1.1 — validiert auf M/Wk/D/1H/15m)

Nach jedem BOS (neues High gebrochen) → **erwarte Retracement zur 50%/61,8% Zone** → dort ist der primäre Entry. Nicht dem Ausbruch hinterherlaufen!

### Anti-FOMO 50/61,8 Regel (NEU v1.1)

> Kein Entry am High — **immer warten auf 50% oder 61,8% Retracement.**
> Gilt auf allen TF. Keine Ausnahmen. Kein FOMO. 🎯

Solange Preis nicht im Discount ist → kein grünes Signal. Der Indikator ist der Disziplin-Partner.

---

## 7. Zonen-Relevanz & Alterung (NEU v1.1)

Zonen-Relevanz ist dynamisch und nimmt ab mit:

| Faktor | Richtung | Relevanz |
|--------|----------|----------|
| Alter der Zone | älter | abnehmen |
| TF der Zone | kleiner | abnehmen |
| Alter der Zone | jünger | zunehmen |
| TF der Zone | höher | zunehmen |

**Goldene Regel:** Je jünger + je höher TF = stärkste Zone. Je älter + je kleiner TF = schwächste Zone.

**Memory-Effekt:** Besonders bei Support-Zonen bleibt ein Gedächtnis des Marktes bestehen — auch ältere Zonen können noch reagieren, aber mit abnehmender Zuverlässigkeit.

**Alte Zonen:** Werden nicht gelöscht — bleiben sichtbar aber de-priorisiert (visuell z.B. durch Transparenz/Farbe).

> **WL-5:** Alterungs-Algorithmus → wie modellieren wir Relevanz-Abnahme im Code? Optionen: Anzahl Bars seit Entstehung, Anzahl verpasster Retests, oder manuell per Input?

---

## 8. Confluence (NEU v1.1)

Überlappung alter und neuer Zonen = **Confluence** = erhöhte Zuverlässigkeit des POI.

Je mehr Zonen sich überlappen, desto stärker der POI.

Mehrere übereinanderliegende historische Zonen = **Confluence Zone = stärkster POI.**

> **WL-6:** Confluence-Visualisierung → Farbintensität als Stärkeanzeige?

---

## 9. Fallback-Zonen bei Strukturbruch (NEU v1.1)

Bricht ein Protected Low/High → ist das nächste aktive HTF S/R Level die Zielzone für den Rücksetzer.

Beispiel: Weekly Protected Low bricht → nächste aktive Monthly Zone ist das Ziel.

Die TF-Ebenen sind nicht unabhängig — sie greifen ineinander als **Sicherheitsnetz.**

> **WL-7:** Fallback-Zonen Visualisierung bei Strukturbruch als Indikator-Feature.

---

## 10. Range-Definition

Range liegt vor wenn Preis zwischen Px/Py keine neuen Higher Highs oder Lower Lows produziert — alle Pivots sind X-Pivots.

**Indikator-Status:** R (Range) — kein direktionales Signal.

> **WL-3:** Mindest-Bounce-Anzahl für Range-Bestätigung → späterer Input-Parameter.

---

## 11. TF-Hierarchie

### Ebene 1 — POI Filter (immer Vorperiode!)

| TF | Priorität | Elemente |
|----|-----------|----------|
| Monthly | Höchste | H, L, C |
| Weekly | Hoch | H, L, C |
| Daily | Einstieg | H, L, C |

**Bedingung:** Erst wenn Preis eine POI-Zone erreicht → Setup wird aktiv geprüft.

**Priorität bei Überlappung:** Monthly > Weekly > Daily.

**Confluence:** Mehrere TF-POIs in gleicher Zone = stärkster POI = höchste Conviction.

### Ebene 2 — HTF Market Structure
1H → Trend, BOS, UMO, Protected High/Low, Order Flow Richtung.

### Ebene 3 — LTF Entry (identische Regeln wie HTF — fraktal!)
15m, 5m, 1m → Entry-Präzisierung. Dieselbe Logik, feinere Granularität → besserer Entry-Preis → besseres RR.

> **WL-2:** LTF Kombinations-Signale (z.B. 15m + 5m Alignment) → spätere Verfeinerung.

---

## 12. Entry-Logik

**Voraussetzung:** POI Ebene 1 erreicht + HTF BOS + UMO + Discount Zone bestätigt.

**Long Entry:** Limit Order bei 50% oder 61,8% Fib.

**Short Entry:** Limit Order bei 50% oder 61,8% Fib (spiegelverkehrt).

**Stop Loss:** Unter/über Fib-Ursprung (Protected Low/High).

**Mindest-RR:** 23,6% muss RR 1:1 liefern — sonst Setup verworfen.

### Exit-Strategie (3 Positionen)

| Position | Exit | Aktion |
|----------|------|--------|
| 1/3 | RR 1:1 | Kosten decken |
| 2/3 | RR 1:2 | B&B — Bread & Butter |
| 3/3 | Runner | Nächstes HTF Ziel 🍒 |

---

## 13. Multi-TF Konflikt & Ambiguity Warning (NEU v1.1)

Aktuellste Struktur im aktiven TF = primäres Signal.

Höhere TF = Kontext und Warnung — kein Override.

### Ambiguity Warning

**Bedingung:** Zwei gleichwertig plausible Szenarien wenn:
- LTF Zyklus komplett (BOS bestätigt) ✅
- HTF Zyklus noch pending (kein BOS) ⏳
- Preis befindet sich nahe HTF Protected High/Low aber noch nicht gebrochen

**Indikator-Ausgabe:**
> ⚠️ "Ambiguous Structure: [LTF] Bullish confirmed — [HTF] BOS pending. Two equally valid scenarios. Wait for confirmation."

> **WL-10:** Ambiguity Warning — weitere Auslöse-Bedingungen definieren:
> - Preis exakt auf 50% Fib (weder Discount noch Premium eindeutig)
> - Protected Low/High nur per Wick gebrochen aber kein Close (BOS Default = Close)

---

## Entscheidungsbaum

```
M/Wk/D POI erreicht?
    └─ Nein → kein Setup
    └─ Ja → HTF (1H) prüfen
              └─ BOS + UMO + Discount bestätigt?
                    └─ Nein → warten
                    └─ Ja → Ambiguity Check
                              └─ HTF pending? → ⚠️ Warning ausgeben
                              └─ LTF Entry suchen (15m/5m/1m)
                                    └─ RR 1:1 bei 23,6% erfüllt?
                                          └─ Nein → verwerfen
                                          └─ Ja → Limit Order bei 50%/61,8%
```

---

## Watch-List

| ID | Thema |
|----|-------|
| WL-1 | Gap/Imbalance innerhalb UMO — Pflicht oder optional für Indikator? |
| WL-2 | LTF Kombinations-Signale (15m + 5m Alignment) |
| WL-3 | Min. Bounce-Anzahl für Range-Bestätigung → Input-Parameter |
| WL-4 | Mitigation-Tiefe als optionaler Parameter (Wick-Grenze vs. Median der Zone) |
| WL-5 | Alterungs-Algorithmus für Zonen — Modellierung Relevanz-Abnahme |
| WL-6 | Confluence-Visualisierung — Farbintensität als Stärkeanzeige |
| WL-7 | Fallback-Zonen Visualisierung bei Strukturbruch |
| WL-8 | Potential vs. Confirmed Darstellung (gestrichelt vs. durchgezogen) |
| WL-9 | Visuelle Zyklusdarstellung (Bullish/Bearish Bögen) als optionales Display-Feature |
| WL-10 | Ambiguity Warning — weitere Auslöse-Bedingungen definieren |

---

## Abkürzungsverzeichnis

| Kürzel | Bedeutung |
|--------|-----------|
| BOS | Break of Structure |
| UMO | Unmitigated Move Origin |
| TF | Timeframe |
| HTF | Higher Timeframe |
| LTF | Lower Timeframe |
| ÜT | Übergeordneter Trend / Timeframe |
| POI | Point of Interest |
| WL | Watch-List — keine Prio für Code, regelmäßig checken |
| OF | Offene Frage (geschlossen wenn beantwortet) |
| SBS | Swing Breakout Sequence — eigenes Handelssystem, nutzt 5 klassifizierte Pivots |
| L/S/R | Long / Short / Range |
| B&B | Bread & Butter — Gewinner decken Verlusttrades |
| Runner | 3. Teilposition ohne festes TP — läuft zum nächsten HTF Ziel 🍒 |
| RR | Risk/Reward Verhältnis |
| Discount | Preisbereich > 50% Fib — kaufen |
| Premium | Preisbereich < 50% Fib — verkaufen |
| Golden Zone | Fibonacci 61,8% Level |
| SL | Stop Loss |
| TP | Take Profit |
| Px/Py | Aktuelle valide Swingpoints (nummeriert nach Entstehung) |
| X-Pivot | Pivot innerhalb Px/Py Range — wird ignoriert |
| Gap | Preislücke / Imbalance zwischen zwei Candles |
| D/Wk/M | Daily / Weekly / Monthly |
| FOMO | Fear Of Missing Out — Emotion, durch 50/61,8 Regel diszipliniert |
| Confluence | Überlappung mehrerer Zonen = stärkerer POI |
| Potential PL/PH | Vorläufiges Protected Low/High vor BOS-Bestätigung |
| Confirmed PL/PH | Bestätigtes Protected Low/High nach BOS |
