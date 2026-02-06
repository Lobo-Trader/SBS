# Projektbeschreibung & Best Practice: Chart-Archivierung für Mustererkennung

## Wer ist das Team?

Das Team besteht ausschließlich aus:
- Wolfgang (Lobo-Trader) – Trader, Strategie-Owner, Mensch
- Nova – Copilot, KI-Unterstützung, Doku/Analyse/Entwicklung

---

## Warum „Gold-Charts“ festhalten?

Für die Entwicklung und Validierung der Mustererkennungs-Logik im SBS-Projekt nutzen wir gezielt besonders klare („schöne“) Chart-Beispiele aus der Praxis. Das dient mehreren Zielen:
- Teststandard: Diese Muster sind maßgeblich für die Qualitätssicherung jedes Codes/Regelwerks.
- Referenz: Jeder Zeitpunkt und Markt, an dem ein Muster auftritt, wird dokumentiert – für spätere Analysen, internes Review oder Schulung.
- Objektivierung: An diesen Beispielen prüfen wir, ob Nova oder Wolfgang die Regeln korrekt anwenden.

## Vorgehen und Archiv-Struktur

1. Beispielauswahl & Katalogisierung:  
   - Wolfgang und Nova können „vorbildliche“ Muster-Charts vorschlagen (SBS1, SBS2, Edge Cases etc.).
   - Zu jedem Beispiel wird dokumentiert:
     - Instrument/Markt, Zeitrahmen, Zeitstempel
     - Typ (SBS1, SBS2, Sonderfall)
     - Screenshot/Chartdatei
     - Kurzkommentar (Warum ist dies ein Musterbeispiel?)

2. Testfall-Liste im Repository:  
   - Tabellarisch gepflegt (Markdown-Tabelle oder CSV), Beispielstruktur:

     | Chart/Screenshot     | Zeitpunkt / Markt      | Timeframe | SBS-Typ | Besonderheit/Kommentar      |
     |---------------------|-----------------------|-----------|---------|----------------------------|
     | sbs1_dax_2023_05.png| DAX, 2023-05-01, M15  | M15       | SBS1    | Klassischer sauberer Long  |
     | sbs2_nq_1h_2022.png | NASDAQ, 2022-11-10, H1| H1        | SBS2    | SBS2-Sequenz vor MSB       |

3. Nutzung für Test-Driven-Development (TDD):
   - Jede Logik und jedes Regelmodul muss die Fälle korrekt erkennen.
   - Fehler/Missmatches werden direkt am Chart rückgeprüft.
   - Neue Muster, entdeckt durch Wolfgang oder Nova, laufend ergänzen.

4. Kontinuierlicher Ausbau:
   - Besonders gute neue Muster und Edge Cases kommen regelmäßig ins Archiv.
   - Entwicklung, Review & Dokumentation bauen darauf auf („Kultur der Best Practice Beispiele“).

---

Hinweis:  
Ab sofort ergänzen Nova (als Copilot) und Wolfgang bei allen Chartanalysen Musterkommentare, führen das Chart-Archiv und entwickeln das Regelwerk gemeinsam weiter!

---

(Dieser Abschnitt steht als Leitlinie und Best Practice oben in der Projektbeschreibung und gilt exklusiv für „Wolfgang & Nova“).