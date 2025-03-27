# Tabellenvorlagen für das Tool CSV-RDF-Mapper

## Formate und Downloads

Für die Nutzung mit dem Tool [CSV-RDF-Mapper](tools_SKOS-CSV-RDF-Mapper.md) haben wir mehrere Vorlagen erstellt, deren Zweck und Struktur wir im Folgenden erläutern.

|Vorlage|Zweck|
|-|-|
|[terms.csv](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/CSV-RDF-Mapper_Templates/terms.csv)|Die Tabelle `terms.csv` dient der Sammlung terminologischer Daten für das zu erstellende SKOS-Vokabular.|
|[termrelations.csv](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/CSV-RDF-Mapper_Templates/termrelations.csv)|Die Tabelle `termrelations.csv` ist eine Ergänzung der Tabelle `terms.csv` und dient der Beschreibung von Beziehungen zwischen den dokumentierten Begriffen.|
|[xlLabels_pref.csv](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/CSV-RDF-Mapper_Templates/xlLabels_pref.csv)|Die Tabelle `xlLabels_pref.csv` ist eine Ergänzung der Tabelle `terms.csv` und dient der ausführlichen Beschreibung bevorzugter Benennungen für die Begriffe in `terms.csv`.|
|[xlLabels_alt.csv](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/CSV-RDF-Mapper_Templates/xlLabels_alt.csv)|Die Tabelle `xlLabels_alt.csv` ist eine Ergänzung der Tabelle `terms.csv` und dient der ausführlichen Beschreibung alternativer Benennungen für die Begriffe in `terms.csv`.|
|[sources.csv](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/CSV-RDF-Mapper_Templates/sources.csv)|Die Tabelle `sources.csv` ist eine Ergänzung der Tabelle `terms.csv` und dient der Beschreibung von Quellen, die bei der Recherche herangezogen wurden und als Belege für die Informationen in `terms.csv`, `termrelations.csv`, `xlLabels_pref` und `xlLabels_alt` dienen.|
|[authors.csv](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/CSV-RDF-Mapper_Templates/authors.csv)|Die Tabelle `authors.csv` ist eine Ergänzung der Tabelle `terms.csv` und dient einerseits der Angabe von Personen, die am Vokabular mitgewirkt und die einzelnen Einträge verfasst haben oder für die Autoren der in `sources.csv` genannten Quellen.|

## Struktur von `terms.csv` und Erläuterung der Spalten

### Wichtige Hinweise vorweg

> Bei der Tabelle `terms.csv` ist insbesondere darauf zu achten, dass Informationen zu einem Begriff auf mehrere Zeilen verteilt sein können. Dabei kann ein großer Teil der Zellen leer bleiben.

> Beim Verwenden der Tabelle muss unbedingt darauf geachtet werden, dass immer ein lokaler Identifier für den Begriff angegeben wird, da sonst die spätere Zusammenführung der Daten in einen einzigen RDF-Eintrag nicht möglich ist: Fehlt der lokale Identifier in allen Zeilen eines Begriffs, kann kein Eintrag zu dem Begriff erstellt werden. Fehlt der lokale Identifier in einer oder mehreren Zeilen wird ein unvollständiger Eintrag erstellt, dem dann die Informationen der jeweiligen Zeilen fehlen.

> Beim Verwenden der Tabelle muss unbedingt darauf geachtet werden, dass immer der **korrekte** lokale Identifier für den Begriff angegeben wird, da sonst die spätere Zusammenführung der Daten in einen einzigen RDF-Eintrag fehlerhaft ist: Wird in einer Zeile nicht der lokale Identifier der zum selben Begriff gehörigen Zeilen angegeben, wird die Information der jeweiligen Zeile in einen eigenen Eintrag übernommen. Wird in einer Zeile eine ein lokaler Identifier angegeben, der bereits für einen anderen Begriff gesetzt wurde, werden die Informationen unterschiedlicher Begriffe in einen Eintrag zusammengeführt!

> Die Zeilenüberschriften und Tabellenstruktur darf nicht verändert werden. Die Tabellen müssen exakt so heißen, wie sie heißen und die exakte Struktur behalten.

> Das Dateiformat ist CSV, die verwendeten Trennzeichen sind allerdings keien Kommas, sondern Semikolons.

### Tabelle mit Beispieldaten

Die Struktur von `terms.csv` und die Bedeutung ihrer Spalten wird anhand einiger Beispieldaten erläutert.
Die nachfolgende Tabelle enthält zwei Begriffe:

|lokaler Identifier des Begriffs|bevorzugte Benennung|bevorzugte Benennung - xlLabel|alternative Benennung|alternative Benennung - xlLabel|Definition|Quellenangaben|Bearbeitungsdatum|Fachzuordnung|Erstellungsdatum|redaktionelle Anmerkung|Änderungsvermerk|Verfasser des Eintrags|Kontextsatz|Bearbeitungsstatus|Symbol oder Formelzeichen|Begriffsbeziehung|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|1|Samstag|1|Sonnabend|2|schönster Tag der Woche an dem man alles machen kann|500|12.12.2024|cet|12.12.2023|Samstag ist großartig|2025-03-13 englischsprachige Definition ergänzt|1|Satz als Benutzungsbeispiel|draft|Bsp.|3|
|2|Montag|3|||weniger schöner Tag|500|2024-02-03|cet|2023-01-01|Text für eine Anmerkung|2025-03-13 englischsprachige Definition ergänzt|1|Montag nervt|draft||3|
|3|Parksuchverkehr|6|Parkverkehr|7|Anteil am Straßenverkehr der durch die Suche nach verfügbarem Parkraum entsteht|2|2025-10-03|https://purl.org/linsearch/ver|2025-03-10|TODO: weitere Synonyme suchen||2|Der Parkraumsuchverkehr ist in Ballungsräumen besonders hoch.|||4|
|3|||Parkplatzsuche|4||2||https://purl.org/linsearch/ver||||2||||none|
|3|||Parkraumsuche|5||2||https://purl.org/linsearch/ver||||2||||none|
|4|Straßenverkehr|8||||2||https://purl.org/linsearch/ver||||2||||none|
|5|Schiffsverkehr|9||||2||https://purl.org/linsearch/ver||||2||||none|

<!-- old -->
<!-- |lokaler Identifier des Begriffs|bevorzugte Benennung (de)|alternative Benennung (de)|Definition (de)|Quellenangaben|Bearbeitungsdatum|Fachzuordnung|Erstellungsdatum|redaktionelle Anmerkung|Änderungsvermerk|Verfasser des Eintrags|Kontextsatz|Bearbeitungsstatus|Symbol oder Formelzeichen|Begriffsbeziehung|
|:-:|:-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Begriff-1|Parksuchverkehr|Parkverkehr|Anteil am Straßenverkehr, der durch die Suche nach verfügbarem Parkraum entsteht|https://www.wikidata.org/wiki/Q97379970 (durch Referenznummer ersetzen)|2025-10-03|https://purl.org/linsearch/ver (durch kontrollierten Wert ersetzen)|2025-03-10|TODO: weitere Synonyme suchen|--|https://orcid.org/0000-0002-1584-4316 Jane Doe (durch Verweisnummer ersetzen)|Der Parkraumsuchverkehr ist in Ballungsräumen besonders hoch.|--||Begriff-2|
|Begriff-1||Parkplatzsuche||||||||||||
|Begriff-1||Parkraumsuche||||||||||||
|Begriff-2|Straßenverkehr||||||||||||| -->

In CSV:

```csv
<!-- Todo: Daten ergänzen -->
```

### Erläuterung der Spalten

Die Tabelle `terms.csv` enthält die folgenden Spalten:
<!-- wird in der Übersicht verwendet, sollte in allen Tabellen gleich sein -->
<!-- * **lokaler Identifier des Begriffs**: Der lokale Identifier des Begriffs kann durch eine fortlaufende Nummer angegeben werden. Diese muss innerhalb von terms.csv einzigartig sein und darf nur in solchen Zeilen verwendet werden, die Informationen zum selben Begriff enthalten. Beschreibt eine Zeile einen neuen Begriff, muss auch ein neuer Identifier verwendet werden. Die lokalen Identifier aus terms.csv werden in anderen Tabellen verwendet, um Querverweise herzustellen. Im Rahmen eines Terminologieprojektes macht es deswegen Sinn, sich pro Tabelle zu notieren, welcher Identifier bereits vergeben wurde bzw. die Inhaltszeilen der CSV-Datei nach der Spalte mit dem _lokalen Identifier des Begriffs_ zu sortieren.
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
* **Änderungsvermerk**: 
* **Verfasser des Eintrags**: 
* **Kontextsatz**: 
* **Bearbeitungsstatus**: 
* **Symbol oder Formelzeichen**: 
* **Begriffsbeziehung**:  -->

## Vorlage zur Verwaltung eigener Daten nutzen