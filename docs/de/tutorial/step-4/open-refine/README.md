# Workflow OpenRefine

<!-- tbd todo to do -->
In den folgenden Abschnitten erläutern wir Ihnen das Tool OpenRefine und wie sie es nutzen können, um tabellarische Daten damit in ein [RDF][RDF]-Vokabular umzuwandeln.
Hierzu stellen wir auch tabellarische Vorlagen sowie eine Mappingdatei zur Verfügung, die Sie direkt für ein zweisprachiges Vokabular nutzen können, das den SKOS-Standard befolgt.

## Software-Requirements

Um Ihr Vokabular mit Open Refine aufzusetzen, benötigen Sie folgende Software.

* ein Tabellenkalkulationstool (Open Office, Microsoft Excel), einen Texteditor (z.B. Visual Studio Code, Notepad++) oder Google Sheets
* [OpenRefine](https://openrefine.org/download)
* die OpenRefine-Extension [rdf-transform](https://github.com/AtesComp/rdf-transform)

## Benötigte Dateien

Natürlich benötigen Sie zunächst einmal ein nach unseren [Vorlagen](tutorial-10.md) aufbereitetes Vokabular mit Ihren eigenen Daten.
Zur Transformation nach [RDF][RDF] benötigen Sie darüber hinaus eine Transformationsdatei für OpenRefine von unserem GitHub-Repositorium - bitte laden Sie hier [rdf-transform-for-move.json](https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/main/OpenRefine_Templates/rdf-transform-for-move.json) vorab herunter.

[RDF]: ## "Resource Description Framework"