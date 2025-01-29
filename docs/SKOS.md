# SKOS - eine Einführung

```yaml
key: value

```

```markdown
# Header

* funny _i_

```

```turtle
@prefix sh:      <http://www.w3.org/ns/shacl#> .
@prefix dash:    <http://datashapes.org/dash#> .
@prefix rdf:     <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:    <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:     <http://www.w3.org/2001/XMLSchema#> .
@prefix ex:      <http://example.org/> .
@prefix skos: <http://www.w3.org/2004/02/skos/core#> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix owl: <http://www.w3.org/2002/07/owl#> .
@prefix dcat: <http://www.w3.org/ns/dcat#> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix m4i: <http://w3id.org/nfdi4ing/metadata4ing#> .
@prefix org: <http://www.w3.org/ns/org#> .

skos:Concept a rdfs:Class, sh:NodeShape ;
    dcterms:title "Begriffsangaben"@de ;
    dcterms:title "Information about the concept"@en;
    sh:targetClass skos:Concept ;
    sh:closed false ;
    # owl:imports <https://gitlab.com/arndts/Playground/-/raw/develop/SourceNodeShape.ttl> ;
    sh:property [
        a sh:PropertyShape ;
        sh:path ex:id ;
        sh:minCount 1;
        sh:maxCount 1;
        sh:order 1 ;
        sh:group ex:TermGroup ;
        sh:name "lokaler Identifier des Begriffs"@de;
        # sh:name "local identifier"@en;
        sh:description "z.B. eine Zahl oder ein alphanumerischer String, der im Vokabular noch nicht verwendet wird, oder eine für das Vokabular reservierte uuid"@de;
    ]
    ;
    sh:property [
        a sh:PropertyShape ;
        sh:path skos:prefLabel;
        sh:minCount 1;
        sh:maxCount 1;
        sh:datatype rdf:langString ;
        sh:languageIn ("en" "de");
        sh:name "bevorzugte Benennung"@de ;
        # sh:name "preferred term"@en;
        sh:description "Tragen Sie hier bitte die gängigste Benennung für den Begriff ein."@de;
        sh:order 3 ;
        sh:group ex:TermGroup
    ].
```
