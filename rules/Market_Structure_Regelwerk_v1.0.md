# Market Structure Regelwerk — Version 1.0

> Grundlage für den Market Structure Indikator als Basis für SBS (Swing Breakout Sequence)
> Erarbeitet: Februar 2026

---

## 1. Grundprinzipien

**Fraktalität:** Market Structure Regeln gelten identisch in allen Timeframes. TF ändert Granularität, nicht die Regel.

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

---

## 5. UMO — Unmitigated Move Origin

**Bullish UMO:** Letzte Abwärtsbewegung bevor Preis nach oben bricht → aktive Kaufzone.

**Bearish UMO:** Letzte Aufwärtsbewegung bevor Preis nach unten bricht → aktive Verkaufszone.

**Unmitigated:** Preis noch nicht zur Zone zurückgekehrt → Zone bleibt aktiv als POI.

**Mitigated:** Preis kehrt zur Zone zurück → UMO verliert Primärfunktion.

**Invalidierter UMO:** Bearish UMO der invalidiert wird → wird zu Support. Bullish UMO der invalidiert wird → wird zu Resistance.

**P3 als UMO:** Bleibt aktiv als Protected Low UND UMO bis aktiv gebrochen — auch wenn übergeordnet bereits Short läuft.

---

## 6. Fibonacci

**Bezugspunkte:** Aktuelles Swingpoint-Paar Px (Protected Low) → Py (Protected High).

**Discount Zone (Long):** Preis > 50% Fib → günstig, kaufen.

**Premium Zone (Short):** Preis < 50% Fib → teuer, verkaufen.

**Golden Zone:** 61,8% — stärkster POI innerhalb Discount/Premium.

---

## 7. Range-Definition

Range liegt vor wenn Preis zwischen Px/Py keine neuen Higher Highs oder Lower Lows produziert — alle Pivots sind X-Pivots.

**Indikator-Status:** R (Range) — kein direktionales Signal.

> **WL-3:** Mindest-Bounce-Anzahl für Range-Bestätigung → späterer Input-Parameter.

---

## 8. TF-Hierarchie

### Ebene 1 — POI Filter (immer Vorperiode!)

| TF | Priorität | Elemente |
|----|-----------|----------|
| Monthly | Höchste | H, L, C |
| Weekly | Hoch | H, L, C |
| Daily | Einstieg | H, L, C |

**Bedingung:** Erst wenn Preis eine POI-Zone erreicht → Setup wird aktiv geprüft.

**Überlappung:** Mehrere TF-POIs in gleicher Zone = stärkster POI = höchste Conviction.

### Ebene 2 — HTF Market Structure

1H → Trend, BOS, UMO, Protected High/Low, Order Flow Richtung.

### Ebene 3 — LTF Entry (identische Regeln wie HTF — fraktal!)

15m, 5m, 1m → Entry-Präzisierung.

> **WL-2:** LTF Kombinations-Signale (z.B. 15m + 5m Alignment) → spätere Verfeinerung.

---

## 9. Entry-Logik

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

## 10. Multi-TF Konflikt

Aktuellste Struktur im aktiven TF = primäres Signal.

Höhere TF = Kontext und Warnung — kein Override.

Beispiel: P6/P5 Short kann Korrektur eines übergeordneten Long sein → Indikator zeigt TF-Konflikt an.

---

## Entscheidungsbaum

```
M/Wk/D POI erreicht?
    └─ Nein → kein Setup
    └─ Ja → 1H prüfen
              └─ BOS + UMO + Discount bestätigt?
                    └─ Nein → warten
                    └─ Ja → LTF Entry suchen
                              └─ RR 1:1 bei 23,6% erfüllt?
                                    └─ Nein → verwerfen
                                    └─ Ja → Limit Order platzieren
```

---

## Watch-List

| ID | Thema |
|----|-------|
| WL-1 | Gap/Imbalance innerhalb UMO — Pflicht oder optional für Indikator? |
| WL-2 | LTF Kombinations-Signale (15m + 5m Alignment) |
| WL-3 | Min. Bounce-Anzahl für Range-Bestätigung → Input-Parameter |

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
