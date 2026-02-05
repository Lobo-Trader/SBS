# SBS (Swing Breakout Sequence) Indicator

Ein TradingView Pine Script v5 Indikator zur automatischen Erkennung von Swing Breakout Sequences.

## 📋 Projekt-Übersicht

Dieses Projekt entwickelt einen Indikator zur Erkennung des SBS-Patterns basierend auf:
- **Punkt 1**: Erster Swing High (nach MSB)
- **Punkt 2**: Pullback/Retracement Low
- **Punkt 3**: Höheres Hoch (über Punkt 1)
- **Punkt 4**: Retracement zur 61.8% Fibonacci-Zone ⚡ **ENTRY SIGNAL**
- **Punkt 5**: Breakout-Bestätigung über Punkt 3

### Trading-Regeln (Mechanisch)
1. **SBS Pattern erkennen**
2. **Entry bei 61.8%** Fibonacci Retracement (Punkt 3 → Punkt 2)
3. **Stop Loss bei 100%** (Punkt 2 Level)
4. **TP1 bei 23.6%** Fibonacci Extension
5. **TP2 bei 0%** (Punkt 3 Level)

## 📁 Repository-Struktur

```
SBS/
├── charts/                 # Chart-Beispiele
│   ├── validated/          # Bestätigte SBS-Muster
│   ├── false-signals/      # Fehlsignale zum Lernen
│   └── edge-cases/         # Grenzfälle
├── rules/                  # Regelentwicklung
│   ├── v1-initial-rules.md
│   ├── v2-refined-rules.md
│   └── observations.md
├── code/                   # Pine Script Code
│   └── sbs-indicator.pine
├── docs/                   # Dokumentation
│   └── pattern-analysis.md
├── CONTRIBUTING.md
└── README.md
```

## 🚀 Aktueller Status

- [x] Repository erstellt
- [x] Basis-Struktur angelegt
- [ ] Chart-Sammlung hochladen
- [ ] Regeln aus Charts ableiten (Phase 1)
- [ ] Regeln verfeinern (Phase 2-N)
- [ ] Pine Script Indikator entwickeln
- [ ] Testing & Optimierung

## 📊 Vorgehensweise

### Phase 1: Chart-Sammlung
- Charts in entsprechende Ordner hochladen
- Jeder Chart zeigt markierte Punkte (1, 2, 3, 4, 5)

### Phase 2: Muster-Analyse
Für jeden Chart analysieren wir:
- Abstände zwischen Swing-Punkten
- Fibonacci-Verhältnisse
- Candlestick-Muster an Punkt 4
- Trendlinien-Winkel
- Volumen-Charakteristiken
- Zeitliche Abstände

### Phase 3: Regel-Extraktion
- Gemeinsame Merkmale identifizieren
- Quantitative Schwellenwerte definieren
- Edge Cases dokumentieren

### Phase 4: Code-Entwicklung
- Pine Script v5 Indikator programmieren
- Backtesting mit Chart-Beispielen
- Iterative Verbesserung

## 📖 Wie Charts hochladen?

Siehe [CONTRIBUTING.md](CONTRIBUTING.md) für Details.

## 📝 Lizenz

Proprietär - Alle Rechte vorbehalten

---

**Entwickelt von Lobo-Trader** 🐺📈