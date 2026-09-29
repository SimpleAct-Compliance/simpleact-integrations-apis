# Vorlage: Abnahme einer Anbindung

Vor der Inbetriebnahme. Die Abnahme prüft nicht, ob die Anbindung funktioniert — das tut sie am ersten Tag immer. Sie prüft, was passiert, wenn sie **nicht** funktioniert, und ob jemand es merkt.

---

| Feld | Eintrag |
|---|---|
| Anbindung | |
| Steckbrief vom | |
| Abnahme am | |
| Beteiligt | Fachbereich · IT · Datenschutz · ggf. Mitbestimmung |

---

## A. Zweck und Grundlage

| # | Prüfpunkt | Ergebnis | Anmerkung |
|---|---|---|---|
| A1 | Der Zweck ist in einem Satz benannt und eine Entscheidung hängt davon ab | erfüllt / offen | |
| A2 | Eintrag im Verarbeitungsverzeichnis liegt vor | | |
| A3 | Rechtsgrundlage festgelegt, bei lit. f Abwägung dokumentiert | | |
| A4 | Zweckänderung gegenüber dem Quellsystem geprüft | | |
| A5 | Mitbestimmung geklärt, falls Verhalten oder Leistung erkennbar | | |
| A6 | Bei Dienstleister: AVV liegt vor, Unterauftragsverarbeiter benannt | | |

## B. Datenminimierung

| # | Prüfpunkt | Ergebnis | Anmerkung |
|---|---|---|---|
| B1 | Jedes übertragene Feld ist einzeln begründet | | |
| B2 | Geprüft, ob Aggregation statt Einzelwerten genügt | | |
| B3 | Geprüft, ob eine Kennung statt eines Namens genügt | | |
| B4 | Freitextfelder ausgeschlossen — oder Schutzniveau im Ziel gleichwertig | | |
| B5 | Besondere Kategorien ausgeschlossen oder gesondert begründet | | |

## C. Aufbewahrung und Betroffenenrechte

| # | Prüfpunkt | Ergebnis | Anmerkung |
|---|---|---|---|
| C1 | Löschfrist im Zielsystem festgelegt und technisch umgesetzt | | |
| C2 | **Löschung in der Quelle wird mitgeführt** | | |
| C3 | Eine Auskunft findet die Person in beiden Systemen | | |
| C4 | Eine Einschränkung nach Art. 18 wirkt in beiden Systemen | | |

*C2 ist der Punkt, der in der Praxis am häufigsten fehlt. Ohne ihn macht die Anbindung jede Löschung rückgängig.*

## D. Verhalten im Fehlerfall — der Kern der Abnahme

| # | Prüfpunkt | Ergebnis | Anmerkung |
|---|---|---|---|
| D1 | Zweiter Lauf mit denselben Daten erzeugt **keine** Dubletten | | |
| D2 | Verschwundener Datensatz wird **markiert, nicht gelöscht** | | |
| D3 | Neuer Datensatz erscheint als **unbewerteter Entwurf** | | |
| D4 | Bewertungsfelder werden **nicht** überschrieben | | |
| D5 | Umbenennung in der Quelle erzeugt keinen zweiten Eintrag | | |
| D6 | Abgebrochener Lauf hinterlässt keinen halben Stand | | |
| D7 | Quellsystem nicht erreichbar → Fehler, nicht stiller Erfolg | | |

### Der entscheidende Test

| # | Prüfpunkt | Ergebnis |
|---|---|---|
| D8 | **Ein Feldname im Quellsystem wird geändert. Meldet die Anbindung einen Fehler — oder meldet sie Erfolg und überträgt nichts?** | |

*Dieser eine Test findet den häufigsten Ausfallgrund überhaupt. Er lässt sich in einer Testumgebung in zehn Minuten durchführen und wird fast nie gemacht.*

## E. Erkennbarkeit von Stillstand

| # | Prüfpunkt | Ergebnis | Anmerkung |
|---|---|---|---|
| E1 | Zeitpunkt des letzten erfolgreichen Laufs ist sichtbar | | |
| E2 | Zahl der verarbeiteten Datensätze wird protokolliert | | |
| E3 | **Alarm bei null Datensätzen** eingerichtet | | |
| E4 | Alarm erreicht eine benannte Person, nicht einen Verteiler | | |
| E5 | Alarm wurde einmal ausgelöst und ist angekommen | | |

## F. Zugang und Sicherheit

| # | Prüfpunkt | Ergebnis | Anmerkung |
|---|---|---|---|
| F1 | Eigene Kennung für die Anbindung, nicht das Konto einer Person | | |
| F2 | Nur die Rechte, die gebraucht werden — lesend, wo lesend genügt | | |
| F3 | Zugangsdaten nicht im Quelltext, Wechsel vorgesehen | | |
| F4 | Übertragung verschlüsselt | | |
| F5 | Läufe der Anbindung selbst werden protokolliert | | |

## G. Verantwortung

| # | Prüfpunkt | Ergebnis | Anmerkung |
|---|---|---|---|
| G1 | Eine namentlich benannte Person ist verantwortlich | | |
| G2 | Vertretung geregelt | | |
| G3 | Wer die Abweichungen liest, und in welchem Turnus | | |
| G4 | Wer informiert, wenn sich das Quellsystem ändert | | |
| G5 | Termin der nächsten Überprüfung steht | | |

---

## Ergebnis

| | |
|---|---|
| Offene Punkte | |
| Davon blockierend | |
| Entscheidung | **Inbetriebnahme** / Inbetriebnahme mit Auflagen / zurückgestellt |
| Auflagen und Frist | |
| Abgenommen durch / am | |

---

MIT-Lizenz, frei verwendbar. Keine Rechtsberatung. Vorlage von [SimpleAct](https://simpleact.de) · Stand September 2026
