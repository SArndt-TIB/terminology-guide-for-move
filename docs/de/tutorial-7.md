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

Ein weitere Problem besteht auch darin, dass eine terminologische Ressource auch einmal umziehen kann.
Der ursprüngliche Identifier wäre dann nicht mehr der gültige Link zur Ressource und müsste aktualisiert werden - und zwar überall, wo er zu Referenzwecken verwendet wird!
Um dies zu vermeiden, verwendet man normalerweise gleichbleibende Identifier sowohl für die terminologiscghe Ressource als Ganzes, als auch für die einzelnen enthaltenen Elemente.
Diese kann man zusätzlich mit Informationen über die Version anreichern und auch den Zugangslink auf verisonierte Daten mitliefern.
So hat man zur Zitation eines Vokabular und eines Begriffs immer einen identischen Identifier für die gesamte terminologische Ressource und den Begriff, kann aber dennoch klar auf eine bestimmte Version Bezug nehmen.

## Welche Identifier-Services gibt es?

### PURL.org

### w3id

### Helmholtz

## Wie richte ich Identifier ein?

<!-- [URI]: ## "Uniform Resource Identifier" -->