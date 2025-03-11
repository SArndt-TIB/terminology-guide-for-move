# Datensammlung, Dokumentation, Konversion

## Was sollte man sammeln?

Im Abschnitt [Elemente einer Terminologie](terminology-5.md) haben wir bereits einige Bestandteile von Terminologien anhand von Beispielen erläutert.
Um eine Terminologie maschinenlesbar zu dokumentieren, müssen jedoch ein paar weitere Details erfasst werden.

<!-- todo: was sammeln? -->

* **lokaler Identifier des Begriffs**: Der lokale Identifier des Begriffs kann durch eine fortlaufende Nummer angegeben werden. Diese muss innerhalb von terms.csv einzigartig sein und darf nur in solchen Zeilen verwendet werden, die Informationen zum selben Begriff enthalten. Beschreibt eine Zeile einen neuen Begriff, muss auch ein neuer Identifier verwendet werden. Die lokalen Identifier aus terms.csv werden in anderen Tabellen verwendet, um Querverweise herzustellen. Im Rahmen eines Terminologieprojektes macht es deswegen Sinn, sich pro Tabelle zu notieren, welcher Identifier bereits vergeben wurde bzw. die Inhaltszeilen der CSV-Datei nach der Spalte mit dem _lokalen Identifier des Begriffs_ zu sortieren.
* **bevorzugte Benennung**: 
* **bevorzugte Benennung - xlLabel**: 
* **alternative Benennung**: 
* **alternative Benennung - xlLabel**: 
* **Definition**: 
* **Quellenangaben**: 
* **Bearbeitungsdatum**: 
* **Fachzuordnung**: 
* **Erstellungsdatum**: 
* **redaktionelle Anmerkung**: 
* **Anmerkung zur Bearbeitungshistorie**: 
* **Verfasser des Eintrags**: 
* **Kontextsatz**: 
* **Bearbeitungsstatus**: 
* **Mathematisches Symbol**: 
* **Begriffsbeziehung**: 

## Tabellarische Dokumentation

Um möglichst vielen Personen die Mitgestaltung eines Vokabulars ohne größere Einsteigshürden zu erlauben, empfehlen wir, die Datensammlung mit Tabellenkalkulationstools durchzuführen.
Hier bieten sich zum Beispiel Tools wie Microsoft Excel, Open Office Calc, Google Sheets oder NextCloud Tables an, die eine lokale oder cloud-basierte Bearbeitung ermöglichen.
Bei der Verwendung solcher Tabellensoftwares sollte die Tabellenstruktur unbedingt eingehalten werden, um spätere Konvertierungsprozesse bestmöglichst zu unterstützen, Fehler zu vermeiden und ein valides Endergebnis zu erstellen.
Teilweise bieten die genannten Tools auch sehr elaborierte Valididerungsmöglichkeiten an, die bereits bei der Eingabe in eine Tabelle eine rigorose Prüfung und entsprechende Warnungen erlauben.
Tabellen lassen sich zudem auch sehr gut im CSV-Format mit Text-Editoren wie VisualStudio Code, Notepad++ oder ... verwalten.