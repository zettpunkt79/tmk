- [Basis-Testmanagementkonzept (MD)](#basis-testmanagementkonzept-md)
  - [Überblick](#überblick)
    - [Zweck des Dokuments](#zweck-des-dokuments)
      - [Abgrenzung](#abgrenzung)
      - [Geltungsbereich und Pflege](#geltungsbereich-und-pflege)
  - [Umgebungen](#umgebungen)
    - [Entwicklungsumgebung](#entwicklungsumgebung)
    - [Abnahmeumgebung](#abnahmeumgebung)
    - [Produktivumgebung](#produktivumgebung)
  - [Testtypen](#testtypen)
    - [Prüfung von Konzepten](#prüfung-von-konzepten)
    - [Provider-Tests](#provider-tests)
    - [Inbetriebnahmetests](#inbetriebnahmetests)
    - [Abnahmetests](#abnahmetests)
    - [Nicht-funktionale Tests](#nicht-funktionale-tests)
      - [Effizienztests](#effizienztests)
      - [Gebrauchstauglichkeitstests](#gebrauchstauglichkeitstests)
      - [Sicherheitstests](#sicherheitstests)
    - [Regressionstests](#regressionstests)
  - [Rollen](#rollen)
  - [Kommunikation](#kommunikation)
    - [Meetingformate](#meetingformate)
      - [Refinement](#refinement)
      - [Dailys/Weeklys](#dailysweeklys)
      - [Review](#review)
    - [Abstimmung von Abnahmekriterien](#abstimmung-von-abnahmekriterien)
    - [Dokumente](#dokumente)
      - [Release-Notes](#release-notes)
    - [Abstimmung von nicht-funktionalen Tests](#abstimmung-von-nicht-funktionalen-tests)
      - [Bedienbarkeitstest](#bedienbarkeitstest)
      - [Tests auf der Abnahmeumgebung](#tests-auf-der-abnahmeumgebung)
    - [Abweichungs- und Änderungsmanagement](#abweichungs--und-änderungsmanagement)
  - [Ausführungsumgebungen der Testtypen](#ausführungsumgebungen-der-testtypen)
  - [Dokumentation](#dokumentation)
    - [Testkonzept (AN)](#testkonzept-an)
    - [Testfallportfolio (AN) ](#testfallportfolio-an)
    - [Konzept zur Umsetzung (AN)](#konzept-zur-umsetzung-an)
    - [{Testkonzept (AG)}](#testkonzept-ag)
    - [{Testspezifikation (AG)}](#testspezifikation-ag)
    - [{Testbericht (AG)}](#testbericht-ag)
    - [{Testplan (AG)}](#testplan-ag)
  - [Testdaten](#testdaten)
    - [Bereitstellung durch {den Auftraggeber}](#bereitstellung-durch-den-auftraggeber)
    - [Bereitstellung durch Auftragnehmer](#bereitstellung-durch-auftragnehmer)
  - [Abweichungs- und Änderungsmanagement](#abweichungs--und-änderungsmanagement-1)
    - [Abweichungs- und Fehlermanagement während einer Entwicklungsphase](#abweichungs--und-fehlermanagement-während-einer-entwicklungsphase)
    - [Änderungsmanagement während einer Entwicklungsphase](#änderungsmanagementwährend-einer-entwicklungsphase)
    - [Information zur Lieferung](#information-zur-lieferung)
    - [Abweichungs- und Fehlermanagement während der Abnahmetests](#abweichungs--und-fehlermanagement-während-der-abnahmetests)
    - [Änderungsmanagement während der Abnahmetests](#änderungsmanagement-während-der-abnahmetests)
    - [Abweichungs-, Fehler- und Änderungsmanagement nach Inbetriebnahme](#abweichungs--fehler--und-änderungsmanagement-nach-inbetriebnahme)

# Basis-Testmanagementkonzept (MD)

Änderungshistorie

| Datum   | Beschreibung           | Autor   |
| ------- | ---------------------- | ------- |
| {Datum} | {Versionsbeschreibung} | {Autor} |

## Überblick

### Zweck des Dokuments

Das Ziel dieses Dokuments ist es, einen umfassenden und vollständigen Überblick über alle erforderlichen Testaktivitäten zu geben, die beim Aufsetzen und Erweitern des neu zu entwickelnden {Testgegenstandes} nötig sind, um eine hohe Qualität der IT-Lösung zu erzielen. Die Gesamt-IT-Lösung besteht aus {einer technischen Infrastruktur sowie Software}. Die Erstumsetzung umfasst {die Testobjekte}. Erweiterungen erfolgen durch die Umsetzung und Integration weiterer {Testobjekte}.

Das Testmanagementkonzept beschreibt insbesondere die Schnittstellen der Testaktivitäten zwischen {dem Auftraggeber} und {dem Auftragnehmer} auf einem übergeordneten Level. Dieses Dokument bildet die Grundlage und enthält wichtige Leitlinien für die Entwicklung eines vollständigen und ausgereiften Testansatzes für den Aufbau der IT-Lösung sowie für jedes kommende Release. Der Testumfang, der Release-Zyklus und Details zum genauen Testablauf können bezogen auf den jeweiligen Testgegenstand variieren und werden in Folgedokumenten wie dem Testkonzept festgehalten.

Zunächst werden im Dokument die Rahmenbedingungen für die Tests der Gesamt-IT-Lösung, wie Umgebungen und Testtypen geklärt. Darauf folgen Erläuterungen zu wichtigen Rollen und Kommunikationsformen im Kontext der Tests. Daran anschließend werden die Umgebungen und Testtypen den Rollen zugeordnet und in einen zeitlichen Rahmen gesetzt. Das Kapitel über Testdokumente erläutert kurz alle für und durch Tests entstehenden Dokumente. Hierbei werden die Testdaten ausgegliedert, um im Folgenden auf ihre speziellen Erstellungs- und Zusammenarbeitsbedürfnisse einzugehen. Den Abschluss bildet die Kommunikation für Abweichungs- und Änderungsmanagement, in dem sowohl einheitliche Terminologien festgelegt als auch zeitliche Abläufe erläutert werden.

#### Abgrenzung

Dieses Dokument beinhaltet keine konkreten Anforderungen zu den Geschäftsprozessen. Außerdem werden keine konkreten Testansätze der Beteiligten beschrieben. Diese finden sich im Testkonzept sowie in weiteren testbegleitenden Dokumenten wieder. An geeigneter Stelle wird auf diese Dokumente verwiesen.

#### Geltungsbereich und Pflege

Das Dokument wird im Rahmen der Erstumsetzung der Gesamt-IT-Lösung erarbeitet und gilt darüber hinaus für alle folgenden Erweiterungen und Anpassungen der IT-Lösung. Es handelt sich um ein gemeinsames Dokument {des Auftraggebers} und {des Auftragnehmers}. Grundsätzlich wird das Dokument zum Auftakt jedes weiteren Projektes im Rahmen der IT-Lösung geprüft, ggf. angepasst und gemeinsam abgenommen. Änderungen am Dokument während einer Projektlaufzeit können von beiden Seiten initiiert werden und bedürfen der Abstimmung mit dem jeweiligen Gegenüber

## Umgebungen

Um die Funktionalität und Qualität neu implementierter Funktionen vor dem Einsatz im Produktivsystem sicherzustellen, kommen mehrere Umgebungen zum Einsatz, um Testfälle mit bestimmten Testzielen durchzuführen. Im Folgenden werden die verschiedenen Umgebungen mit ihren Eigenschaften beschrieben.

### Entwicklungsumgebung

Die Entwicklungsumgebung ist die hausinterne Umgebung {des Auftragnehmers}. Sie stellt die Ausführungsumgebung für die Testaktivitäten dar, die {der Auftragnehmer} vor der Lieferung auf die Abnahmeumgebung ausführt, mit dem Ziel, Fehlerzustände frühzeitig bereits im Entwicklungsprozess zu erkennen und zu beheben.

Die Entwicklungsumgebung wird {beim Auftragnehmer} auf Basis von virtuellen Maschinen möglichst nah an der Zielarchitektur aufgebaut.

{Platzhalter für Unterschiede zu den übrigen Umgebungen}

### Abnahmeumgebung

Die Abnahme-/Staging-Umgebung gehört zur Infrastruktur {des Auftraggebers} und wird {vom Auftragnehmer} gehostet und beliefert. Sie dient der Prüfung von Zwischenergebnissen und ermöglicht Abnahmetests {des Auftragnehmers} vor Installationen auf dem Produktivsystem.

{Platzhalter für Unterschiede zu den übrigen Umgebungen}

{Platzhalter für das Thema „Übernahme von Produktivdaten in die Abnahmeumgebung“}

{Platzhalter für das Thema „Gibt es eine vergleichbare Zonentrennung wie in der Prod-Umgebung?“}

### Produktivumgebung

Diese Ablaufumgebung ist für den Produktivbetrieb der IT-Lösung vorgesehen und gehört {dem Auftraggeber}. Als Bestandteil der Gesamtinfrastruktur erfolgt das Hosting durch {den Auftragnehmer}. Testaktivitäten sind hier nur eingeschränkt vorgesehen, beispielsweise in Form von Inbetriebnahmetests.

## Testtypen

Über den Lebenszyklus einer IT-Lösung werden Tests mit unterschiedlichem Fokus und in unterschiedlicher Verantwortung beschrieben und ausgeführt. Diese Tests sind in einem größeren Zusammenhang nach Hauptaugenmerk, Ausführungsumgebung oder den verwendeten Testdaten gruppierbar, mit dem Ziel, die Planung und Verantwortungsklärung zu erleichtern. Für die Planung, Dokumentation und Kommunikation zu den Testaktivitäten der IT-Lösung {des Auftraggebers} werden die nachfolgenden, einheitlichen Testtypen vereinbart.

### Prüfung von Konzepten

Unter der Prüfung von Konzepten, wie Anforderungen, Designkonzepten, Testkonzepten oder dem Styleguide, wird hier eine Kontroll- und Review-Möglichkeit durch den jeweiligen Partner verstanden. Konzepte, welche durch {den Auftraggeber} erstellt werden, werden für eine bessere Transparenz an {den Auftragnehmer} übergeben. {Der Auftragnehmer} erhält die Möglichkeit, diese zu prüfen und mit Anmerkungen an {den Auftragnehmer} zu übergeben. Gleiches gilt für die Konzepte, die durch {den Auftragnehmer} erstellt werden. Hier erhält {der Auftraggeber} eine Review-Möglichkeit.

Grundsätzlich kann der Prüfungsprozess für die verschiedenen Dokumente unterschiedlich gestaltet werden. Denkbar sind hier die

- Erarbeitung durch eine Partei und Übergabe zum Review an die zweite
- Erarbeitung eines Entwurfes und Übergabe an die andere Partei um die Fertigstellung gemeinsam zu gestalten
- Gemeinsame Erarbeitung, z.B. über Meeting-Formate (s. {Kapitel 5: Kommunikation})

Die Art des gewählten Prozesses hängt insbesondere davon ab, ob das zu erstellende Dokument durch die andere Seite abnahmepflichtig ist und wie viel Inhaltsanteil durch sie beigesteuert wird.

Daher wird der jeweilige Prozess für jede Dokumentart einzeln festgelegt und kann im Projektablauf auch innerhalb einer Konzeptart wechseln. Die Abstimmung hierzu erfolgt in den gemeinsamen Terminen und gehört in den Verantwortungsbereich des Projektmanagements.

### Provider-Tests

Der Provider-Test umfasst die Kernaktivitäten, mit denen ein Infrastruktur- oder Softwareanbieter die Korrektheit der IT-Landschaft bzw. der Software vor der Übergabe an den Kunden überprüft. {Beim Auftragnehmer} werden diese auf der Entwicklungsumgebung durchgeführt.

Typischerweise bestehen Provider-Tests aus den folgenden Teststufen:

- Unit-Tests
- Komponententests
- Integrationstests
- Systemtests

Inhalt und Durchführung von Provider-Tests liegen in der alleinigen Verantwortung {des Auftragnehmers}. Die Dokumentation der Testausführungen wird {dem Auftraggeber} bei Bedarf zur Verfügung gestellt. {Beim Auftragnehmer} sind die Testprotokolle der anforderungsbasierten Tests Bestandteil der Endlieferung.

### Inbetriebnahmetests

Die Inbetriebnahmetests (Anlauftests) bestehen aus verschiedenen Teilen und werden in allen Umgebungen durchgeführt:

1. Der technische Inbetriebnahmetest stellt die korrekte Konfiguration von Hardware und Installation der Software sicher, dies umfasst
   - Kommunikation von Hardwarekomponenten prüfen
   - Protokolldateien prüfen
   - Servicestatus prüfen
2. Der funktionale Inbetriebnahmetest stellt die Verfügbarkeit von Geschäftsprozessen sicher, dazu gehören
   - Verarbeitung und Verteilung von Daten
3. Der Berechtigungstest stellt die Konfiguration der Benutzer- und Zugriffsrechte sicher
4. Die umgebungsbezogenen Provider-Tests stellen das korrekte Verhalten neuer Komponenten sicher, die auf der Entwicklungsumgebung nicht testbar sind. Dies gilt insbesondere für:
   - umgebungsgebundene Hardwarekomponenten
   - Schnittstellenfunktionen ohne Mock-Möglichkeit

### Abnahmetests

Das Hauptaugenmerk von funktionalen Abnahmetests besteht darin, die funktionale Korrektheit der neu implementierten Funktionen und Komponenten zu überprüfen und sicherzustellen, dass sie unter Berücksichtigung der Anwendungsfälle korrekt alle Daten verarbeiten. Der Abnahmetest besteht daher hauptsächlich aus funktionalen Testfällen, die auf den vereinbarten Anforderungen basieren und in ihrer Struktur den Anwendungsfällen folgen. Die Basis für die Abnahmetests des Auftraggebers bilden die an das IT-System gestellten Anforderungen. Die Umsetzung erfolgt in Epics.

Wann einzelne Epics geplant in die Umsetzung gehen und dem Auftraggeber voraussichtlich zum Abnahmetest zur Verfügung stehen, kann dem Release-Plan (Big Picture) entnommen werden. Epics werden mindestens in Form von T-Shirt-Größen geschätzt, die eine grobe Indikation über den zu erwartenden zeitlichen Aufwand geben sollen. Die T-Shirt-Größe XS entspricht einem halben Personentag. Der Aufwand verdoppelt sich je zunehmeder T-Shirt-Größe. S entspricht demnach einen Tag, M zwei Tagen, usw. Die Schätzung wird weiter verfeinert, je näher ein Epic an seine Umsetzung rückt.

Welche Epics im Kontext eines Releases umgesetzt wurden und zum Abnahmetest zur Verfügung stehen, kann außerdem den Release-Notes entnommen werden.

Typischerweise können die Abnahmetests umfassen:

- Test der funktionalen / fachlichen Anforderungen
- End-to-End-Tests von Geschäftsprozessen
- GUI-Tests
- Autorisierungstests

Zusätzlich können auch Tests mit einem technischen Schwerpunkt ausgeführt werden:

- Test der technischen Anforderungen zu Datentransfer und -verarbeitung, Korrektheit der Datenspeicherung
- Integrationstests
- Migrationstests
- Konfigurationstests, die nicht durch Inbetriebnahmetests abgedeckt sind
- Korrekte Umsetzung von Sicherheitsmaßnahmen, z.B. Firewall, Zugriffsrollen, Ports

Der Umfang eines Abnahmetests kann von einzelnen Modulen bis zum Gesamtsystem variieren. Welchen Umfang ein Testlauf einnimmt, legt {der Auftraggeber} selber fest und kann dies auch von Lieferung zu Lieferung neu entscheiden.

(i) Hinweis: Ein Abnahmetest ist nicht gleichzusetzen mit einer Abnahme im Sinne einer Rechtshandlung. Abnahmetests können aber vom Auftraggeber als Entscheidungsgrundlage für die Abnahme im Sinne einer Rechtshandlung herangezogen werden.

### Nicht-funktionale Tests

Nicht-funktionale Tests sichern ab, wie das System die an es gestellten Funktionen erfüllt. Im Rahmen der Web-Anwendungen werden die Testuntergruppen Effizienztests, Gebrauchstauglichkeitstests und Sicherheitstests vereinbart.

#### Effizienztests

Effizienztests werden durchgeführt, um festzustellen, wie das System (bzw. ein Systembestandteil) unter einer bestimmten Arbeitsbelastung in Bezug auf Reaktionsfähigkeit und Stabilität abschneidet. Er stellt die nicht-funktionalen Anforderungen in Bezug auf die Effizienz sicher. Diese Tests werden in der Regel in der Abnahmeumgebung durchgeführt.

Typische Testziele sind:

- Systemverfügbarkeit unter Last
- Reaktionszeit für den Benutzer
- Auffinden von Engpässen in der Anwendung und Infrastruktur

Wir unterscheiden zwischen verschiedenen Testvarianten, d.h.:

- Performance-Test: ist ein Teil des Effizienztests, der insbesondere die Antwortzeiten zeitkritischer Funktionen überprüft. Performance-Test sollten unter optimalen Bedingungen durchgeführt werden, d.h. immer zur gleichen Zeit und ausschließlich.
- Last-/Stresstest: Der Lasttest ist ein Teil des Effizienztests zum Testen eines Systems gegen eine erwartete maximale Last, beginnend mit dem Einzelnutzertest bis zum Mehrnutzertest oder beginnend mit einer kleinen Datenmenge bis zur maximal vereinbarten Datenmenge. Der Stresstest prüft das System über das definierte Maximum hinaus.

#### Gebrauchstauglichkeitstests

Die Tests zur Gebrauchstauglichkeit messen den Grad der Nutzbarkeit, in dem definierte Benutzer ein bestimmtes Ziel effizient und zufrieden mit dem System lösen können. Die Gebrauchstauglichkeit einer Software wird unter verschiedenen Gesichtspunkten betrachtet.

Im Rahmen der I-Lösung werden folgende Testziele maßgeblich verfolgt:

- stimmiges Layout zum Styleguide des Auftraggebers
- einfache Bedienung
- Barrierearmut

Dazu unterscheiden wir drei Testvarianten.

1. Layouttest: Die Prüfung der Konzepte und umgesetzten Artefakte erfolgt insbesondere unter dem Gesichtspunkt, dass das Layout dem Styleguide des Auftraggebers folgt. Außerdem werden die Anwendungen bei Ausführung auf Einhaltung der Konzepte überprüft.
2. Bedienbarkeitstests: Während dieser Tests wird die Anwendung auf die in der Leistungsbeschreibung hervorgehobenen Merkmale einfacher Bedienoberflächen durch Nutzung geprüft. Dieser Test ist in zwei Varianten vorgesehen:
   - Eine Prüfung durch einzelne Mitarbeiter {des Auftragnehmers}, um frühzeitig Probleme zu erkennen
   - Eine Prüfung in Zusammenarbeit mit Mitarbeitern {des Auftraggebers}
3. Barrierearmut: Um die Bedienung der Anwendungen für alle gewünschten Nutzer abzusichern, werden hier folgende Punkte geprüft:
   - vollständige Tastaturbedienbarkeit der Weboberfläche
   - Skalierbarkeit von Bildschirminhalten (Schriftgröße)
   - Einstellbarkeit verschiedener Farbschemata

#### Sicherheitstests

Das Thema IT-Sicherheit wird bereits bei der Konzeption der Systemarchitektur, dem Infrastrukturrahmen und der Softwareanwendung berücksichtigt („Security by design“). Einzelheiten, wie konkrete Sicherheitsaspekte berücksichtigt werden können {der Richtlinie} entnommen werden.

Die Themen der Richtlinie beinhalten u.a.:

- Die Zugriffskontrolle von Gebäuden, des Rechenzentrums und personalisierter Arbeitsrechner
- Verschlüsselungen
- Zertifikats-, Identity-, und Credentials-Management
- Patch und Schwachstellen -Management
- Firewalls und Virenschutz
- Zugriffe auf API-Gateways, CI- und Collab-Systeme
- Authentifizierung und -Autorisierung

Technische Maßnahmen, wie die Installation und Konfiguration von Virenschutz- und Firewall-Software obliegen den umsetzenden Fachabteilungen des Auftragnehmers und können dem Auftraggeber durch entsprechende Protokolle auf Anfrage belegt werden. Gleiches gilt für Verfahren zur statischen Codeanalyse mit dem Ziel, Sicherheitsschwachstellen frühzeitig aufzudecken und zu schließen.

Durch den Auftraggeber kann im Bedarfsfall ein Penetrationstest zur gezielten Suche nach Sicherheitslücken vorgenommen werden.

### Regressionstests

Regressionstests werden üblicherweise im Rahmen der Entwicklung auf der Entwicklungsumgebung und bei den Abnahmetests auf der Abnahmeumgebung durchgeführt. Ziel ist es, sicherzustellen, dass zuvor entwickelte und getestete Software auch dann noch die gleiche Leistung erbringt, wenn sie durch neu implementierte Funktionen oder Komponenten geändert oder mit neuen Schnittstellen versehen wird.

Aus Release-bezogenen Testfällen oder eigens für die Regression entworfenen Tests wird eine fortlaufend erweiterte Testfallsammlung erstellt. Diese beinhaltet hauptsächlich funktionale Positivtests, die in der Regel nicht bei jeder Lieferung vollständig ausgeführt werden. Die Auswahl erfolgt unter Berücksichtigung der aktuellen Lieferobjekte. Um die Testausführungszeit zu reduzieren, besteht eine der Anforderungen an den Regressionstest darin, die Testautomatisierung sinnvoll zu maximieren.

## Rollen

Die folgende Tabelle veranschaulicht die Zuordnung der verschiedenen Projektrollen zu ihren individuellen Testaktivitäten.

AG = Auftraggeber
AN = Auftragnehmer

| Rolle                                                 | Aufgabe                                                   | Zuständigkeit |
| ----------------------------------------------------- | --------------------------------------------------------- | ------------- |
| Projektleitung                                        | Initiierung Testaktivitäten (bei wichtigen Meilensteinen) | AG            |
| Projektleitung                                        | Abstimmung Testkoordination AN (auf Abnahmeebene)         | AG            |
| Testmanager                                           | Initiierung/ Begleitung Testaktivitäten                   | AG            |
| Testmanager                                           | Abstimmung Testkoordination AN                            | AG            |
| Testmanager                                           | Freigabe von Fehlermeldungen                              | AG            |
| Testmanager                                           | Übergabe der konsolidierten Fehlerliste                   | AG            |
| Qualitätssicherung                                    | interne Testaufgaben AG                                   | AG            |
| Qualitätssicherung                                    | Übergabe der Abnahmeprotokolle                            | AG            |
| Datenkonzeption und zentrale Datenqualtitätssicherung | Erstellen und Koordinieren der Testdaten/-struktur        | AG            |
| Test Engineer                                         | Entwicklung Testkonzept                                   | AN            |
| Test Engineer                                         | Testdesign                                                | AN            |
| Test Engineer                                         | Testausführung und - dokumentation                        | AN            |
| Test Engineer                                         | Testergebnisanalyse                                       | AN            |
| Test Engineer                                         | Testautomatisierung                                       | AN            |
| Test Engineer                                         | Unterstützung QS für Team                                 | AN            |
| Entwickler                                            | Testergebnisanalyse                                       | AN            |
| Entwickler                                            | Bugfixing                                                 | AN            |
| Projekt Manager/ Test Manager                         | Initiierung Testaktivitäten                               | AN            |
| Projekt Manager/ Test Manager                         | Überwachung und Koordination Testaktivitäten intern       | AN            |
| Projekt Manager/ Test Manager                         | Abstimmung Testkoordination mit AG                        | AN            |
| Projekt Manager/ Test Manager                         | Übergabe Testdokumente                                    | AN            |
| Projekt Manager/ Test Manager                         | Entgegennahme konsolidierte Fehlerliste                   | AN            |
| Systemarchitekt/in                                    | Ansprechpartner für Konzepte                              | AN            |
| Projektleiter/in                                      | Ansprechpartner für Konzepte                              | AN            |
| Projektleiter/in                                      | Ansprechpartner für Umsetzung                             | AN            |
| Lead-Entwickler/in                                    | Ansprechpartner für Umsetzung                             | AN            |
| Lead-Entwickler/in                                    | Testergebnisanalyse                                       | AN            |
| Lead-Entwickler/in                                    | Bugfixing                                                 | AN            |

## Kommunikation

Im Folgenden werden die Rahmenbedingungen für die Kommunikation zu Testthemen festgelegt. Hierzu zählt sowohl die direkte Kommunikation beispielweise im Rahmen von Meeting-Formaten, als auch die Kommunikation über Dokumente und Ticketsysteme.

### Meetingformate

{Der Auftraggeber} hat die Möglichkeit, an verschiedenen Meeting-Formaten teilzunehmen und diese auch für die Kommunikation in Bezug auf Testaktivitäten zu nutzen. Die Teilnahme an den hier genannten Meeting-Formaten ist als optional anzusehen. Eine Teilnahme fördert allerdings die Transparenz und ermöglicht AG und AN gleichermaßen, frühzeitig zu Testthemen in Kontakt zu kommen und Fragen im direkten Dialog zu klären.

#### Refinement

Im zweiwöchentlichen Refinement besteht die Möglichkeit, einen Überblick über die Projektaktivitäten der nächsten 1 ½ Monate zu erhalten. Ein Ziel dieses Termins ist es, transparent zu machen, welche Artefakte absehbar in diesem Zeitfenster umgesetzt, auf dem Abnahmesystem geliefert und vom AG getestet werden können.

#### Dailys/Weeklys

Der AG hat die Möglichkeit, an kurzzyklischen Meeting-Formaten wie Dailys oder Weeklys teilzunehmen. In diesen Terminen überprüft das cross-funktionale Entwicklungsteam seinen Fortschritt in Richtung des Sprint-Ziels und den Trend bei der Abarbeitung der Sprint Backlog-Einträge. Der AG erhält so bereits frühzeitig die Möglichkeit, Einblick in den Entwicklungsfortschritt und die Testaktivitäten des AN zu erhalten und Implikationen für die eigenen Testaktivitäten abzuleiten.

#### Review

Am Ende eines zweiwöchigen Sprints hat der AG die Möglichkeit, am Sprint-Review teilzunehmen. Ziel dieses Termins ist es, dem cross-funktionalen Team die Entwicklungsergebnisse transparent zu machen, indem die entwickelten Artefakte allen Teilnehmenden vorgestellt werden. Der AG hat die Möglichkeit, an diesen Terminen teilzunehmen und so bereits vor der Lieferung einen Eindruck von der Umsetzung zu erhalten und diese im Sinne eines ersten Tests kritisch zu hinterfragen.

### Abstimmung von Abnahmekriterien

Um der Fehlinterpretation von Anforderungen vorzubeugen, müssen mindestens die funktionalen Anforderungen in Form von testbaren Abnahmekriterien konkretisiert werden. Diese Abnahmekriterien bilden die Basis für die Ableitung funktionaler Tests durch den AN. Zeitlich werden die Abnahmekriterien im Kontext der Konzept-Erstellung für ein Epic zwischen AG und AN abgestimmt. Es können je nach Umfang dedizierte Termine oder Workshops dafür vorgesehen werden. Die konkrete Ausgestaltung sollte in den gemeinsamen Terminen besprochen werden und gehört in den Verantwortungsbereich des Projektmanagements. Der Umfang und Zyklus dieser Termine wird sich absehbar je nach Projektphase und Testgegenstand unterscheiden.

Die vereinbarten Abnahmekriterien zu einer Anforderungen werden {im gemeinsamen Confluence-Bereich} festgehalten und der Freigabestatus dokumentiert. Der AN übernimmt die Abnahmekriterien nach der Freigabe an ein Requirement {im gemeisamen Jira} welches den Bezug von der Anforderung zur Umsetzung und zum Test herstellt.

### Dokumente

Grundsätzlich werden die unter "Dokumentation" {Kapitel 8} genannten Dokumente an die jeweilige Gegenseite zur Erhöhung der Transparenz gegeben. Die Übergabe erfolgt via Projektmanagement im Lieferumfang bzw. direkt zwischen Lead QS (AN) und Testmanagement (AG) via E-Mail. Rückmeldungen sollten konsolidiert über die letztgenannten Personen erfolgen.

#### Release-Notes

Im Zuge der Zwischen-Lieferungen erhält der AG Release-Notes, die den Inhalt der Lieferung transparent machen im Hinblick auf die darin umgesetzten Anforderungen und die darin behobenen, vom AG gemeldeten Fehler. Ebenfalls enthalten sind Hinweise, die die Testaktivitäten des AG einschränken können, beispielsweise bekannte Fehler oder Bestandteile der Lieferung, wie Mockobjekte, die nicht getestet werden, sondern nur die Testbarkeit der anderen Teile ermöglichen sollen.

### Abstimmung von nicht-funktionalen Tests

#### Bedienbarkeitstest

Im Rahmen der nicht-funktionalen Tests ist ein gemeinsamer Bedienbarkeitstest geplant. Für diesen werden alle benötigten Dokumente (Konzepte, Testspezifikationen, Zeitpläne, etc.) gesondert in Zusammenarbeit erstellt. Ein denkbarer Zeitpunkt für den Bedienbarkeitstest ist die Fertigstellung des MVP (Minimal Valuable Product), da darin die wichtigsten Kernfunktionalitäten bereits zur Verfügung stehen und notwendige Änderungen in der Verfeinerung hin zum ersten produktiven Release berücksichtigt werden können.

#### Tests auf der Abnahmeumgebung

Nicht-funktionale Tests, insbesondere Lasttests oder Sicherheitstests, können Auswirkungen auf die allgemeine Performanz des Systems oder von Systemteilen haben. Außerdem handelt es sich dabei häufig um Tests mit einer längeren Ausführungszeit. Es ist daher wichtig, die Durchführung solcher Tests gesondert abzusprechen, da diese Auswirkungen auf andere Testaktivitäten haben können.

Transparente Ablaufpläne und eine gemeinsame Terminvereinbarung verhindern negative Auswirkungen auf Testergebnisse {des Auftraggebers} oder Lieferungen {vom Auftragnehmer}.

### Abweichungs- und Änderungsmanagement

Die Kommunikation für das Abweichungs- und Änderungsmanagement erfolgt auf Grundlage eines gemeinsam genutzten Ticketsystems. Genaue Definitionen zu den Inhalten der Tickets, Status oder Prioritäten werden unter "Abweichungs- und Änderungsmanagement" {Kapitel 10} festgehalten.

## Ausführungsumgebungen der Testtypen

Aufgrund unterschiedlicher Einflussfaktoren, wie der verfügbaren Zeit, Zugriffsrechten oder der Größe der Umgebung, werden nicht alle Testtypen auf allen Umgebungen vollständig ausgeführt. Grundsätzlich können die Tests innerhalb einer Umgebung parallel stattfinden. Für jeden Liefergegenstand sind die Tests auf den unterschiedlichen Umgebungen in folgender Reihenfolge auszuführen:

- Entwicklungsumgebung
- Abnahmeumgebung
- Produktivumgebung

Die folgende Matrix zeigt, auf welcher Umgebung von wem welche Testtypen ausgeführt werden. Es kann für einen schnellen Überblick verwendet werden, ob ein bestimmter Testtyp auf einer Umgebung Anwendung findet.

|                             | Entwicklungsumgebung | Abnahmeumgebung | Produktivumgebung |
| --------------------------- | -------------------- | --------------- | ----------------- |
| Provider-Test               | AN                   |                 |                   |
| Inbetriebnahmetest          | AN                   | AN, AG          | AN                |
| Abnahmetests                |                      | AG              |                   |
| Zuverlässigkeitstests       | AN                   | AN{1}, AG       | AG{2}             |
| Effizienztests              | AN                   | AN{1}, AG       |                   |
| Gebrauchstauglichkeitstests | AN                   | AG              |                   |
| Regressionstests            | AN                   | AG              |                   |

{1} Aus technischen Gründen kann es für {den Auftragnehmer} erforderlich sein, einige nicht-funktionale Tests auf der Abnahmeumgebung auszuführen. Dies ist optional und erfolgt nur mit vorheriger Abstimmung mit dem Auftraggeber.

{2} Die auf der Produktivumgebung durchgeführten Zuverlässigkeitstests des Auftraggebers wurden im Phasenplan nicht berücksichtigt, da es sich um Betriebstests handelt.

## Dokumentation

Dieses Kapitel beinhaltet einen Überblick der Testdokumente, welche für das IT-Gesamtprojekt erstellt werden. Dabei wird für jedes Dokument der Inhaltsschwerpunkt wiedergegeben und die Verantwortung festgelegt.

### Testkonzept (AN)

Das Testkonzept beschreibt das konzeptionelle Vorgehen zum Test einer Applikation oder Infrastruktur und seiner Komponenten durch {den Auftragnehmer}. Dies umfasst alle Testarten bis einschließlich Systemtest, jedoch nicht den Abnahmetest des Kunden. Es wird lediglich das auf das Projekt bezogene Testen beschrieben, nicht der Regelbetrieb. Es wird mindestens ein Testkonzept auf der Ebene der Gesamt-IT-Lösung erstellt, welches Release-übergreifend genutzt wird.

Das Dokument klärt insbesondere folgende Punkte (Auszug):

- Testobjekte (zu testende und nicht zu testende Leistungsmerkmale)
- Testarten in Teststufen
- weiterführende Testdokumente wie das Testfallportfolio (nachfolgend erläutert)
- Kriterien für Testaktivitäten
- Pflege der Dokumente
- Verantwortlichkeiten

Das Testkonzept richtet sich nach den Prozessen {des Auftragnehmers }und liegt in {dessen} Verantwortungsbereich. Das Dokument wird zur Vergrößerung der Transparenz im gemeinsamen Wissensmanagementtool {Confluence} hinterlegt.

### Testfallportfolio (AN) 

{Der Auftragnehmer} entwirft im Rahmen der Umsetzung verschiedene Arten von Tests. Hierzu zählen verschiedene Testarten zu den unter Provider-Tests {Kapitel 3.2} genannten Teststufen. Der Umfang und die Art der Entwürfe hängt von den aktuell umzusetzenden Anforderungen und der jeweiligen Testart ab. Alle Testfallentwürfe zusammen bilden als Sammlung das Testfallportfolio (die Begrifflichkeit entspringt dem Prozesshaus des Auftragnehmers). Die hier enthaltenen anforderungsbasierten Testfälle werden bereits parallel zur Umsetzung auf Basis der abgestimmten Abnahmekritieren entworfen. Es handelt sich dabei um Testfälle auf einem abstrakten Niveau, um im Wiederholungsfall die Testdaten anpassen und damit die Aussagekraft der Tests verbessern zu können. Testfälle, die absehbar automatisiert werden, werden häufig bereits in einer automatisierungsfreundlichen Beschreibungssprache (z.B. Gherkin-Syntax: Given, When, Then) verfasst.

Die Testfälle werden grundsätzlich release-bezogen in der jeweiligen Projektphase entworfen. Je nach Eignung können sie für Regressionstests weiterverwendet werden. Die Regelungen hierzu werden im Testkonzept festgelegt.

Alle Tests werden in Zusammenarbeit der umsetzenden Fachabteilung (AN) mit ISTQB-zertifizierten Mitarbeitern im cross-funktionalen Entwicklungs-Teams erstellt und liegen im Verantwortungsbereich {des Auftragnehmers}. Auf Wunsch können die anforderungsbasierten Testfälle des Testfallportfolios als Information an {den Auftraggeber} übergeben werden.

### Konzept zur Umsetzung (AN)

Das Konzept zur Umsetzung eines Epics wird {vom Auftragnehmer} zu Beginn jenes Release-Zyklusses erstellt, für den das Epic eingeplant wurde. Die Konzepterstellung (im Wissensmanagementsystem {Confluence}) basiert auf einem Konzepttemplate welches einen Platzhalter für die Diskussion von Testthemen vorsieht. Hier werden Epic-spezifische, testrelevante Themen festgehalten, z.B. welche Testdaten oder Schnittstelleninformationen benötigt werden, welche Testdatengeneratoren umzusetzen sind und welche Mock-Objekte absehbar für den Test benötigt werden bzw. den Test einschränken. Weitere wiederkehrende Testthemen, die im Rahmen des Konzepts grundsätzlich besprochen und festgehalten werden sollen, können im Projektverlauf im Konzepttemplate aufgenommen werden. Das Konzepttemplate wird {dem Auftraggeber} im gemeinsamen Wissensmanagementsystem zugänglich gemacht.

### {Testkonzept (AG)}

### {Testspezifikation (AG)}

### {Testbericht (AG)}

### {Testplan (AG)}

## Testdaten

### Bereitstellung durch {den Auftraggeber}

Wurde im Rahmen der Konzepterstellung für die Umsetzung eines Epics festgestellt, dass Testdaten für die Testausführung notwendig sind, so sollten diese dem AN vor der geplanten Umsetzung der jeweiligen Anforderungen zur Verfügung gestellt werden. Absehbare Testdaten im Projektverlauf sind u. a. :

- Schnittstellenspezifikationen von bestehenden Umsystemen, die im Projektverlauf mindestens übergangsweise bespielt werden müssen
- Schnittstellenspezifikationen von Drittsystemen, die von den neu zu implementierenden Artefakten bespielt werden müssen
- Änderungsmeldungen, sofern sich o.g. Schnittstellen zur Projektlaufzeit ändern
- Beispieldaten von Schnittstellen, die eine datenliefernde Funktion haben. Die Beispieldaten sollten idealerweise im technischen Format der Datenübertragung geliefert werden (z.B. XML, JSON)
- Informationen zu Authentisierungs-/Authentifizierungs-Mechanismen, die bei der Verwendung der o.g. Schnittstellen berücksichtigt werden müssen
- Zugangsdaten für bestehende Anwendungen/-datenbanken und Drittsysteme, auf die von AN-Seite zu Testzwecken zugegriffen werden darf
- Hinweise auf Einschränkungen, die beim Zugriff auf bestehende Um-/Drittsysteme zu beachten sind (z.B. in Bezug auf das Anlegen, Ändern, Löschen von Daten zu Testzwecken)
- Testdaten aus Anwendersicht je
  - Vollzugsbereich
  - Fachverfahren
  - einfachstem Fall einer Datenerfassung
  - komplexesten Fall einer Datenerfassung
- Beispieldaten für Datei-Uploads
- Datenbank-Dumps und/oder Datenbank-Zugriffsmöglichkeiten für den Test von Datenmigrationen
- Datenbank-Auszüge, die als Import mit dem Ziel von Tests auf natürlichen Daten genutzt werden können

### Bereitstellung durch Auftragnehmer

Artefakte, die dem AG zur Prüfung auf dem Abnahmesystem geliefert werden, enthalten einen für den Betrieb der Artefakte erforderlichen Grundstock an Daten. Es kann die gegenseitige Vereinbarung getroffen werden, dass im Rahmen der Lieferung auf das Abnahmesystem vorhandene Datenbankinhalte auf einen definierten Initial-Datenbestand zurückgesetzt werden, um Testaktivitäten zu erleichtern und definierte Datenlagen zu erzeugen.

Da absehbar im Zuge der Testautomatisierung auf AN-Seite Testdatengeneratoren umgesetzt werden, kann eingeplant werden, dass diese auch dazu genutzt werden, den Initial-Datenbestand mit Testdaten ({beispielsweise ein Grundstock an Stammdaten}) für den AG anzureichern. Diese Testdaten wären dann Teil der Lieferung. Mehraufwände für die Abstimmung der Testdaten und für eventuell erforderliche Erweiterungen der Testdatengeneratoren für Zwecke des Auftraggebers sind als zusätzliche Abstimmungs- und Entwicklungsleistungen für die jeweilige Projektphase einzuplanen.

Neben generierten Testdaten können Mechanismen geschaffen werden, natürliche (Alt-)Daten für Testzwecke zu importieren und ggf. zusätzlich zu anonymisieren. Die Entwicklungsaufwände für Import- und Anonymisierungsmechanismen sind als zusätzliche Entwicklungsleistung für die jeweilige Projektphase einzuplanen.

## Abweichungs- und Änderungsmanagement

### Abweichungs- und Fehlermanagement während einer Entwicklungsphase

Das Abweichungs- und Fehlermanagement während der Entwicklungsphasen unterliegt dem Prozesshaus {des Auftragnehmers} und wird im Testkonzept dargestellt. Grundsätzlich gelten hier festgestellte Abweichungen und Fehler als behoben, wenn der AN-interne Test erfolgreich ist.

### Änderungsmanagement während einer Entwicklungsphase

Zu Beginn jeder Entwicklungsphase (oder auch Release-Zyklus) werden die umzusetzenden Anforderungen oder Teile davon definiert. Sollten während der Entwicklungsphase neue Änderungswünsche gemeldet werden, so werden die Neuerungen auf einen möglichen Zusammenhang zur aktuellen Umsetzung geprüft. Gibt es hier keinerlei erkennbaren Zusammenhang, so gehen die neuen Anforderungen ins übliche Anforderungsmanagement über. Sollten sich thematische Zusammenhänge ergeben, so werden alle betroffenen Anforderungen aus der aktuellen Umsetzung markiert. Es erfolgt eine detaillierte Prüfung, ob die Änderungswünsche den bis zum Ende der aktuellen Entwicklungsphase geplanten Stand beeinflussen und damit eine Entscheidung innerhalb des Sprints, ob die Umsetzung für dieses Artefakt angehalten oder fortgesetzt wird.

### Information zur Lieferung

Bei einer agilen Umsetzung kann es vorkommen, dass in der Teillieferung unfertige oder fehlerhafte Artefakte enthalten sind. Hierüber wird der AG so früh wie möglich in Kenntnis gesetzt, um dies bei den eigenen Tests berücksichtigen zu können und um Meldungen bekannter Fehler zu vermeiden.

Die Lieferung eines Teilprojektes kann nur dann als vollständig trotz Fehler deklariert werden, wenn

- die gefundenen Abweichungen/Fehler (durch AN oder AG) festgehalten und bewertet sind,
- nur abgrenzbare Funktionen betroffen sind und
- beide Parteien sich über das Vorhandensein der Abweichungen/Fehler abgestimmt haben.

### Abweichungs- und Fehlermanagement während der Abnahmetests

Grundsätzlich wird der Abnahmetest durch den AG selbst gestaltet. Dazu gehört auch die hausinterne Erfassung von Abweichungen und Fehlern. Die gefundenen Abweichungen und Fehler werden zur weiteren Bewertung und Behebung an {den Auftragnehmer} übergeben. Für eine hohe Transparenz wird der Einsatz eines Ticketsystems empfohlen.

Der Auftraggeber kann gefundene Abweichungen und Fehler kontinuierlich melden. Hierbei sollten folgende Informationen übermittelt werden:

- Fehlernummer zur eindeutigen Identifikation
- Beschreibung des Vorgehens zur Reproduktion des Fehlers
- erwartetes Ergebnis
- tatsächliches Ergebnis
- Verweis auf Anforderung
- idealerweise unterstützendes Material wie Screenshots, Logs oder Rechnerkonfigurationen

Die Tickets werden von Mitarbeitern {des Auftragnehmers} auf Nachvollziehbarkeit geprüft. Dazu zählt die Prüfung der Anforderung genauso wie die Reproduktion der Fehler. Idealerweise gibt es einen regelmäßigen Abstimmungstermin, in dem die bis zu diesem Zeitpunkt neu eingehenden Meldungen besprochen werden, beispielsweise im gemeinsamen Refinement. Für eine bessere Nachvollziehbarkeit werden die Bewertungen auch im Ticketsystem kenntlich gemacht.

Sobald die Bewertung der Meldungen abgeschlossen ist, können als valide Abweichungen und Fehler erkannte Meldungen über das Backlog zur Behebung eingeplant werden. Die Dringlichkeit der Behebung richtet sich in erster Linie nach technischen Gesichtspunkten (z.B. behindernde Auswirkung auf weitere Umsetzung oder Tests), in zweiter nach gesetzlichen Vorgaben und dann folgend nach den Bewertungen des Auftraggebers. Für invalide Fehler hat der AG die Möglichkeit, diese zu prüfen, zu konkretisieren oder als Änderungswunsch anzugeben.

Die innerhalb einer Entwicklung durch {den Auftragnehmer} bearbeiteten und erfolgreich getesteten Nachbesserungen werden in den Lieferdokumenten mit der eindeutigen Fehlernummer als Liefergegenstand gekennzeichnet. Außerdem werden die Fehlertickets im Ticketsystem entsprechend aktualisiert. Der Auftraggeber kann damit die anstehenden notwendigen Tests planen. Der Fehler gilt erst als behoben, wenn die Prüfung des Auftraggebers erfolgreich abgeschlossen wurde.

Langläufertickets oder strittige Meldungen können über einen regelmäßigen Abstimmungstermin, beispielsweise im Rahmen des Refinements, geklärt werden. Darüber hinaus gelten die für das gesamte Projekt definierten Eskalationswege.

### Änderungsmanagement während der Abnahmetests

Aus den während einer Lieferung durchgeführten Tests können sich Änderungswünsche ergeben. Diese können jederzeit an {den Auftragnehmer} gemeldet werden und werden dann als neue Anforderungen bewertet und festgehalten. Dies gilt auch für Änderungswünsche, die sich aus bewerteten Fehlermeldungen ergeben.

### Abweichungs-, Fehler- und Änderungsmanagement nach Inbetriebnahme

Nach Inbetriebnahme des System (Go Live) sind alle Fehler diese Komponenten betreffend über das abgestimmte Service-Ticketsystem zu melden. Für Änderungswünsche kann eine hiervon abweichende Kommunikationsform festgelegt werden.
