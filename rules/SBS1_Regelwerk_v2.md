# Mechanical SBS1 – Vollständiges Regelwerk

> **Swing Breakout Sequence (SBS1)** – Ein Trendfortsetzungsmuster basierend auf Pure Price Action.  
> Es identifiziert strukturelle Brüche (MSB/BOS) und nutzt eine definierte Punktefolge P0→P5  
> für präzise Entry-, Stop- und Target-Bestimmung.

---

## Kapitel 0 – Fundament: Pure Price Action (Pivot-Logik)

Das SBS-System baut auf einem eigenständigen **Pure Price Action System** auf,  
das ausschließlich Swing-Pivots (HH, HL, LH, LL) und deren Brüche betrachtet.

### Pivot-Definitionen

| Begriff | Bedeutung |
|---------|-----------|
| **HH** | Higher High – neues Hoch über dem vorherigen Hoch |
| **HL** | Higher Low – neues Tief über dem vorherigen Tief |
| **LH** | Lower High – neues Hoch unter dem vorherigen Hoch |
| **LL** | Lower Low – neues Tief unter dem vorherigen Tief |

### Trendstruktur

```
Aufwärtstrend:   HH → HL → HH → HL → ...  (Struktur intakt)
Abwärtstrend:    LL → LH → LL → LH → ...  (Struktur intakt)
```

### MSB / BOS – Definition (KRITISCH)

> Ein **Market Structure Break (MSB)** bzw. **Break of Structure (BOS)** liegt vor,  
> wenn der **Close-Preis einer Kerze** das Level eines vorherigen Swing-Pivots  
> (HH oder LL) **endgültig durchbricht**.

**Zwingend: Close-Regel**

```
✅ BOS bestätigt  = Kerzen-CLOSE liegt über/unter dem Pivot-Level
❌ KEIN BOS       = Preis berührt das Level nur (Wick/Shadow)
❌ KEIN BOS       = Intrabar-Unterschreitung ohne Close-Bestätigung
```

**Zeitliche Konsequenz:**  
Der MSB ist erst in dem Moment bekannt, in dem die entsprechende Kerze **schließt**.  
Alle rückwirkenden Punkte (P0, P1) werden erst ab diesem Zeitpunkt als bestätigt behandelt.

### Was ein MSB bedeutet

Ein MSB zeigt an, dass der Markt ein Preisniveau durchbrochen hat,  
bei dem potenzielle **Limit-Orders** von Marktteilnehmern lagen.  
Diese Orders sind nun nicht mehr aktiv – der Markt hat sie abgeräumt.  
Das ist das strukturelle Fundament für die folgende SBS-Bewegung.

---

## Kapitel 1 – SBS1 Grundstruktur

### Zeitliche Abfolge (ZWINGEND)

```
P0  →  MSB  →  P1  →  P2  →  P3  →  P4  →  (P5 optional)  →  Entry
```

**Kein Punkt darf zeitlich vor seinem Vorgänger liegen.**  
**Rückwärtslesen ist zur Identifikation notwendig** (P0 wird erst nach MSB+P1 bekannt).

---

## Kapitel 2 – Bullisches SBS1

### Entscheidungsbaum

```
SCHRITT 1: MSB ABWARTEN
─────────────────────────────────────────────────────
Warte auf einen CLOSE über einem vorherigen Swing-HH
→ Erst jetzt ist der MSB bestätigt
→ Erst jetzt wird P0 rückwirkend bestimmt

       │
       ▼

SCHRITT 2: P0 RÜCKWIRKEND BESTIMMEN
─────────────────────────────────────────────────────
P0 = das Swing-LOW das den Impuls startete,
     der den MSB erzeugt hat
→ P0 liegt zeitlich VOR dem MSB

       │
       ▼

SCHRITT 3: P1 IDENTIFIZIEREN
─────────────────────────────────────────────────────
P1 = erstes Swing-HIGH nach dem MSB
→ erstes Higher High nach dem Bruch

       │
       ▼

SCHRITT 4: P2 ABWARTEN
─────────────────────────────────────────────────────
Warte auf Retracement nach P1

BEDINGUNGEN:
  ✅ P2 liegt UNTER dem MSB/BOS-Level
  ✅ P2 ≥ 50% Retracement von P0 → P1
  ✅ P2 liegt ÜBER P0 (sonst Pattern ungültig!)

ACHTUNG – P2 kann sich verschieben:
  → Preis darf nach P1 noch weiter fallen
  → Neues tieferes P2 ist erlaubt (solange > P0)
  → Fällt Preis unter P0 → Pattern UNGÜLTIG

       │
       ▼

SCHRITT 5: P3 ABWARTEN
─────────────────────────────────────────────────────
Warte auf neues Higher High über P1

BEDINGUNGEN:
  ✅ P3 deutlich über P1

ACHTUNG – P3 kann sich verschieben:
  → Preis kann erst weiter steigen → höheres P3 möglich
  → Preis kehrt evtl. gar nicht zurück
    → Pattern setzt sich fort ohne Entry (kein Trade)

       │
       ▼

SCHRITT 6: P4 ABWARTEN – ENTRY-ZONE
─────────────────────────────────────────────────────
Fibonacci wird gemessen von P0 (=100%) → P3 (=0%)

BEDINGUNGEN:
  ✅ P4 erreicht oder unterschreitet 61,8% von P0→P3
  ✅ P4 liegt zwingend UNTER P2

AB P4: DREI SZENARIEN
─────────────────────────────────────────────────────
  a) Preis fällt unter 100% (= unter P0-Niveau)
     → Pattern VERSAGT → kein Trade

  b) Sofortige Aufwärtsbewegung nach P4
     → ENTRY bei 61,8%

  c) Seitwärts / W-Pattern → P5 (OPTIONAL)
     → P5 liegt unter P4
     → Zusätzliche Bestätigung
     → Erhöht Pattern-Qualität
     → Ist KEIN Pflichtbestandteil

       │
       ▼

SCHRITT 7: TRADE-PARAMETER
─────────────────────────────────────────────────────
  Entry:  61,8% Fibonacci (P0 → P3)
  Stop:   100% Fibonacci  (= P0-Niveau)
  TP1:    23,6% Fibonacci
  TP2:    0%   Fibonacci  (= P3-Niveau)
```

---

## Kapitel 3 – Punkteübersicht Bullisches SBS1

| Punkt | Bedeutung | Bedingung |
|-------|-----------|-----------|
| **P0** | Ausgangspunkt der Impulsbewegung | Swing-Low vor MSB; wird rückwirkend bestimmt |
| **MSB** | Market Structure Break | Close einer Kerze über vorherigem Swing-HH; erst dann bekannt! |
| **P1** | Erstes Higher High nach MSB | Erster Swing-High nach dem Bruch |
| **P2** | Retracement nach P1 | Unter MSB-Level; ≥50% von P0→P1; darf nicht unter P0 fallen |
| **P3** | Neues Higher High | Deutlich über P1; kann sich mehrfach nach oben verschieben |
| **P4** | Entscheidender Pullback / Entry-Zone | Unter P2; ≥61,8% Retracement von P0→P3 |
| **P5** | Optionales W-Pattern | Unter P4; erhöht Qualität; kein Pflichtbestandteil |

---

## Kapitel 4 – Fibonacci-Referenz

```
Gemessen IMMER von P0 (=100%) bis P3 (=0%)

  0,0%  ────────────────── P3 (Extrempunkt)     ← TP2
 23,6%  ──────────────────                       ← TP1
 61,8%  ──────────────────  ◄ ENTRY / P4-Zone
100,0%  ────────────────── P0 (Ausgangspunkt)   ← STOP
```

---

## Kapitel 5 – Invalidierung

Das Pattern ist **ungültig / versagt** wenn:

- Preis fällt unter P0 (während Warten auf P2 oder P4)
- P2 liegt über dem MSB-Level
- P3 liegt nicht deutlich über P1
- P4 liegt über P2
- Nach P4: Close unter 100%-Niveau (= Stop-Level)

---

## Kapitel 6 – Bearisches SBS1 (gespiegelt)

Alle Regeln gelten **identisch aber invertiert**:

| Bullisch | Bearisch |
|----------|----------|
| MSB = Close über Swing-HH | MSB = Close unter Swing-LL |
| P0 = Swing-Low | P0 = Swing-High |
| P1 = erstes Higher High | P1 = erstes Lower Low |
| P2 unter MSB, ≥50% Retrace aufwärts | P2 über MSB, ≥50% Retrace abwärts |
| P3 = neues Higher High über P1 | P3 = neues Lower Low unter P1 |
| P4 unter P2 bei ≥61,8% | P4 über P2 bei ≥61,8% |
| P5 = W-Pattern unter P4 | P5 = M-Pattern über P4 |
| Entry Long bei 61,8% | Entry Short bei 61,8% |
| Stop unter 100% | Stop über 100% |

---

## Kapitel 7 – Praxisbeispiel Bearisches SBS1

**MGC1 (Micro Gold Future) · 5M Chart · 16./17. Februar 2026**

```
P0   = 5037,6  (10:35 Uhr, 16. Feb)  – Swing-High, Ausgangspunkt
MSB  = 4989    (bestätigt ~01:50 Uhr, 17. Feb durch Close unter 4989)
               ⚠️ Der MSB bei 4989 entstand um 16:10 Uhr,
                  ist aber erst ~01:50 Uhr BESTÄTIGT
                  (erst dann schließt eine Kerze mit Close unter 4989)
P1   = 4989    (16:10 Uhr, 16. Feb)  – erstes Lower Low nach MSB
P2   = 5022    (00:15 Uhr, 17. Feb)  – Bounce, ~69% Retrace von P0→P1 ✅
P3   = 4941    (00:25 Uhr, 17. Feb)  – neues Lower Low unter P1 ✅
P4   = ~4978   (Fibonacci 61,8% von P0→P3: 5037-(96×0,618)=~4978) ✅

Trade-Parameter:
  Entry Short:  ~4978
  Stop:         5037,6  (= P0)
  TP1:          ~5014   (23,6%)
  TP2:          4941    (0% = P3-Niveau)
```

---

## Kapitel 8 – Visuelle Darstellung

### Bullisches SBS1 (Linienchart)

```
Preis
  │
  │                              P3 ●──────────────  0,0%  TP2
  │                             /│
  │                            / │
  │              P1 ●         /  │──────────────────  23,6% TP1
  │             /   \        /
  │            /     \      /
  │  MSB ·····        \    /
  │  ─────────          P2●
  │           /              \
  │          /                P4 ●────────────────── 61,8% ENTRY
  │  P0 ●───                   │
  │                             │ (optional P5 ● unter P4)
  │                             │──────────────────── 100%  STOP
  └────────────────────────────────────────────────── Zeit
     Impuls  MSB  P1   P2    P3   P4  Entry
```

### Bearisches SBS1 (Linienchart)

```
Preis
  │                             │──────────────────── 100%  STOP
  │                             │ (optional P5 ● über P4)
  │  P0 ●───                   │
  │          \                P4 ●────────────────── 61,8% ENTRY
  │           \              /
  │  MSB ·····        P2●
  │  ─────────          \      \
  │            \         \      \
  │              P1 ●     \      │──────────────────  23,6% TP1
  │                        \     │
  │                         \    │
  │                          P3 ●──────────────────   0,0%  TP2
  └────────────────────────────────────────────────── Zeit
```

---

## Kapitel 9 – Abgrenzung SBS2 (Vorschau)

> **SBS2** deckt Sonderfälle ab in denen die P0→P1→P2... Struktur entsteht  
> **ohne einen vorherigen MSB/BOS**.  
> Die Punktefolge und Entry-Logik bleibt identisch.  
> SBS2 wird in einem separaten Dokument definiert.

---

*Dokument: SBS1_Regelwerk_v2.md*  
*Erstellt: 17. Februar 2026 | Lobo-Trader / Nova*  
*Repository: https://github.com/Lobo-Trader/SBS/tree/main/rules*
