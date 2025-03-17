# Konversion nach RDF

An diesem Punkt des Tutorials gehen wir davon aus, dass Sie eine der von uns bereitgestellten [Vorlagen](tutorial-10.md) verwendet haben, um erste Daten zu sammeln sowie das Tool [OpenRefine](tools_OpenRefine.md) installiert haben.
Wenn Sie noch keine Daten gesammelt haben, können Sie den Konvertierungsschritt auch mit unseren Beispieldaten ausprobieren, die Sie in einer der folgenden Vorlagen finden:
* [OpenRefineTemplate_wExampleData (Google Sheets)](https://docs.google.com/spreadsheets/d/1EmFfhrcOVAOKf_kfwLzgdKANrdEeT7qKBRdSSPrnlIs/edit?usp=sharing)
* OpenRefineTemplate_wExampleData: [.xslx-Format](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/OpenRefine_Templates/OpenRefineTemplate_wExampleData.xlsx) | [.csv-Format](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/OpenRefine_Templates/OpenRefineTemplate_wExampleData.csv) | [.tsv-Format](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/OpenRefine_Templates/OpenRefineTemplate_wExampleData.tsv)

Im nächsten Schritt nutzen wir OpenRefine, um eine RDF-Version dieser Daten zu erstellen, die dem SKOS-Standard entspricht.

## Schritt 1 -  Starten Sie OpenRefine

Starten Sie OpenRefine so wie für Ihr Betriebssystem angegeben. Nähere Informationen zum Starten und Beenden der Anwendung finden Sie [hier](https://openrefine.org/docs/manual/running). Beim Start sollte sich bereits ein Webbrowser oder ein neuer Tab in einem laufenden Webbrowser öffnen, der die Adresse [http://127.0.0.1:3333](http://127.0.0.1:3333) aufruft.
Hier sollte dann der folgende Startbildschirm zu sehen sein:

![Screenshot des OpenRefine-Startbildschirms](images/openrefine-startscree.png)

## Schritt 2 -  Legen Sie ein neues Projekt an

Gehen Sie zum Menüpunkt `Projekt erstellen`.
Hier können Sie ein Projekt durch Laden einer lokalen Datei starten.
Nach dem Laden der Datei wird zunächst der Dateiname innerhalb der roten Markierung angezeigt.
Um fortzufahren, bestätigen Sie den Vorgang mit dem Button `Nächste`.

![Screenshot von OpenRefine mit der Ansicht zum Anlegen eines neuen Projekts](images/openrefine-create_new_project.png)

Anschließend wird eine Vorschau der Daten angezeigt.
OpenRefine ist in der Lage, das Dateiformat zu erkennen und die Daten entsprechend zu prozessieren.
Dennoch besteht hier noch die Möglichkeit zur Korrektur durch Angabe eines anderen Datenformats.
Darüber hinaus können einige Parameter gesetzt werden, die den Datenimport und letzlich das beeinflussen, was in OpenRefine zur weiteren Bearbeitung angezeigt wird.
Besonders relevant ist bei trennzeichengetrennten Dateien die Wahl des korrekten Trennzeichens.
Auch auf die Zeichenkodierung sollte geachtet werden: Für im deutschen Sprachgebrauch verwendete Sonderzeichen sollten die Daten mit Format UTF-8 geladen werden. Auch unsere Vorlagen bedienen diese Kodierung.
Bei kommaseparierten Tabellen kann es vorkommen, dass die Werte selbst Kommas enthalten, sodass hier die Option `Zeichen verwenden zum Einschließen von Zellen mit Spaltentrennern` verwendet werden sollte, damit solche Zellen nicht versehentlich getrennt werden.
Bei der Eingabe in Tabellenkalkulationstools kann es auch ab und an vorkommen, dass ungewollt Leerzeichen vor oder nach dem Wert eingegeben werden. Mit `Führende & nachgestellte Leerzeichen aus Zeichenfolgen entfernen` können diese beim Import gleich entfernt werden.
Mit den Optionen `Erste X Zeilen am Dateianfang`, `Nächste X Zeilen als Spaltenüberschriften analysieren`, `Anfängliche X Datenzeilen verwerfen` und `Lade maximal X Datenzeilen` lässt sich festlegen, ab wo in der Tabelle Daten erfasst werden sollen. Hat eine Tabelle keine Spaltennamen, können diese auch nachträglich im Feld `Spaltennamen (durch Kommata getrennt)` hinzugefügt werden.
Ob leere Zeilen und Spalten gespeichert werden sollen lässt sich ebenso einstellen wie ob eine Dateiquelle oder eine Archivdatei gespeichert werden soll. Wir verwenden hier die voreingestellten Optionen.
Über die Vorschau der Daten lässt sich gut erkennen, ob die Tabelle korrekt ausgelesen wird.
Bevor man das Projekt endgültig anlegt, kann man optional noch den Projektnamen ändern und einige Tags eingeben. 
Dies ist sinnvoll, sobald man mehrere Projekte verwaltet.
Der folgende Screenshot zeigt den Vorschaubildschirm mit den eben vorgestellten, einstellbaren Optionen.

![Screenshot des Vorschaubildschirms von OpenRefine sowie der Parsing-Optionen für den Import einer Quelle](images/openrefine-preview_dataload.png)

Nachdem das Projekt erstellt wurde, wird es geöffnet.
Man sieht dann in der Startansicht diverse Elemente.

1 Die Daten werden auch in OpenRefine tabellarisch angezeigt. Standardmäßig werden 10 Zeilen angezeigt.<br>
2 Man hat die Option die Ansicht zwischen Zeilen und Datensätzen umzuschalten. Bei der Form unserer Tabelle ist diese Option nicht bedeutsam.<br>
3 Man kann einstellen, wie viele Zeilen angezeigt werden sollen und ...<br>
4 ... einfach in den Daten navigieren.<br>
5 Die Daten lassen sich darüber hinaus auch mit diversen Facetten und Filtern in beliebige Teilmengen aufteilen. Standardmäßig wird der Reiter `Facette/ Filter` zuerst geöffnet, mit `Rückgängig/ Wiederholen` kann umgeschaltet werden zum Bearbetungsverlauf - alle Zellen lassen sich einzeln oder in Massenbearbeitungen überarbeiten.<br>
6 Die später benötigte Erweiterung RDF Transform sollte bereits über einen Button aufrufbar sein.

![Screenshot von OpenRefine mit geladenen Daten und Annotationen, die die Elemente des graphischen User Interfaces erläutern](images/openrefine-data_loaded.png)

## Schritt 3 - Wechseln Sie zur Bearbeitungshistorie

Wechseln Sie zur Ansicht der Bearbeitungshistorie mit dem Button `Rückgängig / Wiederholen`.
Hier müssen jetzt zwei Buttons - `Extrahieren...` und `Anwenden...` verfügbar sein.

![](images/openrefine_history.png)

Klicken Sie auf den Button `Anwenden...`.
Es öffnet sich ein Eingabefenster, in das Sie einen OpenRefine-Vorgangsverlauf einfügen können.
Diesen Vorgangsverlauf haben wir bereits auf unserem GitHub-Repositorium in der Datei [rdf-transform-for-move.json](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/OpenRefine_Templates/rdf-transform-for-move.json) vordefiniert.
Den Inhalt dieser Datei können Sie jetzt einfach in das Fenster hineinkopieren.
Im Anschluss wenden Sie ihn durch Klcik auf den Button `Operationen durchführen` an.

![Schreenshot von OpenRefine, der das geöffnete Fenster für die Eingabe eines Vorgangsverlaufes zeigt](images/openrefine-vorgangsverlauf-anwenden.png)

Im Anschluss sehen Sie im Verlauf des Projekts dann zwei Bearbeitungsschritte:

0. Create project
1. Save RDF Transform

Der Arbeitsschritt `Save RDF Transform` beinhaltet die Definition eines Mappings der tabellarischen Daten auf ein RDF-basiertes Schema.
Dieses kann nur angewendet werden, wenn die Tabellenvorlagen bei der Bearbeitung nicht in ihrer Struktur geändert wurde.

![Screenshot von OpenRefine, das die zwei Bearbeitungsschritte aus dem geladenen Vorgangsverlauf zeigt](images/openrefine_history_is_applied.png)

- [ ] TODO: Noch ergänzen: Wie updated man das RDF-Transform-Schema um den eigenen Identifier?

## Schritt 4 -  Export der RDF-Daten

Um nun einen RDF-Export Ihrer Daten zu erhalten müssen Sie jetzt nicht mehr viel machen.
Lediglich ein Klick auf den Button `Export` und die Auswahl der richtigen Export-Option ist notwendig.
Wir wählen hier unter `RDF Transform` den `Pretty Export` und dort - wegen besserer Lesbarkeit des Codes - `Turtle (Pretty)`.

![Screenshot von OpenRefine, der das Menü zum Exportieren von RDF-Dateien zeigt](images/openrefine-rdf_export.png)

OpenRefine erstellt dabei eine Datei mit dem Namen [OpenRefine_Templates/OpenRefineTemplate_wExampleData_tsv.ttl](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/OpenRefine_Templates/OpenRefineTemplate_wExampleData_tsv.ttl) (sofern das Projekt beim Datenimport nicht anders benannt wurde!).
Die erzeugte Datei wird dabei wie ein Download behandelt.
Sie kann mit einem Texteditor wie Notepad++ oder Visual Studio Code oder einer Spezialsoftware für Ontologien (z.B. [Protégé](https://protege.stanford.edu/)) oder [SKOS-Vokabulare](https://gbv.github.io/bartoc-vocabulary-software/) geöffnet werden.
Diesen Export sollten Sie im selben Repositorium ablegen, in dem Sie auch die tabellarischen Daten abgelegt haben.
Der aus unserer Vorlage mit Beispieldaten generierte Output in dieser Exportdatei sieht folgendermaßen aus:

<!-- Updaten wenn ich ex: ersetzt habe -->

```Turtle
@prefix :        <http://purl.org/mydomain/mysubdomain/> .
@prefix dcat:    <http://www.w3.org/ns/dcat#> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix ex:      <https://www.example.com/> .
@prefix foaf:    <http://xmlns.com/foaf/0.1/> .
@prefix m4i:     <http://w3id.org/nfdi4ing/metadata4ing#> .
@prefix owl:     <http://www.w3.org/2002/07/owl#> .
@prefix rdf:     <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:    <http://www.w3.org/2000/01/rdf-schema#> .
@prefix skos:    <http://www.w3.org/2004/02/skos/core#> .
@prefix skosxl:  <http://www.w3.org/2008/05/skos-xl#> .
@prefix vcard:   <http://www.w3.org/2006/vcard/ns#> .
@prefix xsd:     <http://www.w3.org/2001/XMLSchema#> .

:Concept2  rdf:type         skos:Concept;
        dcterms:created     "03.06.2025"^^xsd:date;
        dcterms:creator     :Author1;
        dcterms:modified    "08.11.2025"^^xsd:date;
        dcterms:subject     <http://uri.gbv.de/terminology/bk/55.84>;
        skos:editorialNote  "add definitions"@en , "get approval for concept by project lead"@en , "add context sentence"@en , "Begriff von Projektleitung absegnen lassen"@de , "Definitionen ergänzen"@de , "Kontextsatz ergänzen"@de;
        skos:prefLabel      "street traffic"@en , "Straßenverkehr"@de;
        ex:editorialStatus  "draft";
        ex:id               "Concept2" .

:Source2  rdf:type         ex:Source;
        dcterms:publisher  "Wikidata";
        dcterms:title      "parking search traffic";
        dcat:accessURL     "https://www.wikidata.org/w/index.php?title=Q97379970&oldid=1936875884"^^xsd:anyURI;
        ex:id              "Source2" .

<https://purl.org/linsearch/ver>
        rdf:type  skos:Concept .

:Author2  rdf:type      foaf:Person;
        m4i:orcidId     "https://orcid.org/0000-0002-0871-8994";
        foaf:firstName  "Jane";
        foaf:lastName   "Doe";
        ex:id           "Author2" .

:Concept1  rdf:type         skos:Concept;
        dcterms:created     "03.06.2025"^^xsd:date;
        dcterms:creator     :Author1;
        dcterms:modified    "08.11.2025"^^xsd:date;
        dcterms:source      :Source1 , :Source2;
        dcterms:subject     <http://uri.gbv.de/terminology/bk/55.84>;
        skos:altLabel       "Parkplatzsuche"@de , "Parksuchverkehr"@de , "Parkverkehr"@de;
        skos:broader        :Concept2;
        skos:changeNote     "Die Definition wurde geändert, weil ..."@de , "The definition has been changed due to the fact that ..."@en;
        skos:definition     "Anteil des Straßenverkehrs, der bei der Suche nach einem Parkplatz anfällt"@de , "portion of street traffic resulting from the search for parking space"@en;
        skos:editorialNote  "Please search further synoynms in English"@en , "Bitte weitere Synonyme aus dem Englischen suchen!"@de;
        skos:prefLabel      "parking traffic"@en , "Parkraumsuchverkehr"@de;
        ex:contextSentence  "Parking traffic is highest in densely populated metropolitan areas."@en;
        ex:editorialStatus  "draft";
        ex:exampleSentence  "Der Parkraumsuchverkehr ist in Ballungsgebieten am höchsten."@de;
        ex:id               "Concept1" .

:Author4  rdf:type      foaf:Person;
        m4i:orcidId     "https://orcid.org/0000-0002-0871-8993";
        foaf:firstName  "Harro";
        foaf:lastName   "Maier";
        ex:id           "Author4" .

:Source1  rdf:type         ex:Source;
        dcterms:creator    :Author4 , :Author1;
        dcterms:issued     "2026"^^xsd:gYear;
        dcterms:publisher  "Fiktiver Verlag";
        dcterms:title      "Wörterbuch der Verkehrswissenschaften";
        dcat:accessURL     "https://example.com/verlagsseite/buchseite"^^xsd:anyURI;
        ex:id              "Source1" .

:Author1  rdf:type      foaf:Person;
        m4i:orcidId     "https://orcid.org/0000-0002-0871-8994";
        foaf:firstName  "Jane";
        foaf:lastName   "Doe";
        ex:id           "Author1" .

:Concept5  rdf:type      skos:Concept;
        dcterms:creator  :Author2;
        dcterms:source   :Source2;
        dcterms:subject  <https://purl.org/linsearch/ver>;
        skos:prefLabel   "Schiffsverkehr"@de;
        ex:id            "Concept5" .

<http://uri.gbv.de/terminology/bk/55.84>
        rdf:type  skos:Concept .

```
