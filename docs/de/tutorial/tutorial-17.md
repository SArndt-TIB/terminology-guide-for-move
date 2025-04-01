# End of Life

## ... der terminologischen Ressource

Eine Terminologie sollte idealerweise ein lebendes Dokument sein, das sich kontinuierlich weiterentwickelt und neuen Gegegebenheiten des Faches und seines sich entwickelnden Gegenstandsbereiches und Wissensstandes anpassen sollte,
Sollte es doch einmal nicht mehr möglich sein, das Vokabular weiterzuentwickeln und sich auch niemand finden lässt, die Fackel weiter zu tragen, sollte man die terminologische Ressource nicht einfach kommentarlos sich selbst überlassen und verwaisen.
<!-- abandon in the word i am searching for... -->

Wir hatten bereits im Schritt [Metadaten ergänzen](tutorial-6.md) empfohlen, den Status des Vokabulars in seinen Metadaten anzugeben.
Hierzu wird der als skos:ConceptScheme und owl:Ontology deklarierte Identifier einfach annotiert.
Ein Beispiel für das Testvokabular zeigt der folgende Code.

``` turtle

<testvocab> rdf:type owl:Ontology , skos:ConceptScheme ;
    bibo:status "draft"@en .

```

Um das Lebensende der Terminologie anzuzeigen, kann der erste Schritt sein, diese Statusangabe zu aktualisieren.
Wir empfehlen hier die Verwendung des Wertes "abandoned".
Gleichzeitig können die Metadaten um weitere Informationen ergänzt werden, zum Beispiel wäre es möglich, einen ausfürlich Kommentar zu schreiben, der über die Property [rdfs:comment](URL ergänzen) angegeben wird.
Mit einem solchen Kommentar können zum Beispiel die Gründe angegeben werden, warum eine terminologische Ressource nicht weiter unterstützt und weiterentwickelt wird.

Darüber hinaus könnte man die Metadaten auch um das folgende Statement erweitern: 

``` turtle

<testvocab> rdf:type owl:Ontology , skos:ConceptScheme ;
    owl:deprecated true .

```

Auch in der öffentlichen Arbeitsumgebung kann ein entsprechender Hinweis gegeben werden, dass Support und Aktualisierung eingestellt werden, indem man das Repositorium archiviert.
<!-- tbd todo to do: noch mal klären, was wirklich passiert, wenn man auf GitHub und GitLab das Projekt archiviert -->
Es können dann keine weiteren Berarbeitungen daran vorgenommen werden.
Sofern die Lizenz es erlaubt, könnte man aber auch eine Weiterführung der Arbeiten durch andere qualifizierte Arbeitsgruppen erlauben.
Hierzu sollte vom ursprünglichen Projekt ein [Fork](URL ergänzen) erstellt werden.

## ... einzelner Konzepte

Mitunter kommt es vor, dass ein Konzept als veraltet deklariert werden muss.
Hierdurch soll dann erreicht werden, dass der Identifier eines solchen Konzeptes nicht mehr verwendet werden soll.
Dabei ist es wichtig zu beachten, dass dieses Konzept nicht einfach nur entfernt werden darf.
Im Gegenteil: es muss weiterhin Teil der terminologischen Ressource bleiben und muss sogar noch weiter kommentiert werden.
Wenn ein Konzept in einem externen Datenbestand verwendet wird, ist es notwendig, dass dieser Datenbestand irgendwann von der Veraltung des Konzepts erfährt und auf potentielle Nachfolger umsteigt.
Ein deprecatetes (todo deutschsprachigen Ausdruck finden!) Konzept könnte dabei folgendermaßen annotiert sein:

``` turtle

:Concept5 rdf:type skos:Concept ;
    owl:deprecated true ;
    # reason
    # follow-up term
    # more?
    # check with obo

```
