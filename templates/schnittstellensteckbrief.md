# Vorlage: Schnittstellensteckbrief

Ein Blatt je Anbindung. Wer die Felder nicht füllen kann, sollte die Anbindung nicht in Betrieb nehmen — nicht aus Formalismus, sondern weil jedes leere Feld später eine Frage ist, die niemand beantworten kann.

---

## Kopf

| Feld | Eintrag |
|---|---|
| Bezeichnung | |
| Muster | Abgleich / Ereigniskanal / Protokollzugang / Nachweisausgabe |
| Quellsystem | |
| Zielsystem | |
| Richtung | herein / hinaus / beidseitig |
| **Verantwortliche Person** | *nicht das Team — eine Person, die Meldung bekommt, wenn die Anbindung stillsteht* |
| Vertretung | |
| In Betrieb seit | |
| Letzte Überprüfung | |

## Zweck

| Feld | Eintrag |
|---|---|
| Welche Frage beantwortet diese Anbindung? | |
| Welche Entscheidung hängt davon ab? | |
| Was passiert, wenn sie einen Monat ausfällt? | |
| Ursprünglicher Zweck der Daten im Quellsystem | |
| **Zweckänderung geprüft (Art. 6 Abs. 4)?** | ja am ______ / entfällt, weil ______ |

## Übertragene Felder

| Feld | Personenbezug | Warum erforderlich | Aggregiert | Pseudonymisiert |
|---|---|---|---|---|
| | ja / nein | | ja / nein | ja / nein |

| Feld | Eintrag |
|---|---|
| **Freitextfelder übertragen?** | nein / ja — *dann besondere Kategorien möglich, Schutzniveau im Ziel prüfen* |
| Besondere Kategorien (Art. 9) enthalten? | ja / nein |
| Bewusst weggelassene Felder | *ebenso aussagekräftig wie die übernommenen* |

## Datenschutz

| Feld | Eintrag |
|---|---|
| Eintrag im Verarbeitungsverzeichnis Nr. | |
| Rechtsgrundlage | |
| Bei berechtigtem Interesse: Abwägung vom | |
| Empfänger außerhalb der Organisation | |
| Auftragsverarbeiter beteiligt? | ja — AVV vom ______ / nein |
| Drittlandübermittlung | ja — Garantie: ______ / nein |
| **Aufbewahrung im Zielsystem** | |
| Werden Löschungen aus der Quelle mitgeführt? | ja / **nein — dann hebt die Anbindung jede Löschung faktisch auf** |
| Wie wird eine Betroffenenanfrage in beiden Systemen beantwortet? | |
| **Mitbestimmung erforderlich?** | nein / ja — beteiligt am ______, Vereinbarung vom ______ |

## Betrieb

| Feld | Eintrag |
|---|---|
| Häufigkeit | |
| Auslöser | Zeitplan / Ereignis / manuell |
| Zugangsdaten | eigene Kennung der Anbindung / **Konto einer Person — zu ändern** |
| Rechte im Quellsystem | nur lesend / schreibend — Begründung: ______ |
| Stabiler Schlüssel aus der Quelle | |

### Führung je Feld (nur beim Muster Abgleich)

| Feld | Führendes System | Bei Konflikt |
|---|---|---|
| | Quelle / Register | überschreiben / markieren |

*Bewertungsfelder — Risikoklasse, Zweckbestimmung, Einstufung — werden vom Register geführt und nie überschrieben.*

### Verhalten bei Abweichungen

| Fall | Verhalten |
|---|---|
| Neuer Datensatz in der Quelle | als **unbewerteter Entwurf** anlegen, nicht als fertigen Eintrag |
| Datensatz verschwindet aus der Quelle | **zur Prüfung markieren, nie löschen** |
| Widersprüchlicher Wert | nach Führungstabelle |
| Doppelter Lauf | keine Dublette — Schlüssel: ______ |

## Überwachung

| Feld | Eintrag |
|---|---|
| Zeitpunkt des letzten erfolgreichen Laufs sichtbar? | ja / nein |
| Zahl der verarbeiteten Datensätze protokolliert? | ja / nein |
| **Alarm bei null Datensätzen?** | ja / nein — *sonst sieht Stillstand wie Ruhe aus* |
| Alarm bei Fehler — an wen | |
| Wer liest die Abweichungen, wie oft | |
| Protokollierung der Anbindung selbst | |

## Abhängigkeiten

| Feld | Eintrag |
|---|---|
| Was bricht, wenn das Quellsystem sich ändert | |
| Bekannte Schwachstelle | *meist: Feldnamen ohne Versionierung* |
| Wer informiert über Änderungen am Quellsystem | |

---

MIT-Lizenz, frei verwendbar. Keine Rechtsberatung. Vorlage von [SimpleAct](https://simpleact.de) · Stand September 2026
