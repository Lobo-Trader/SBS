# MS Confluence System – Konzeptdokument
**Autor:** Wolfgang (Lobo-Trader) & Nova (Claude)
**Datum:** 26.02.2026
**Version:** 1.0

---

## 1. VISION

Ein einziger TradingView-Indikator der drei Module kombiniert und automatisch auf
Trademöglichkeiten prüft. Risk first – Profit ist Byproduct (Orion-Prinzip).

---

## 2. DAS SPIELFELD – Framework Übersicht

### Grundprinzip
Der Markt wird als Spielfeld verstanden. Vor jedem Trade muss das Spielfeld
definiert sein. Kein Trade ohne Spielfeld-Kontext.

### Timeframe-Hierarchie
| TF | Rolle | Werkzeug |
|----|-------|----------|
| H1 | Spielfeld definieren – BSL/SSL als Rahmen | Modul 1 |
| M5 | Entry-Zone innerhalb H1 Zone – Risk↓ | Modul 1 |
| M1 | Bubble-Bestätigung + Signal | Modul 2 |

### Spielfeld-Typen
| Typ | Beschreibung | Aktive Seite |
|-----|-------------|-------------|
| **Trend Long** | Preis über SSL – Support aktiv | Nur SSL (unten) |
| **Trend Short** | Preis unter BSL – Resistance aktiv | Nur BSL (oben) |
| **Range** | Preis zwischen BSL und SSL | Beide Seiten |

---

## 3. DIE DREI MODULE

### Modul 1 – BSL/SSL Liquidity Zones
**Basis:** BuySellSide Liquidity v4 FINAL (Pine V6)
**Funktion:** Erkennt Pivot-Cluster als Buyside/Sellside Liquiditätszonen

**Output-Status (für Hauptprogramm):**
- `bsl_active` (bool) – BSL Zone vorhanden und aktiv
- `ssl_active` (bool) – SSL Zone vorhanden und aktiv
- `price_at_bsl` (bool) – Preis innerhalb BSL Zone
- `price_at_ssl` (bool) – Preis innerhalb SSL Zone
- `bsl_level` (float) – BSL Zonenmitte
- `ssl_level` (float) – SSL Zonenmitte
- `bsl_top` / `bsl_bot` (float) – BSL Zonengrenzen
- `ssl_top` / `ssl_bot` (float) – SSL Zonengrenzen

**TF-Logik:**
- H1 Zone = Spielfeld-Rahmen (Makro)
- M5 Zone innerhalb H1 Zone = Entry-Level (Mikro, Risk↓)

---

### Modul 2 – Delta/Volume Bubble
**Basis:** Delta/Volume Bubble [Quant Z-Score] (Pine V6, wizardry)
**Funktion:** Z-Score des Volume-Deltas, Absorption, Divergenz-Erkennung

**Output-Status (für Hauptprogramm):**
- `bubble_active` (bool) – Bubble vorhanden (≥2σ)
- `bubble_bull` (bool) – Bullisches Delta
- `bubble_bear` (bool) – Bearisches Delta
- `bubble_size` (string) – "S" / "M" / "L" (≥2σ / ≥3σ / ≥4σ)
- `absorption` (bool) – Absorption erkannt (violett: hohes Vol + kleiner Body)
- `divergence_bull` (bool) – Bullische Divergenz (Kurs↓ aber Delta+)
- `divergence_bear` (bool) – Bärische Divergenz (Kurs↑ aber Delta-)

---

### Modul 3 – POI Nearest
**Basis:** POI_Near_Final (Pine V6)
**Funktion:** Zeigt die 2-5 nächsten POIs zum aktuellen Preis

**POI-Hierarchie:** Monthly > Weekly > Daily
**POI-Liste:** PMH/PML/PMC, PWH/PWL/PWC, PDH/PDL/PDC, PP/R1-R3/S1-S3, VWAP

**Output-Status (für Hauptprogramm):**
- `poi_near` (bool) – Preis ≤ ATR-Distanz zu nächstem POI
- `poi_level` (float) – Level des nächsten POI
- `poi_name` (string) – Name des nächsten POI
- `poi_above` (float) – Nächster POI oberhalb (Resistance)
- `poi_below` (float) – Nächster POI unterhalb (Support)

---

## 4. HAUPTPROGRAMM – Confluence Engine

### Aufgabe
Fragt die Status-Outputs aller drei Module ab und bewertet die aktuelle
Marktsituation auf Trademöglichkeiten.

### Signal-Hierarchie

#### A) MARKET ENTRY SIGNAL (sofort, höchste Priorität)
Voraussetzung: Preis ist an Zone + Bubble-Bestätigung

| Signal | Bedingung | Typ |
|--------|-----------|-----|
| **Short Market** | price_at_bsl + absorption | Sofort Short |
| **Long Market** | price_at_ssl + absorption | Sofort Long |
| **Short Divergenz** | price_at_bsl + divergence_bear | Sofort Short |
| **Long Divergenz** | price_at_ssl + divergence_bull | Sofort Long |

#### B) LIMIT ENTRY SETUP (vorbereiten, mittlere Priorität)
Voraussetzung: Preis nähert sich Zone, noch kein Bubble-Signal

| Setup | Bedingung | Aktion |
|-------|-----------|--------|
| **Short Limit** | price_near_bsl + poi_near (Resistance) | Limit Short an BSL |
| **Long Limit** | price_near_ssl + poi_near (Support) | Limit Long an SSL |

#### C) STOP ENTRY SETUP (bei kritischem Level darunter/darüber)
Orion-Regel: Wenn relevantes POI-Level knapp jenseits der Zone liegt

| Setup | Bedingung | Aktion |
|-------|-----------|--------|
| **Short Stop** | price_at_bsl + poi_above (nahe) | Buy-Stop über POI |
| **Long Stop** | price_at_ssl + poi_below (nahe) | Sell-Stop unter POI |

---

### Confluence Score (0–7)
| Bedingung | Punkte |
|-----------|--------|
| Preis an BSL oder SSL Zone | +1 |
| M5 Zone innerhalb H1 Zone (doppelte Confluence) | +2 |
| POI in Zone (poi_near = true) | +1 |
| Bubble aktiv (≥2σ) | +1 |
| Absorption | +1 |
| Divergenz | +2 *(stärkstes Signal)* |
| **Maximum** | **8** |

---

### Alert-Logik
| Alert | Trigger |
|-------|---------|
| **POI Nähe** | Preis ≤ 0.5×ATR(14) zu POI |
| **Absorption an Zone** | absorption + price_at_bsl/ssl |
| **Divergenz an Zone** | divergence_bull/bear + price_at_bsl/ssl |
| **Confluence Score** | Score ≥ User-Schwellenwert (Default: 3) |

---

## 5. ARCHITEKTUR (Pine V6)

```
MS_Confluence_System
├── Module 1: f_bsl_ssl()      → gibt Status-Struct zurück
├── Module 2: f_bubble()       → gibt Status-Struct zurück
├── Module 3: f_poi()          → gibt Status-Struct zurück
└── Main:     f_confluence()   → wertet alle 3 aus → Signal + Alert
```

### Entwicklungsreihenfolge
1. ✅ Modul 1 – BSL/SSL (FINAL v4)
2. ✅ Modul 3 – POI Nearest (FINAL)
3. ⬜ Modul 2 – Bubble (portieren/integrieren)
4. ⬜ Hauptprogramm – Confluence Engine
5. ⬜ Alerts verdrahten

---

## 6. DESIGN-PRINZIPIEN

- **Risk first** – jede Regel dient der Risikoreduktion (Orion-Leitmotiv)
- **Kleinste Schritte** – jedes Modul standalone kompilierbar und validierbar
- **Long/Bull immer zuerst** dokumentiert
- **Pine V6** durchgehend (wizardry-Bibliothek für echtes Delta)
- **Keine Lookahead-Bias** in Echtzeit-Signalen
- **barstate.islast** mit Tracking-Arrays für sauberes Rendering

---

## 7. PRAXISBEISPIEL – Orion Trade 27.02.2026 (Textbook)

### Setup: MNQ1! H1 – Move Origin Retest

**Kontext:** Nach massivem Aufwärtsmove (24./25. Feb) Rücksetzer zur Ursprungszone.

```
Move Origin Zone: ~24.840 – 24.880
→ Zone definiert durch: Lower Low + Impulskerze (bullisch)
→ Institutioneller Footprint: Wo startete der originale Impuls?
```

### Trade-Details
| Parameter | Wert |
|-----------|------|
| **Entry** | Limit Buy an MO-Oberkante (~24.880) |
| **Stop** | 62.25 Punkte unter Entry (0.25%) |
| **Target** | 107.75 Punkte → Buyside Liquidity (0.433%) |
| **R:R** | 1.73R (erreicht) |
| **Potential** | Weit mehr – Preis lief noch deutlich weiter |

### Die Kernregel (in einem Satz)
> **"Retest einer Zone die durch Lower Low mit Impulskerze beschrieben ist"**

### Mapping zu unserem Framework
| Orion-Element | Unser Framework |
|---------------|----------------|
| Move Origin Zone | SSL Zone (Modul 1) + POI darunter (Modul 3) |
| Impulskerze | Bubble-Bestätigung (Modul 2) |
| Limit Entry | Signal-Typ B: Limit Entry Setup |
| Buyside Liquidity als TP | BSL Zone (Modul 1) als Ziel |
| Risk first | SL definiert vor Entry – Orion-Leitmotiv |

### Warum "Textbook easy peasy"
1. Zone klar definiert (MO = LL + Impuls)
2. Rücksetzer präzise in Zone
3. Limit Entry – kein Stress, keine Entscheidung unter Druck
4. SL logisch unter Zone
5. TP = nächste Liquidität (BSL)

---

## 8. OFFENE FRAGEN

1. Wie wird H1 BSL/SSL in M1-Chart referenziert? → request.security()
2. Wie wird M5 BSL/SSL in M1-Chart referenziert? → request.security()
3. UDT oder separate Arrays für Modul-Status-Übergabe?
4. Bubble-Modul: eigener Code oder wizardry-Import direkt im Hauptprogramm?

---

*MS_Confluence_System_Konzept.md · Wolfgang · Nova (Claude) · 27.02.2026*
