# SBS Pattern Definition - Detailed Point Descriptions

**Version:** 0.3  
**Status:** 🧪 Working Hypotheses  
**Last Updated:** 2026-02-05

---

## 📐 Complete Pattern Structure

```
MSB → 1 → 2 → 3 → 4 → Entry (50-61.8%) → 5 → Breakout → TP1 → TP2
```

---

## 🔴 MSB (Market Structure Break)

### What is it?
The starting point of the movement that breaks a previous high.

### Criteria:
- **Close** above previous high (not just wick)
- **Minimum strength:** ≥23.6% Fibonacci of swing range
- Creates **dynamic movement** (momentum required)

### Why 23.6%?
We want to ensure it's a real breakout, not just noise. A 1-pip break is NOT sufficient.

### Fibonacci Anchor Points:
- **100% Fibo** = MSB origin level (bottom of the breakout move)
- **0% Fibo** = Point 3 (highest high)

---

## 🔵 Point 1 (P1)

### What is it?
First higher high that creates the MSB.

### Criteria:
- Above previous high
- Creates new high
- Is the pivot of MSB movement

### Visual:
```
     P1 ← New High
    /|
   / |
  /  prev high
```

---

## 🟢 Point 2 (P2)

### What is it?
Pullback after Point 1.

### Criteria:
- **MUST** fall below previous high (the high BEFORE P1)
- **Minimum:** 1 pip is sufficient (with strong momentum)
- Is a local low
- **Maximum depth:** TBD from chart analysis

### Why minimum 1 pip?
With strong momentum, pullback can be very shallow.

### Visual:
```
     P1
    /|
   / |\
  /  | \
     |  P2 ← Must be below prev high
   prev high
```

---

## 🟡 Point 3 (P3)

### What is it?
New higher high above Point 1.

### Criteria:
- Above Point 1 (higher high)
- **Confirmation ONLY when:** Price then falls below Point 2
- **Invalid if:** No move below Point 2 occurs

### CRITICAL: Retrospective Confirmation!
Point 3 is only confirmed AFTER price moves below Point 2.

### Timing:
- Can be immediately next bar
- Often takes at least as long as P2→P3 duration
- Can extend to multiple times the P2→P3 duration
- **Timeout:** TBD from charts

### Visual:
```
          P3 ← Highest high
         /|
        / |
     P1   |
    /|    |
   / |    |\
  /  |    | \
     P2   |  \ ← MUST go below P2 to confirm P3
          |
```

---

## 🟣 Point 4 (P4)

### What is it?
Pullback from Point 3 that goes below Point 2.

### Criteria:
- Below Point 2 (this confirms P3)
- Updated with each new low
- **Valid as long as:** Price stays above 100% Fibo
- **Invalid if:** Price breaks below 100% Fibo

### Important Notes:
- **P4 ≠ Entry Point!**
- P4 typically between 65-90% Fibo
- P4 is below the entry zone (50-61.8%)
- P4 is dynamic until price rises above 61.8% again

### Visual:
```
          P3 (0%)
         /|
        / |
     P1   |\
    /|    | \
   / |    |  \
  /  P2   |   P4 ← Below P2, around 70-80% Fibo
     |    |   |
   MSB ───────────── 100% Fibo (Stop Loss area)
```

---

## 🟠 Entry Zone (Golden Zone)

### Range: 50% - 61.8% Fibonacci

### Strategy:
1. Wait for price to reach Golden Zone
2. Start with limit order at 50%
3. Trail order upward if price rises
4. Improve Risk:Reward ratio
5. Final entry somewhere between 50-61.8%

### Important:
- NOT a fixed order at 61.8%
- Dynamic entry management
- Only filled ONCE
- Partial exits must be possible

---

## 🔴 Point 5 (P5) - The Post-Entry Sweep

### What is it?
Second pullback AFTER entry that goes below 61.8% again.

### Current Understanding:
- **Frequency:** "Appears to be the rule" (trader experience)
- **Position:** "Often below 61.8%, around P4 level" (~65-75% Fibo?)
- **Function:** Liquidity sweep / stop hunt

### Characteristics:
- Sweeps for open orders
- Creates floating loss after entry
- Is NORMAL, not a failure signal
- Do NOT exit at P5!

### Relation to P4:
- P5 usually a **higher low** vs P4 (~83%?)
- P5 can equal P4
- P5 lower than P4 is rare

### High Variance:
Different traders interpret P5 differently:
- Some: P5 = any swing low after entry
- Some: P5 = only if below 61.8%
- Some: Don't mark P5 at all

**Priority:** Needs empirical analysis from charts!

### Visual:
```
          P3 (0% - TP2)
         /|         /
        / |        /
     P1   |       / ← Breakout after P5
    /|    |\     /
   / |    | \   /
  /  P2   |  \ / ← 61.8% Entry
     |    |  P4
     |    |   |\
     |    |   | P5 ← Second dip (liquidity sweep)
   MSB ───────────── 100% Fibo
              105% ← Actual Stop Loss (100% + ATR buffer)
```

---

## 🎯 Take Profit Levels

### TP1: 23.6% Fibonacci
- First target
- Partial exit recommended

### TP2: 0% Fibonacci (Point 3 level)
- Second target
- Full exit or trailing stop

---

## ❌ Pattern Invalidation

### Scenario A: Price breaks below 100% Fibo
```
Setup FAILED
→ Long bias invalid
→ NO trade
→ Wait for new setup
```

### Scenario B: No move below Point 2 after Point 3
```
Point 3 unconfirmed
→ Setup invalid
→ Wait for new setup
```

### Scenario C: Point 4 doesn't reach Golden Zone
```
Price doesn't pull back to 50-61.8%
→ No entry signal
→ Setup "missed" (not failed!)
→ Strong momentum - wait for next MSB
```

---

## 🔬 Validation Required

All definitions are HYPOTHESES until validated through:
1. Chart analysis (20-50+ examples)
2. Statistical measurement
3. Expert review
4. Backtesting

**Next Step:** Upload charts for empirical validation! 📊
