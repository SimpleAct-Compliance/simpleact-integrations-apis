# Woher die Daten kommen

## Die Reihenfolge, in der man suchen sollte

Nicht jede Quelle lohnt die Anbindung. Drei Fragen entscheiden:

1. **Sieht sie eine Veränderung zuerst?** Eine Quelle, die erst nach dem Inventar aktualisiert wird, hilft nicht.
2. **Ist ihr Inhalt belastbar?** Eine Liste, die jemand pflegt, hat dieselbe Schwäche wie das Inventar selbst.
3. **Lässt sich der Personenbezug begrenzen?** Manche Quellen liefern Gold und Sprengstoff im selben Datensatz.

Die folgenden elf Quellen sind nach dem Verhältnis von Nutzen zu Aufwand sortiert, nicht nach Vollständigkeit.

---

## 1. Beschaffung und Kreditorenbuchhaltung

**Liefert:** neue Anbieter, Vertragsbeginn und -ende, Tarif, Kostenstelle, verantwortliche Person.

Die wertvollste Quelle überhaupt, weil fast jedes eingekaufte KI-Werkzeug irgendwann eine Rechnung erzeugt. Sie sieht auch das, was niemand als KI-Projekt angemeldet hat.

**Liefert nicht:** ob das Produkt überhaupt KI enthält. Das steht selten im Rechnungstext und muss einmalig zugeordnet werden.

**Praktisch:** Ein Abgleich der Kreditorenliste gegen eine gepflegte Liste bekannter KI-Anbieter findet in der ersten Runde regelmäßig Werkzeuge, die im Inventar fehlen. Das ist eine Abfrage, kein Projekt.

## 2. Auslagenerstattung und Firmenkreditkarten

**Liefert:** Werkzeuge, die an der Beschaffung vorbei bezogen wurden — Einzelabonnements, die jemand privat auslegt und erstattet bekommt.

Die zuverlässigste Spur für Schatten-KI, und die am häufigsten übersehene. Wer wissen will, was im Haus tatsächlich benutzt wird, findet es hier eher als in einer Umfrage.

**Vorsicht:** Diese Daten sind personenbezogen und betreffen das Verhalten einzelner Beschäftigter. Die Auswertung braucht eine Rechtsgrundlage, eine klare Zweckbindung und in aller Regel die Einbindung der Mitbestimmung. Sinnvoll ist eine **aggregierte** Auswertung nach Anbieter, nicht nach Person — die Frage lautet „welche Werkzeuge sind im Haus", nicht „wer benutzt was".

## 3. Anmeldedienst und Verzeichnis

**Liefert:** welche Anwendungen über die zentrale Anmeldung angebunden sind, wer welche Rolle hat, wann eine Anwendung zuletzt genutzt wurde, verwaiste Konten.

Gut geeignet, um Zuständigkeiten aktuell zu halten: Wenn die im Inventar als verantwortlich eingetragene Person das Unternehmen verlassen hat, weiß der Verzeichnisdienst es zuerst.

**Liefert nicht:** alles, was ohne zentrale Anmeldung läuft — also gerade die Werkzeuge, um die es meistens geht.

## 4. Netzprotokolle, Proxy, Namensauflösung

**Liefert:** Zugriffe auf bekannte KI-Dienste, auch ohne Vertrag und ohne Anmeldung.

Die einzige Quelle, die vollständig unbekannte Nutzung findet.

**Vorsicht:** die heikelste Quelle überhaupt. Verbindungsdaten einzelner Beschäftigter sind ohne Weiteres Verhaltenskontrolle. Brauchbar ist fast ausschließlich die **aggregierte** Auswertung: welche Dienste werden kontaktiert, wie oft, aus welchem Bereich — ohne Rückführung auf Personen. Ohne Mitbestimmung und ohne dokumentierte Zweckbindung sollte diese Quelle nicht angefasst werden.

## 5. Ticket- und Aufgabensysteme

**Liefert:** den Ereigniskanal. Menschen melden dort ohnehin, was nicht funktioniert.

Der praktische Wert liegt weniger im Auslesen als im Umgekehrten: Wer das Melden einer KI-Auffälligkeit dorthin legt, wo die Leute ohnehin sind, bekommt Meldungen. Wer ein separates Formular baut, bekommt Stille.

**Achtung auf die Abgrenzung:** Ein Ticket ist keine Vorfallmeldung im Sinne der Meldepflichten. Es ist der Eingang. Die Bewertung, ob daraus eine Meldung folgt, bleibt ein eigener Schritt — siehe [Incident Management](https://github.com/SimpleAct-Compliance/simpleact-incident-management).

## 6. Vertragsverwaltung

**Liefert:** AVV-Bestand, Laufzeiten, Kündigungsfristen, Unterauftragsverarbeiter, Änderungsmitteilungen.

Der natürliche Partner des Anbieterregisters. Besonders wertvoll ist die Kündigungsfrist: Sie ist der letzte Zeitpunkt, zu dem eine Neubewertung noch eine Konsequenz haben kann.

## 7. Das KI-System selbst

**Liefert:** Protokolle über Ausgaben, Eingriffe, Ablehnungen, Modellversion, Fehlerquoten.

Die einzige Quelle, die etwas über **Wirksamkeit** sagt. Aus ihr kommt die Kennzahl, die mehr verrät als jede Selbstauskunft: wie oft eine Ausgabe tatsächlich überstimmt wurde.

**Liefert oft nicht, was man braucht:** Der Zugang zu Protokollen ist eine Vertragsfrage. Wer ihn nicht in der Beschaffung geklärt hat, bekommt ihn im Betrieb nicht mehr.

## 8. Versions- und Auslieferungssysteme

**Liefert:** bei selbst entwickelten Systemen Modellversion, Abhängigkeiten, Auslieferungszeitpunkte.

Damit die Antwort auf die Frage, die nach einem Vorfall immer gestellt wird: Welcher Stand war zum Zeitpunkt X in Betrieb?

## 9. Personalstammdaten

**Liefert:** Rollen, Eintritte, Austritte, Wechsel — die Auslöser für Schulungen und für die Neuzuweisung von Zuständigkeiten.

**Liefert nicht:** Leiharbeitskräfte, freie Mitarbeiter, Auftragnehmer. Genau die Gruppe, die bei der Kompetenzpflicht regelmäßig fehlt.

## 10. Betriebsüberwachung

**Liefert:** ob ein System überhaupt noch läuft, Verfügbarkeit, Antwortzeiten, Fehlerraten.

Nützlich vor allem zur Bereinigung: Systeme, die seit Monaten keinen Verkehr haben, gehören entweder abgeschaltet oder ausgetragen.

## 11. Kundendienst

**Liefert:** Beschwerden über automatisierte Entscheidungen, Widersprüche, Auskunftsanfragen — oft bevor sie als solche erkannt werden.

Eine Anfrage nach Art. 15 DSGVO kommt selten mit dem Wort „Auskunft". Sie kommt als Beschwerde. Wer im Kundendienst nicht erkennt, was das ist, lässt eine Frist laufen.

---

## Was sich daraus bauen lässt

Eine kleine Zahl von Prüfungen, die jeweils zwei Quellen gegeneinanderhalten. Sie finden mehr als jede Einzelauswertung:

| Prüfung | Quelle A | Quelle B | Findet |
|---|---|---|---|
| Anbieter ohne Inventareintrag | Kreditorenliste | KI-Inventar | eingekaufte, nicht erfasste Systeme |
| Anbieter ohne AVV | Anbieterregister | Vertragsverwaltung | Vertragslücken |
| System ohne verantwortliche Person | KI-Inventar | Verzeichnisdienst | verwaiste Zuständigkeiten |
| Aufsicht ohne Eingriffe | Systemprotokolle | Schulungsstand | formale statt tatsächlicher Aufsicht |
| Dienst ohne Freigabe | Netzprotokolle (aggregiert) | Liste freigegebener Werkzeuge | Schatten-KI |
| System ohne Nutzung | Betriebsüberwachung | KI-Inventar | Karteileichen |

Jede dieser Zeilen ist eine Abfrage, die sich monatlich wiederholen lässt. Zusammen ersetzen sie die jährliche Umfrage, die ohnehin niemand ernst beantwortet.

## Verwandtes

- [Vier Muster](./schnittstellen-muster.md)
- [Datenschutz in der Schnittstelle](./datenschutz-in-schnittstellen.md)

---

Keine Rechtsberatung. Stand: September 2026.
