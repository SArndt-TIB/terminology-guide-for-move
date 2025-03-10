# Tabellarische Datensammlung

Um möglichst vielen Personen die Mitgestaltung eines Vokabulars ohne größere Einsteigshürden zu erlauben, empfehlen wir, die Datensammlung mit Tabellenkalkulationstools durchzuführen.
Hier bieten sich zum Beispiel Tools wie Microsoft Excel, Open Office Calc, Google Sheets oder NextCloud Tables an, die eine lokale oder cloud-basierte Bearbeitung ermöglichen.
Bei der Verwendung solche Tabellensoftwares sollte die Tabellenstruktur unbedingt eingehalten werden, um spätere Konvertierungsprozesse bestmöglichst zu unterstützen, Fehler zu vermeiden und ein valides Endergebnis zu erstellen.
Teilweise bieten die genannten Tools auch sehr elaborierte Valididerungsmöglichkeiten an, die bereits bei der Eingabe in eine Tabelle eine rigorose Prüfung und entsprechende Warnungen erlauben.

Für die Nutzung mit dem Tool [CSV-RDF-Mapper](tools_SKOS-CSV2RDF.md) haben wir mehrere Vorlagen erstellt, deren Zweck und Struktur wir im Folgenden erläutern.

|Vorlage|Zweck|
|-|-|
|[terms.csv](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/csv-templates/terms.csv)|Die Tabelle `terms.csv` dient der Sammlung terminologischer Daten für das zu erstellende SKOS-Vokabular.|
|[termrelations.csv](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/csv-templates/termrelations.csv)|Die Tabelle `termrelations.csv` dient der Beschreibung von Beziehungen zwischen den dokumentierten Begriffen.|
|[sources.csv](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/csv-templates/sources.csv)|Die Tabelle `sources.csv` dient der Beschreibung von Quellen, die bei der Recherche herangezogen wurden und als Belege für die Informationen in `terms.csv` und `termrelations.csv` dienen.|
|[authors.csv](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/csv-templates/authors.csv)|Die Tabelle `authors.csv` dient der Angabe von Personen, die am Vokabular mitwirken und die die einzelnen Einträge verfasst haben.|

## Struktur von `terms.csv`

### Wichtige Hinweise vorweg

> Bei der Tabelle `terms.csv` ist insbesondere darauf zu achten, dass Informationen zu einem Begriff auf mehrere Zeilen verteilt sein können. Dabei kann ein großer Teil der Zellen leer bleiben.

> Beim Verwenden der Tabelle muss unbedingt darauf geachtet werden, dass immer ein lokaler Identifier für den Begriff angegeben wird, da sonst die spätere Zusammenführung der Daten in einen einzigen RDF-Eintrag nicht möglich ist: Fehlt der lokale Identifier in allen Zeilen eines Begriffs, kann kein Eintrag zu dem Begriff erstellt werden. Fehlt der lokale Identifier in einer oder mehreren Zeilen wird ein unvollständiger Eintrag erstellt, dem dann die Informationen der jeweiligen Zeilen fehlen.

> Beim Verwenden der Tabelle muss unbedingt darauf geachtet werden, dass immer der **korrekte** lokale Identifier für den Begriff angegeben wird, da sonst die spätere Zusammenführung der Daten in einen einzigen RDF-Eintrag fehlerhaft ist: Wird in einer Zeile nicht der lokale Identifier der zum selben Begriff gehörigen Zeilen angegeben, wird die Information der jeweiligen Zeile in einen eigenen Eintrag übernommen. Wird in einer Zeile eine ein lokaler Identifier angegeben, der bereits für einen anderen Begriff gesetzt wurde, werden die Informationen unterschiedlicher Begriffe in einen Eintrag zusammengeführt!

> Die Zeilenüberschriften und Tabellenstruktur darf nicht verändert werden. Die Tabellen müssen exakt so heißen, wie sie heißen und die exakte Struktur behalten.

### Beispieldaten

Die Struktur von `terms.csv` und die Bedeutung ihrer Spalten wird anhand einiger Beispieldaten erläutert.
Die nachfolgende Tabelle enthält zwei Begriffe:

|lokaler Identifier des Begriffs|bevorzugte Benennung (de)|alternative Benennung (de)|Definition (de)|Quellenangaben|Bearbeitungsdatum|Fachzuordnung|Erstellungsdatum|redaktionelle Anmerkung|Anmerkung zur Bearbeitungshistorie|Verfasser des Eintrags|Kontextsatz|Bearbeitungsstatus|Mathematisches Symbol|Begriffsbeziehung|
|:-:|:-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Begriff-1|Parksuchverkehr|Parkverkehr|Anteil am Straßenverkehr, der durch die Suche nach verfügbarem Parkraum entsteht|https://www.wikidata.org/wiki/Q97379970 (durch Referenznummer ersetzen)|2025-10-03|https://purl.org/linsearch/ver (durch kontrollierten Wert ersetzen)|2025-03-10|TODO: weitere Synonyme suchen|--|https://orcid.org/0000-0002-1584-4316 Jane Doe (durch Verweisnummer ersetzen)|Der Parkraumsuchverkehr ist in Ballungsräumen besonders hoch.|--||Begriff-2|
|Begriff-1||Parkplatzsuche||||||||||||
|Begriff-1||Parkraumsuche||||||||||||
|Begriff-2|Straßenverkehr|||||||||||||

In CSV:

```csv
<!-- Todo: Daten ergänzen -->
```

### Erläuterung der Spalten

Die Tabelle `terms.csv` enthält die folgenden Spalten:

* **Lokaler Identifier des Begriffs**: Der lokale Identifier des Begriffs kann durch eine fortlaufende Nummer angegeben werden. Diese muss innerhalb von terms.csv einzigartig sein und darf nur in solchen Zeilen verwendet werden, die Informationen zum selben Begriff enthalten. Beschreibt eine Zeile einen neuen Begriff, muss auch ein neuer Identifier verwendet werden. Die lokalen Identifier aus terms.csv werden in anderen Tabellen verwendet, um Querverweise herzustellen. Im Rahmen eines Terminologieprojektes macht es deswegen Sinn, sich pro Tabelle zu notieren, welcher Identifier bereits vergeben wurde bzw. die Inhaltszeilen der CSV-Datei nach der Spalte mit dem _lokalen Identifier des Begriffs_ zu sortieren.
* bevorzugte Benennung (de)
* alternative Benennung (de)
* Definition (de)
* Quellenangaben
* Bearbeitungsdatum
* Fachzuordnung
* Erstellungsdatum
* redaktionelle Anmerkung
* Anmerkung zur Bearbeitungshistorie
* Verfasser des Eintrags
* Kontextsatz
* Bearbeitungsstatus
* Mathematisches Symbol
* Begriffsbeziehung
