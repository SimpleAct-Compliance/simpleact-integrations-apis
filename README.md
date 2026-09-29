# Governance anschließen: Register, die sich selbst füllen

**Ein KI-Inventar, das von Hand gepflegt wird, ist nach sechs Monaten falsch.** Nicht weil jemand nachlässig ist, sondern weil die Wirklichkeit in anderen Systemen entsteht — in der Beschaffung, im Verzeichnisdienst, im Ticketsystem, in der Kreditkartenabrechnung. Dieses Repository beschreibt, woher Governance-Daten tatsächlich kommen und wie man sie anbindet, ohne dabei ein zweites Datenschutzproblem zu bauen.

*Where AI governance data actually comes from, and how to connect existing systems to a register without creating a second data protection problem.*

---

## Das Problem

Jedes Governance-Vorhaben beginnt mit einer Bestandsaufnahme. Die meisten enden auch dort. Ein halbes Jahr später stimmt das Inventar nicht mehr, und niemand merkt es — bis eine Prüfung, ein Vorfall oder eine Auskunftsanfrage die Lücke aufdeckt.

Die Ursache ist nicht Disziplin. Sie ist strukturell:

> **Die Ereignisse, die ein Register veralten lassen, passieren nicht im Register.**

Ein Fachbereich abonniert ein Werkzeug. Ein Anbieter tauscht ein Modell. Ein Projekt wird eingestellt. Eine Mitarbeiterin wechselt die Rolle und behält Zugriffsrechte. Keines dieser Ereignisse läuft über den Ort, an dem es dokumentiert sein müsste.

Wer das mit einer jährlichen Abfrage lösen will, bekommt einmal im Jahr eine Momentaufnahme und elf Monate Blindheit.

## Der Ansatz

Nicht alles automatisieren — sondern die wenigen Stellen finden, an denen ein vorhandenes System eine Veränderung zuerst sieht, und genau dort einen Fühler setzen.

| Was man wissen will | Wo es zuerst sichtbar wird |
|---|---|
| Ein neues KI-Werkzeug ist im Haus | Beschaffung, Kreditkartenabrechnung, Abonnementverwaltung |
| Jemand nutzt etwas ohne Freigabe | Netzprotokolle, Anmeldedienst, Auslagenerstattung |
| Ein Anbieter hat das Modell gewechselt | Versionsangabe der Schnittstelle, Änderungsverlauf, eigener Testsatz |
| Ein System ist außer Betrieb | Abrechnung, Betriebsüberwachung |
| Eine Aufsicht findet nicht mehr statt | Protokolle des Systems selbst |
| Eine Zuständigkeit ist verwaist | Verzeichnisdienst, Personalstammdaten |

Die dritte Zeile der linken Spalte ist bemerkenswert: **Die Auslagenerstattung ist eines der zuverlässigsten Frühwarnsysteme für nicht freigegebene Werkzeuge**, die eine Organisation besitzt — und sie kostet nichts, weil die Daten ohnehin anfallen.

## Vier Muster, mehr braucht es nicht

| Muster | Richtung | Wofür |
|---|---|---|
| **Abgleich** | herein | Inventar aktuell halten: Systeme, Anbieter, Zuständigkeiten |
| **Ereigniskanal** | herein | Vorfälle und Auffälligkeiten dort melden, wo Menschen ohnehin sind |
| **Protokollzugang** | herein | Belege für Aufsicht und Aufarbeitung, ohne sie zu kopieren |
| **Nachweisausgabe** | hinaus | Register in ein prüfbares Dokument überführen |

Alles Weitere ist meist Sonderfall. Wer mit diesen vier anfängt und jedes einzeln abnimmt, hat mehr erreicht als mit einer großen Plattformintegration, die nach dem ersten Feldnamenwechsel stillsteht.

## Die unbequeme Regel

**Eine Schnittstelle ist eine Verarbeitungstätigkeit.**

Sie hat einen Zweck, eine Rechtsgrundlage, Empfänger und eine Aufbewahrung. Wer ein Governance-Werkzeug an den Verzeichnisdienst hängt und dabei Namen, Rollen und Anmeldezeitpunkte übernimmt, hat eine neue Verarbeitung personenbezogener Daten begonnen — mit Beteiligung des Betriebsrats, wenn es um Verhaltens- oder Leistungskontrolle gehen könnte.

Das ist kein Argument gegen Anbindung. Es ist ein Argument dafür, sie wie eine Verarbeitung zu behandeln und nicht wie eine Konfiguration.

## Inhalt

| Dokument | Inhalt |
|---|---|
| [Woher die Daten kommen](./knowledge-base/governance-signale.md) | Elf Quellen, was sie liefern, was sie nicht liefern, wie zuverlässig sie sind |
| [Vier Muster](./knowledge-base/schnittstellen-muster.md) | Abgleich, Ereigniskanal, Protokollzugang, Nachweisausgabe — mit den Fallstricken je Muster |
| [Datenschutz in der Schnittstelle](./knowledge-base/datenschutz-in-schnittstellen.md) | Datenminimierung, Aufbewahrung über Systemgrenzen, Mitbestimmung, Auftragsverarbeitung |
| [Vorlage: Schnittstellensteckbrief](./templates/schnittstellensteckbrief.md) | Ein Blatt je Anbindung |
| [Vorlage: Abnahme](./templates/integrationsabnahme.md) | Bevor eine Anbindung in Betrieb geht |

## Was hier nicht steht

Keine Produktschnittstelle, kein Endpunktverzeichnis, kein Beispielcode für ein bestimmtes System. Die Feldnamen ändern sich, die Fragen nicht. Wer die Schnittstellenbeschreibung eines konkreten Werkzeugs sucht, findet sie bei dessen Anbieter — für SimpleAct unter [simpleact.de](https://simpleact.de).

## Stand und Lizenz

Zuletzt aktualisiert: 2026-09-29 · MIT — frei nutzbar, auch kommerziell. Keine Rechtsberatung.
