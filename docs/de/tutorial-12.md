# Datensammlung, Dokumentation, Konversion

## Was sollte man sammeln?

Im Abschnitt [Elemente einer Terminologie](terminology-5.md) haben wir bereits einige Bestandteile von Terminologien anhand von Beispielen erläutert.
Um eine Terminologie maschinenlesbar zu dokumentieren, müssen jedoch ein paar weitere Details erfasst werden.

<!-- todo: was sammeln? -->
Neben den Fachausdrücken sollte man auch festhalten, aus welcher _Sprache_ der Fachausdruck stammt.
Dies ist nicht nur bei mehrsprachiger Terminologiearbeit zu empfehlen, sondern auch bei einsprachiger Terminologiearbeit sollte auf diese explizite Form der Dokumentation von Anfang an geachtet werden.
Einen Spezialfall bilden hier mathematische Symbole oder Formelzeichen, die in der Regel sprachübergreifend genutzt werden.
In diesem Fall ist eine Kennzeichnung nicht unbedingt erforderlich.
Zusätzlich kann man die gesammlten Fachausdrücke auch bewerten.
Hierzu hat sich in der Terminologiedokumentation eine Unterscheidung zwischen _bevorzugter Benennung_/ _Vorzugsbenennung_ und _alternativer Benennung_ oder strenger _abgelehnter Benennung_ etabliert.
Um die Verwendung der Fachausdrücke zu demonstrieren, können auch Beispielsätze formuliert und einem Bergriffseintrag hinzugefügt werden.
Dies ist insbesondere für Übersetzungskontexte sinnvoll, aber auch für solche Nutzer, für die die Fachsprache auch noch Teil einer Fremdsprache ist (z.B. internationale Studierende, Gastwissenschaftler).

Auch Definitionen eines Begriffs sollten explizit einer Sprache zugeordnet werden, in der sie verfasst sind.

Wird die Terminologie eines interdisziplinären Wissensgebietes oder die Terminologie unterschiedlicher Teildisziplinen mit ähnlichem Gegenstandsbereich erhoben, bietet es sich auch an, die Einträge einem fachlichen Klassifikationssystem zuzuordnen, um Einträge mit ähnlichen oder identischen Benennungen schneller differenzieren zu können.
Hierzu kann ein Verweis auf kontrollierte Vokabulare erfolgen.

Bei der expliziten Modellierung von Begriffsbeziehungen sollte nach Möglichkeit der Beziehungstyp, der zwischen den beiden Begriffen herrscht, explizit und konkret benannt werden.
Hierbei spielen insbesondere Abstraktionsbeziehungen eine wichtige Rolle im wissenschaftlichen Begriffssystem.

Neben den eigentlichen terminologischen Daten und ihren Charakterisierungen ist die Aufnahme von Metadaten pro Begriffseintrag ebenfalls zu empfehlen.
Durch solche Metadaten können Arbeitsabläufe transparent gemacht, Beweggründe für eine bestimmte Modellierung gegeben oder auch legitimiert werden, sowie Ansprechpersonen angegeben werden.
Relevante Metadaten sind in diesem Zusammenhang zum Beispiel 

* der Verfasser des Eintrags
* das Datum der Erstellung des Eintrags,
* das Datum der letzten Bearbeitung,
* der aktuelle Bearbeitungsstatus,
* redaktionelle Anmerkungen,
* Anmerkungen zur Bearbeitungshistorie,
* Quellenangaben,
* eindeutige Referenznummern für die Begriffseinträge.

## Tabellarische Dokumentation

Um möglichst vielen Personen die Mitgestaltung eines Vokabulars ohne größere Einsteigshürden zu erlauben, empfehlen wir, die Datensammlung in tabellarischer Form durchzuführen und dafür zum Beispiel Tabellenkalkulationstools oder Texteditoren zu nutzen.
Hier bieten sich zum Beispiel Tools wie Microsoft Excel, Open Office Calc, Google Sheets oder NextCloud Tables an, die eine lokale oder cloud-basierte Bearbeitung ermöglichen.
Tabellen lassen sich zudem auch sehr gut mit Text-Editoren wie VisualStudio Code oder Notepad++ verwalten, wenn sie in nicht-binären Formaten wie [CSV][CSV] oder [TSV][TSV] verwaltet werden.
Teilweise bieten die genannten Tools auch sehr elaborierte Valididerungsmöglichkeiten an, die bereits bei der Eingabe in eine Tabelle eine rigorose Prüfung und entsprechende Warnungen erlauben.
Bei der Verwendung solcher Tabellensoftwares sollte die Tabellenstruktur unbedingt eingehalten werden, um spätere Konvertierungsprozesse bestmöglichst zu unterstützen, Fehler zu vermeiden und ein valides Endergebnis zu erstellen.

[CSV]: ## "Comma-seperated values/ kommaseparierte Werte"
[TSV]: ## "Tab-seperated values/ tabulatorseparierte Werte"