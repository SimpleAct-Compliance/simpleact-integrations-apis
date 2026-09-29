# Vier Muster

## Muster 1: Abgleich

*Ein vorhandenes System liefert regelmäßig Datensätze, die das Register aktuell halten.*

Typisch: Kreditorenliste, Anwendungsliste aus dem Anmeldedienst, Vertragsverwaltung, Personalstammdaten.

### Die Entscheidung, die alles andere bestimmt

**Wer hat recht, wenn beide Seiten etwas anderes sagen?**

Diese Frage muss je **Feld** beantwortet werden, nicht je System. In der Praxis liegt die Wahrheit fast immer verteilt:

| Feld | Führendes System |
|---|---|
| Anbietername, Vertragsbeginn, Tarif | Beschaffung |
| Verantwortliche Person | Verzeichnisdienst |
| Risikoklasse, Zweckbestimmung, Einstufung | **Register** — steht nirgendwo sonst |
| Betriebsstatus | Betriebsüberwachung |

Wer das nicht festlegt, baut eine Schnittstelle, die bei jedem Lauf die Bewertungen überschreibt, die jemand von Hand eingetragen hat. Das passiert genau einmal, danach wird die Schnittstelle abgeschaltet.

### Die vier Fallstricke

**Löschen ist gefährlicher als Anlegen.** Ein Datensatz verschwindet aus der Quelle — heißt das, das System ist außer Betrieb, oder ist nur ein Filter falsch? Ein Abgleich sollte nie löschen, sondern **zur Prüfung markieren**. Alles andere vernichtet irgendwann eine Historie, die für eine Aufarbeitung gebraucht wird.

**Neue Einträge sind Entwürfe.** Ein automatisch angelegter Eintrag ist ein Hinweis, kein Inventareintrag. Er braucht eine Einstufung durch einen Menschen, und bis dahin sollte er als unbewertet sichtbar sein — nicht als vollständig.

**Wiederholbarkeit.** Zweimal derselbe Lauf darf nicht zweimal denselben Eintrag erzeugen. Das verlangt einen stabilen Schlüssel aus der Quelle, nicht den Namen — Namen ändern sich.

**Umbenennungen.** Ein Anbieter wird umbenannt oder übernommen. Ohne stabilen Schlüssel entsteht ein zweiter Eintrag, und die Historie des ersten ist verloren.

### Häufigkeit

Täglich ist fast immer zu oft, jährlich zu selten. Monatlich reicht für Beschaffung und Verträge; wöchentlich für Zuständigkeiten, wenn Personalwechsel häufig sind. Wichtiger als die Frequenz ist, dass jemand die Abweichungen **liest** — ein Abgleich, dessen Ergebnis niemand ansieht, ist teurer als keiner.

---

## Muster 2: Ereigniskanal

*Auffälligkeiten werden dort gemeldet, wo die Menschen ohnehin arbeiten.*

Typisch: Ticketsystem, Gruppenchat, Formular im Intranet, E-Mail-Verteiler.

### Die Regel

**Der Meldeweg muss kürzer sein als das Zögern.** Wer überlegen muss, wo er meldet, meldet nicht. Ein Kanal, den alle kennen, schlägt drei spezialisierte, die niemand findet.

Daraus folgt: einen Eingang, nicht mehrere. Die Sortierung passiert danach, nicht davor.

### Was der Kanal aufnehmen muss

Fünf Angaben, mehr nicht — jedes weitere Pflichtfeld kostet Meldungen:

1. Was ist aufgefallen
2. Welches System
3. Wann
4. Wer meldet
5. Läuft gerade jemand Gefahr, oder hat es Zeit

Alles Weitere wird im Gespräch geklärt. Ein Formular mit vierzehn Pflichtfeldern ist ein Filter gegen Meldungen, nicht für sie.

### Die Abgrenzung, die sitzen muss

Ein Ticket ist **kein** Fristbeginn nach den Meldepflichten — aber es kann einer werden. Der Übergang von „Auffälligkeit" zu „Vorfall" ist ein bewerteter Schritt mit einem benannten Verantwortlichen und einem Zeitstempel.

Umgekehrt gilt: Wenn eine Auffälligkeit tagelang unbewertet im Ticketsystem liegt, läuft die Frist trotzdem, sobald die Kenntnis vorlag. Ein Eingangskanal ohne Sichtung ist ein Risiko, kein Verfahren.

### Rückmeldung

Der meistunterschätzte Teil. Wer meldet und nie erfährt, was daraus wurde, meldet beim nächsten Mal nicht mehr. Eine Rückmeldung in zwei Sätzen genügt und entscheidet darüber, ob der Kanal in einem Jahr noch lebt.

---

## Muster 3: Protokollzugang

*Belege für Aufsicht, Eingriffe und Systemverhalten — lesend, ohne Kopie.*

### Warum lesend

Protokolle enthalten regelmäßig personenbezogene Daten, oft in großer Menge und mit hoher Aussagekraft über einzelne Personen. Wer sie in ein Governance-Werkzeug kopiert, verlagert ein Datenschutzrisiko von einem System, das dafür gebaut ist, in eines, das es nicht ist — und verdoppelt die Aufbewahrung.

Die bessere Lösung ist fast immer: **Kennzahlen übernehmen, Einzeldatensätze verweisen.** Das Register enthält „im September wurden 1.284 Ausgaben erzeugt, 37 überstimmt", zusammen mit einem Verweis, unter dem die Einzelfälle im Quellsystem auffindbar bleiben.

### Was man wirklich braucht

| Kennzahl | Wofür |
|---|---|
| Zahl der Ausgaben | Bezugsgröße |
| Zahl der Eingriffe und Ablehnungen | Wirksamkeit der Aufsicht |
| Fehler- und Ausfallraten | Abweichung vom erwarteten Verhalten |
| Modellversion im Zeitverlauf | stille Wechsel erkennen |
| Auffällige Verteilungen über Gruppen | Hinweis auf Verzerrung |

Die letzte Zeile ist die heikelste: Sie verlangt gerade jene Merkmale, die man sonst nicht verarbeiten würde. Sie gehört nicht in einen laufenden Abgleich, sondern in eine gesondert begründete, zeitlich begrenzte Auswertung.

### Die Vertragsfrage

Protokollzugang ist nichts, was man technisch löst, wenn er vertraglich nicht vorgesehen ist. Er gehört in den Beschaffungsfragebogen — siehe [Anbieterregister](https://github.com/SimpleAct-Compliance/simpleact-model-vendor-register).

---

## Muster 4: Nachweisausgabe

*Aus dem Register wird ein Dokument, das jemand außerhalb lesen kann.*

Typisch: Auszug für eine Prüfung, Bericht an die Leitung, Anlage zu einer Ausschreibung, Unterlagen für die Aufsichtsbehörde.

### Drei Anforderungen

**Stichtagsbezug.** Ein Nachweis ohne Stichtag ist wertlos, weil er sich nicht mit einem späteren vergleichen lässt. Datum, Uhrzeit und Stand gehören auf jede Seite.

**Reproduzierbarkeit.** Derselbe Stichtag muss dasselbe Dokument ergeben — auch in einem Jahr. Das verlangt, dass Änderungen am Register versioniert sind und nicht überschrieben werden.

**Lesbarkeit für Außenstehende.** Ein Auszug, der interne Kürzel und Systemnamen enthält, erzeugt Rückfragen statt Vertrauen. Was ein Feld bedeutet, gehört in den Auszug, nicht in das Wissen des Erklärenden.

### Der häufigste Fehler

Der Nachweis wird zum Zeitpunkt der Prüfung erstellt und enthält den aktuellen Stand. Gefragt ist aber regelmäßig der Stand zu einem vergangenen Zeitpunkt — dem eines Vorfalls, einer Entscheidung, einer Beschwerde. Wer nur den Jetzt-Stand ausgeben kann, kann die Frage nicht beantworten.

---

## Was für alle vier gilt

**Eine Anbindung, die niemandem gehört, verrottet.** Jede Schnittstelle braucht eine benannte Person, die erfährt, wenn sie stillsteht. Der häufigste Ausfallgrund ist nicht ein Fehler, sondern ein Feldnamenwechsel im Quellsystem, den niemand bemerkt hat — der Lauf meldet Erfolg und überträgt nichts.

**Stillstand muss auffallen.** Ein Abgleich, der nichts findet, sieht genauso aus wie einer, der nicht läuft. Der Unterschied muss sichtbar sein: Zeitpunkt des letzten erfolgreichen Laufs, Zahl der verarbeiteten Datensätze, Alarm bei null.

**Klein anfangen.** Eine funktionierende Anbindung an die Kreditorenliste ist mehr wert als vier halbfertige. Die Reihenfolge nach Nutzen: Beschaffung, Ereigniskanal, Vertragsverwaltung, alles Übrige.

## Verwandtes

- [Woher die Daten kommen](./governance-signale.md)
- [Datenschutz in der Schnittstelle](./datenschutz-in-schnittstellen.md)
- [Vorlage: Schnittstellensteckbrief](../templates/schnittstellensteckbrief.md)

---

Keine Rechtsberatung. Stand: September 2026.
