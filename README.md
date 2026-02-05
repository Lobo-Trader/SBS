# SBS (Swing Breakout Sequence) Indicator

Ein TradingView Pine Script v5 Indikator zur automatischen Erkennung von SBS-Mustern.

## 🎯 Projekt-Ziel

Entwicklung eines robusten Indikators, der das SBS-Muster (Swing Breakout Sequence) automatisch erkennt und signalisiert.

## 📊 SBS-Muster Übersicht

Das SBS-Muster besteht aus 5 Punkten:

1. **Punkt 1**: Erster Swing High (nach MSB - Market Structure Break)
2. **Punkt 2**: Pullback/Retracement Low
3. **Punkt 3**: Higher High (über Punkt 1)
4. **Punkt 4**: Retracement zur 61.8% Fibonacci-Zone ⚡ **ENTRY SIGNAL**
5. **Punkt 5**: Breakout-Bestätigung über Punkt 3

### Trading-Parameter:
- **Entry**: 61.8% Fibonacci Retracement (Punkt 3 → Punkt 2)
- **Stop Loss**: 100% (Punkt 2 Level)
- **TP1**: 23.6% Fibonacci Extension
- **TP2**: 0% (Punkt 3 Level)

## 📁 Repository-Struktur

```
SBS/
├── charts/                  # Chart-Beispiele
│   ├── validated/          # Bestätigte SBS-Muster
│   ├── false-signals/      # Fehlsignale
│   └── edge-cases/         # Grenzfälle
├── rules/                   # Regelwerk-Entwicklung
│   ├── v1-initial-rules.md
│   ├── v2-refined-rules.md
│   └── observations.md
├── code/                    # Pine Script Code
│   └── sbs-indicator.pine
└── docs/                    # Zusätzliche Dokumentation
    └── pattern-analysis.md
```

## 🚀 Entwicklungs-Phasen

### Phase 1: Datensammlung ✅ AKTUELL
- Chart-Beispiele hochladen und kategorisieren
- Muster visuell analysieren

### Phase 2: Regelextraktion
- Gemeinsame Merkmale identifizieren
- Quantitative Parameter definieren
- Edge Cases dokumentieren

### Phase 3: Code-Entwicklung
- Pine Script v5 Implementierung
- Backtesting mit Chart-Beispielen
- Optimierung

### Phase 4: Validierung & Verfeinerung
- Live-Testing
- Iterative Verbesserungen

## 📈 Wie Charts hochladen?

1. Navigiere zum entsprechenden Ordner in `charts/`
2. Klicke auf "Add file" → "Upload files"
3. Benenne die Datei aussagekräftig: `SYMBOL_DATUM_BESCHREIBUNG.png`
   - Beispiel: `NQ_2026-02-03_clear-sbs.png`
4. Füge im Commit eine kurze Beschreibung hinzu

## 🔍 Was analysieren wir?

Für jeden Chart extrahieren wir:
- ✅ Abstände zwischen Punkten (in Bars/Candles)
- ✅ Fibonacci-Verhältnisse
- ✅ Candlestick-Muster an Punkt 4
- ✅ Trendlinien-Winkel
- ✅ Volumen-Charakteristiken
- ✅ Zeitliche Muster

## 📝 Lizenz

Proprietary - Alle Rechte vorbehalten

---

**Erstellt**: 2026-02-05 13:37:24  
**Plattform**: TradingView (Pine Script v5)  
**Status**: 🟡 In Entwicklung