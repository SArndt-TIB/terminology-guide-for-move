# Identifier erstellen

## Was ist ein Identifier?

Ein Identifier im Kontext der Terminologiearbeit für das Semantic Web ist eine eindeutige Web-Adresse ([Uniform Resource Identifier (URI)](https://de.wikipedia.org/wiki/Uniform_Resource_Identifier) oder [Internationalized Resource Identifier (IRI)](https://de.wikipedia.org/wiki/Internationalized_Resource_Identifier)), mit der eine terminologische Ressource oder auch ihre einzelnen Elemente oder auch Versionen davon **dauerhaft** erreichbar sind.
Für die dauerhafte Erreichbarkeit einer Ressource braucht es zuverlässige und langfristig agierende Dienstleister, die die Ressource in allen Varianten langfristig und ohne Unterbrechung zur Verfügung stellen können.
Mit der [Einrichtung eines GitHub- oder GitLab-basierten Repositoriums](tutorial-2.md) haben wir bereits eine gute Grundlage gelegt, um die zu unserem Vokabular gehörigen Dateien zu verwalten, dauerhaft verfügbar zu halten und auch offizielle Releases herauszugeben.
Leider sind die Links dieser Ressourcen nicht sonderlich chic und memorabel - der wirklich maschinenlesbare Output der Konversion unserer Tabelle nach RDF mit OpenRefine ist zum Beispiel unter <https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/develop/OpenRefine_Templates/OpenRefineTemplate_wExampleData_tsv.ttl> erreichbar.
Solche Links als Identifier für das Vokabular zu verwenden ist theoretisch zwar möglich, aber sähe ein wenig gewähnungsbedürftig aus, ganz zu Schweigen von den Identifiern der einzelnen Entitäten wie den Begriffen:

``` turtle
@prefix owl:     <http://www.w3.org/2002/07/owl#> .
@prefix rdf:     <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:    <http://www.w3.org/2000/01/rdf-schema#> .
@prefix skos:    <http://www.w3.org/2004/02/skos/core#> .
@prefix skosxl:  <http://www.w3.org/2008/05/skos-xl#> .
@prefix xsd:     <http://www.w3.org/2001/XMLSchema#> .

<https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/develop/OpenRefine_Templates/OpenRefineTemplate_wExampleData_tsv.ttl>   
  rdf:type owl:Ontology ;
  rdf:type skos:ConceptScheme .

<https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/develop/OpenRefine_Templates/OpenRefineTemplate_wExampleData_tsv.ttl#Concept1>
  rdf:type skos:Concept ;
  skos:prefLabel "Parkraumsuchverkehr"@en .
```

Ein weitere Problem besteht darin, dass eine terminologische Ressource auch einmal umziehen kann.
Der ursprüngliche Identifier wäre dann nicht mehr der gültige Link zur Ressource und müsste aktualisiert werden - und zwar überall, wo er zu Referenzzwecken verwendet wird!
Um dies zu vermeiden, verwendet man normalerweise gleichbleibende Identifier sowohl für die terminologische Ressource als Ganzes, als auch für die einzelnen enthaltenen Elemente - unabhängig von der Location an der sie tatsächlich bereitgestellt werden.
So hat man zur Zitation einer Terminologie und ihrer Begriffe gleichbleibende Identifier, auch wenn die Ressource ggf. die Domain wechselt.
Die Verbindung zwischen dem Identifier und dem tatsächlichen Ablage-Ort der Ressource muss dabei sorgfältig gepflegt und gewissenhaft aktualisiert werden - dies dann allerdings nur noch für die Terminologie und ihre Elemente und nicht mehr überall dort, wo sie genutzt wird.
Insgesamt entsteht hierdurch also eine enorme Arbeitserleichterung für alle, die eine Terminologie im Web und in Dokumenten referenzieren wollen.
Um die Verbindung zwischen einer als Identifier wirkenden URI oder IRI sowie der realen Lokalität einer Ressource herzustellen, bedarf es normalerweiser eigener Server, der richtigen Konfiguration zur Weiterleitung der Identifier-URIs auf die Ziel-URIs sowie eigener Domains.
Um "nur" eine Terminologie zu veröffentlichen, ist dies ein erheblicher Aufwand für einzelne Nutzer.
Glücklicherweise gibt es eine Reihe von Services, die das Betreiben der Infrastruktur übernehmen und auch Domains registrieren, sodass die einzelnen Nutzenden nur noch konfigurieren müssen, welche Identifier sie benötigen, wohin diese weitergeleitet werden sollen und dass sie aktualisiert werden, sobald dies notwendig wird.
Hierbei können auch Identifier erstellt werden, die klar auf eine bestimmte Versionen einer Terminologie Bezug nehmen können.

## Services zur Einrichtung von Identifiern

### PURL.org

Ein kostenfrei nutzbarer Dienst zur Registrierung und Konfiguration von Identifiern ist der [PURL-Service](https://purl.archive.org/) des [Internet Archive](https://archive.org/about/), einer amerikanischen non-profit Organisation. 
Registrierte Nutzer können hier relativ einfach Domains im Namensraum <https://purl.org> registrieren und weitere Subdomains für unterschiedliche Ressourcen erstellen.
Die PURLs werden dabei nach dem folgenden Muster gebildet:

![Bildliche Darstellung der Zusammensetzung einer PURL von der Seite https://purl.lib.fsu.edu/docs/images/purlparts.png](https://purl.lib.fsu.edu/docs/images/purlparts.png)
<!-- Switch to this version if image ever goes offline -->
<!-- ![Lokale Kopie einer bildlichen Darstellung der Zusammensetzung einer PURL, ursprünglich von der Seite https://purl.lib.fsu.edu/docs/images/purlparts.png (Abrufdatum: 18.03.2025)](images/purlparts.png) -->

_Scheme_ und _host_ sind für alle PURLs des Service identisch, es besteht aber auch die Möglichkeit statt `.org/` die Endungen `.net/`, `.info/`, oder `.com/` zu verwenden.
Auch diese alternativen Endungen des hosts lösen korrekt auf die festlegten Ziele auf.
Der Nutzer kann _domain_ und _PURL name_ bestimmen wodurch individuelle PURLs erzeugt werden, deren Zieladressen der Nutzer selbst festlegen kann, die er aber auch selbst aktualisieren muss, sollten sie sich ändern.

Die Registrierung der Domains erfolgt dabei über ein Webformular, sodass dieser Service insbesondere für Einsteiger sehr gut geeignet ist.

![](images/PURLorg%20-%20administration.png)

Da eine Domain nur einmal vergeben werden kann, macht es Sinn, zunächst mit einer Suche zu prüfen, ob die gewünschte Domain nicht schon vergeben ist.
Der nachfolgende Screeshot zeigt die Ergebnisse zur Suche nach `library`.

![](images/PURLorg%20-%20domain%20search.png)

Ist die gewünschte Domain noch frei, kann sie angelegt und im Anschluss konfiguriert werden.
Im Screenshot sieht man die für dieses Tutorial registrierte Domain <http://purl.org/terminology-guide-for-move> für seine mit Stand 2025-03-18 gültige Adresse <https://sarndt-tib.github.io/terminology-guide-for-move/#/>.
Als HTTP Statuscode wurde hier `302 Found` gewählt, um anzuzeigen, dass eine Ressource existiert sowie bei Anfragen ihren Ort anzuzeigen oder dorthin weiterzuleiten.
Bei der Verwendung der PURL in einem Webbrowser erfolgt dies so schnell, dass der Nutzer es eigentlich kaum merkt.

![](images/PURLorg-new-domain-saved.png)

Nach dem Anlegen einer Domain können dann weitere Subdomains angelegt werden.
Beim Beispiel dieses Tutoriums könnten Subdomains zum Beispiel für die Unterseiten benötigt werden.
Den Abschnitt [Was ist Terminologie?](terminology-1.md) kann man zum Beispiel über die GitHub-Adresse <https://sarndt-tib.github.io/terminology-guide-for-move/#/de/terminology-1> erreichen.
Hierfür wäre eine PURL <http://purl.org/terminology-guide-for-move/terminology-1> sinnvoll.
Der bereits registrierten Domain <http://purl.org/terminology-guide-for-move> wird also noch ein `/terminology-1`angehängt.
Die PURL kann dann nach der Erstellung genutzt werden, um genau auf die Unterseite zu leiten.

Um nicht für jede einzelne Unterseite eine eigene subdomain anlegen zu müssen, kann auch die Option `partial` genutzt werden.
Da das Tutorial eine deutsch- und eine englischsprachige Version unterscheidet, die über einen Domain-Bestandteil differenziert werden (zum Beispiel in <https://sarndt-tib.github.io/terminology-guide-for-move/#/de/tutorial-6>), muss hier eine eigene Subdomain ergänzt werden, in diesem Fall <http://purl.org/terminology-guide-for-move/de/>.
Der PURL Type/ HTTP Status Code muss dabei auf `partial` gesetzt werden.
<http://purl.org/terminology-guide-for-move/de/tutorial-6> leitet dann weiter auf die Unterseite <https://sarndt-tib.github.io/terminology-guide-for-move/#/de/tutorial-6>.
Auch jede beliebige andere PURL mit einem korrekten PURL-Namen löst mit dieser Konfiguration auf das richtige Ziel auf, z.B. <http://purl.org/terminology-guide-for-move/de/About> auf <https://sarndt-tib.github.io/terminology-guide-for-move/#/de/About>.

Für das mit OpenRefine erzeugte Beispieldatenvokabular (vgl. [Konversion nach RDF)](tutorial-11.md)) hatten wir bereits eine PURL verwendet.
Auch diese wurde über den PURL-Dienst als Subdomain von <http://purl.org/terminology-guide-for-move> als <http://purl.org/terminology-guide-for-move/testvocab> registriert.
Sie leitet mit HTTP-Status-Code `303 See Other` zur Rohdatei auf GitHub, die unter <https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/develop/OpenRefine_Templates/OpenRefineTemplate_wExampleData_tsv.ttl> erreichbar ist.

Die Identifier der einzelnen Entitäten des Vokabular beinhalten diese PURL als Bestandteil, da sie als Basis-IRI für das Vokabular verwendet wurde.
Wir hatten zum Beispiel Entitäten wie <http://purl.org/terminology-guide-for-move/testvocab/Concept5> angelegt.
Auch diese könnten jetzt mit einer PURL aufgelöst werden, wofür aber noch weitere Konfiguration notwendig ist.
Die aktuelle Konfiguration löst einen `404 Not found`-Fehler aus.
Mit einer neuen partiellen Weiterleitung von <http://purl.org//terminology-guide-for-move/testvocab/> auf <https://raw.githubusercontent.com/SArndt-TIB/terminology-guide-for-move/refs/heads/develop/OpenRefine_Templates/OpenRefineTemplate_wExampleData_tsv.ttl#>, also auf ein Fragment des Vokabulars, wird die Auflösung der Entitäten-Identifier des Vokabulars zumindest auf das gesamte Vokabulardokument möglich.
<!-- Je nach Browser wird auch gleich der Sprung an die richtige Stelle im Dokument vorgenommen. -->

* [ ] TODO: zeigen, wie man auf eine versionierte Version auflösen kann.
<!-- * [ ] TODO: zeigen, wie man auf einzelne Begriffe auflöst? die müssten dann aber auch als eigenes Dokument angelegt werden, was einen weiteren Prozessierungsschritt erfordert... -->

### w3id

* <https://w3id.org/>

### Helmholtz

## Weiterführende Links


<!-- [URI]: ## "Uniform Resource Identifier" -->