# Datenschutz in der Schnittstelle

## Der Satz, um den es geht

**Eine Schnittstelle ist eine Verarbeitungstätigkeit.**

Sie hat einen Zweck, eine Rechtsgrundlage, Empfänger, eine Aufbewahrungsdauer und technische Maßnahmen. Sie gehört damit ins Verarbeitungsverzeichnis — nicht als Anmerkung zu einem bestehenden Eintrag, sondern als eigener, wenn sie einen eigenen Zweck verfolgt.

Das wird regelmäßig übersehen, weil eine Anbindung wie eine technische Einstellung aussieht. Sie ist aber der Moment, in dem Daten aus einem Zusammenhang in einen anderen wandern — und genau das ist der Vorgang, den das Datenschutzrecht reguliert.

## Zweckänderung ist der eigentliche Punkt

Die Daten in den Quellsystemen wurden zu einem bestimmten Zweck erhoben. Anmeldedaten dienen der Zugangskontrolle, Rechnungsdaten der Buchhaltung, Auslagen der Erstattung.

Sie für Governance auszuwerten, ist ein **anderer Zweck**. Ob das zulässig ist, richtet sich nach Art. 6 Abs. 4 DSGVO — Vereinbarkeit des neuen mit dem ursprünglichen Zweck — oder es braucht eine eigene Grundlage.

Die Prüfung ist meist zu bestehen, weil die Zwecke verwandt und die Erwartungen der Betroffenen nicht verletzt sind. Aber sie muss stattfinden und dokumentiert werden. Drei Fragen genügen:

1. Wie weit liegt der neue Zweck vom ursprünglichen entfernt?
2. In welchem Verhältnis stehen Organisation und Betroffene — besteht eine Abhängigkeit?
3. Welche Folgen hat die Auswertung für die Einzelne?

Bei Frage 3 trennt sich die Sache: „Welche Werkzeuge sind im Haus" hat für niemanden Folgen. „Wer benutzt welches Werkzeug" hat sie.

## Datenminimierung, praktisch

Die meisten Anbindungen übernehmen zu viel, weil es einfacher ist, alles zu übertragen als auszuwählen. Vier Fragen je Feld:

| Frage | Konsequenz |
|---|---|
| Brauche ich das Feld für eine Entscheidung? | sonst weglassen |
| Brauche ich den Einzelwert oder genügt die Summe? | dann aggregieren |
| Brauche ich den Namen oder genügt eine Kennung? | dann pseudonymisieren |
| Brauche ich ihn dauerhaft oder für eine Auswertung? | dann befristen |

**Der Regelfall für Governance-Auswertungen ist die Aggregation.** Für die Frage „nutzen wir nicht freigegebene Werkzeuge" braucht niemand eine Namensliste. Ein Zähler je Dienst reicht, um zu handeln — und er reicht auch, um zu erkennen, dass gehandelt werden muss.

Wo ein Personenbezug wirklich nötig ist, etwa bei verwaisten Zuständigkeiten, ist er auf das eine Feld zu begrenzen, das die Aufgabe trägt.

## Die Stelle, an der es regelmäßig schiefgeht

**Freitextfelder.** Ein Ticket, eine Beschreibung, ein Kommentar — dort steht, was Menschen hineinschreiben, und das schließt Gesundheitsangaben, Beschwerden über Kollegen und ganze Kundenfälle ein.

Wer Tickets in ein Governance-Register übernimmt, übernimmt diese Felder mit. Zwei Auswege: Freitext nicht übernehmen und nur verweisen, oder ihn übernehmen und das Zielsystem auf demselben Schutzniveau betreiben wie das Quellsystem. Der erste ist fast immer der richtige.

## Aufbewahrung über Systemgrenzen

Ein Datensatz, der in zwei Systemen liegt, hat zwei Löschfristen — und gelöscht ist er erst, wenn beide abgelaufen sind und beide Löschungen tatsächlich stattfinden.

Das ist der häufigste Grund, warum Löschkonzepte scheitern: Die Kopie im nachgelagerten System steht in keinem Verzeichnis, also löscht sie niemand.

Drei Festlegungen je Anbindung:

- **Welche Frist gilt im Zielsystem** — sie kann kürzer sein als im Quellsystem, aber selten länger begründbar
- **Was passiert, wenn im Quellsystem gelöscht wird** — wird die Löschung mitgeführt, oder bleibt die Kopie liegen
- **Wie wird eine Betroffenenanfrage beantwortet** — die Person muss in beiden Systemen gefunden werden, sonst ist die Auskunft unvollständig

Der zweite Punkt hat eine unangenehme Seite: Eine Anbindung, die Löschungen **nicht** mitführt, hebt jede Löschung im Quellsystem faktisch auf.

## Mitbestimmung

Sobald eine Anbindung Daten verarbeitet, die Verhalten oder Leistung einzelner Beschäftigter erkennbar machen, ist in Deutschland regelmäßig der Betriebsrat zu beteiligen — und zwar bevor die Anbindung läuft, nicht danach.

Betroffen sind vor allem:

- Netz- und Proxyprotokolle
- Anmelde- und Nutzungszeitpunkte
- Auslagen und Kartenumsätze
- Protokolle darüber, wer wie oft eine Ausgabe überstimmt hat

Der letzte Punkt ist der bittere: Genau die Kennzahl, die die Wirksamkeit der menschlichen Aufsicht belegt, ist zugleich eine Leistungskennzahl über einzelne Personen. Der gangbare Weg ist die Auswertung auf Gruppenebene, verbunden mit der ausdrücklichen Zusage, sie nicht zur individuellen Bewertung zu verwenden. Diese Zusage gehört in eine Vereinbarung, nicht in eine Zusicherung.

## Wenn die Anbindung über einen Dritten läuft

Ein Werkzeug, das im Auftrag Daten aus mehreren Systemen zusammenführt, ist Auftragsverarbeiter. Erforderlich sind ein Vertrag nach Art. 28, die Benennung der Unterauftragsverarbeiter, Klarheit über den Verarbeitungsort und ein Weisungsrecht, das auch die Löschung umfasst.

Zwei Punkte, die in dieser Konstellation besonders zählen:

- **Was passiert am Ende des Vertrags** mit den zusammengeführten Daten — Rückgabe oder Löschung, nachweisbar
- **Wer sieht die Daten beim Dienstleister** — die Zusammenführung erzeugt regelmäßig einen aussagekräftigeren Datenbestand als jedes Quellsystem für sich

Der zweite Punkt ist der eigentliche Grund, warum Zusammenführung ein eigenes Risiko ist und nicht die Summe der Einzelrisiken.

## Sicherheit, kurz

Drei Dinge, die bei Governance-Anbindungen auffällig oft fehlen:

**Eigene Zugangsdaten je Anbindung**, nicht das Konto einer Person. Sonst endet die Anbindung, wenn die Person geht — und bis dahin handelt sie unter deren Namen, was jede Protokollauswertung wertlos macht.

**Lesende Rechte, wo lesend genügt.** Ein Abgleich, der nur liest, braucht keine Schreibrechte, auch wenn sie bequemer wären.

**Protokollierung der Anbindung selbst.** Wann lief sie, was hat sie übertragen, was hat sie geändert. Ohne das lässt sich nach einem Fehler nicht rekonstruieren, welche Daten woher stammen.

## Verwandtes

- [Woher die Daten kommen](./governance-signale.md)
- [Vier Muster](./schnittstellen-muster.md)
- Grundlagen zu Verzeichnis und Rechtsgrundlagen: [DSGVO-Arbeitsbereich](https://github.com/SimpleAct-Compliance/simpleact-gdpr-compliance-workspace)

---

Keine Rechtsberatung. Stand: September 2026.
