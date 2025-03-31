# Umwandlung nach RDF

> :warning: Der CSV-RDF-Mapper Workflow ist noch nicht voll funktionsfähig! Wir arbeiten noch daran!

Graph, der am 2025-03-10 bei CSV-RDF-Mapper rausgekommen ist

``` turtle
@prefix dct: <http://purl.org/dc/terms/>.
@prefix foaf: <http://xmlns.com/foaf/0.1/>.
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix skos: <http://www.w3.org/2004/02/skos/core#>.
@prefix ex: <http://example.org/>.
@prefix met: <http://w3id.org/nfdi4ing/metadata4ing#>.
@prefix d: <http://www.w3.org/ns/dcat#>.

ex:Author1
    a ex:Author;
    ex:id "1";
    met:hasOrcidId "https://orcid.org/0000-0002-0871-8995";
    foaf:firstName "Max";
    foaf:lastName "Muster".
ex:Author2
    a ex:Author;
    ex:id "2";
    met:hasOrcidId "https://orcid.org/0000-0002-0871-8994";
    foaf:firstName "Jane";
    foaf:lastName "Doe".
ex:Author4
    a ex:Author;
    ex:id "4";
    met:hasOrcidId "https://orcid.org/0000-0002-0871-8993";
    foaf:firstName "Harro";
    foaf:lastName "Maier".
ex:Source2
    a ex:Source;
    ex:id "2";
    dct:creator ex:Authornull;
    dct:issued "2020-07-15"^^xsd:date;
    dct:publisher "Wikidata";
    dct:title "parking search traffic"^^rdf:langString;
    d:accessURL
        "https://www.wikidata.org/w/index.php?title=Q97379970&oldid=1936875884"^^xsd:anyURI.
ex:Source500
    a ex:Source;
    ex:id "500";
    dct:creator ex:Author4;
    dct:issued "2022-05-01"^^xsd:date;
    dct:publisher "TIB";
    dct:title "Lexikon"^^rdf:langString;
    d:accessURL "http://www.example.com/quelle"^^xsd:anyURI.
ex:TermRelation1
    a ex:TermRelation;
    ex:id "1";
    rdf:object skos:Concept4;
    rdf:predicate "http://www.w3.org/2004/02/skos/core#broader";
    rdf:subject skos:Concept3 .
skos:Concept1
    a skos:Concept;
    ex:editorialStatus "draft";
    ex:exampleSentence "Satz als Benutzungsbeispiel"^^rdf:langString;
    ex:id "1";
    ex:mathSymbol "Bsp.";
    dct:created "12.12.2023"^^xsd:date;
    dct:creator ex:Author1;
    dct:modified "12.12.2024"^^xsd:date;
    dct:source ex:Source500;
    dct:subject "cet";
    skos:altLabel "Sonnabend"^^rdf:langString;
    skos:definition
    "sch\u00f6nster Tag der Woche an dem man alles machen kann"^^rdf:langString;
    skos:editorialNote "Samstag ist gro\u00dfartig"^^rdf:langString;
    skos:changeNote "2025-03-13 englischsprachige Definition ergänzt"^^rdf:langString;
    skos:prefLabel "Samstag"^^rdf:langString;
    skos:semanticRelation ex:TermRelation3 .
skos:Concept2
    a skos:Concept;
    ex:editorialStatus "draft";
    ex:exampleSentence "Montag nervt"^^rdf:langString;
    ex:id "2";
    ex:mathSymbol "null";
    dct:created "2023-01-01"^^xsd:date;
    dct:creator ex:Author1;
    dct:modified "2024-02-03"^^xsd:date;
    dct:source ex:Source500;
    dct:subject "cet";
    skos:altLabel "null"^^rdf:langString;
    skos:definition "weniger sch\u00f6ner Tag"^^rdf:langString;
    skos:editorialNote "Text f\u00fcr eine Anmerkung"^^rdf:langString;
    skos:changeNote "2025-03-13 englischsprachige Definition ergänzt"^^rdf:langString;
    skos:prefLabel "Montag"^^rdf:langString;
    skos:semanticRelation ex:TermRelation3 .
skos:Concept3
    a skos:Concept;
    ex:editorialStatus "null";
    ex:exampleSentence
        "Der Parkraumsuchverkehr ist in Ballungsr\u00e4umen besonders hoch."^^rdf:langString,
        "null"^^rdf:langString;
    ex:id "3";
    ex:mathSymbol "null";
    dct:created "2025-03-10"^^xsd:date, "null"^^xsd:date;
    dct:creator ex:Author2;
    dct:modified "2025-10-03"^^xsd:date, "null"^^xsd:date;
    dct:source ex:Source2;
    dct:subject "https://purl.org/linsearch/ver";
    skos:altLabel
        "Parkplatzsuche"^^rdf:langString, "Parkraumsuche"^^rdf:langString,
        "Parkverkehr"^^rdf:langString;
    skos:definition
        "Anteil am Stra\u00dfenverkehr der durch die Suche nach verf\u00fcgbarem Parkraum entsteht"^^rdf:langString,
        "null"^^rdf:langString;
    skos:editorialNote
    "TODO: weitere Synonyme suchen"^^rdf:langString, "null"^^rdf:langString;
    skos:changeNote "null"^^rdf:langString;
    skos:prefLabel "Parksuchverkehr"^^rdf:langString, "null"^^rdf:langString;
    skos:semanticRelation ex:TermRelation4, ex:TermRelationnone.
skos:Concept4
    a skos:Concept;
    ex:editorialStatus "null";
    ex:exampleSentence "null"^^rdf:langString;
    ex:id "4";
    ex:mathSymbol "null";
    dct:created "null"^^xsd:date;
    dct:creator ex:Author2;
    dct:modified "null"^^xsd:date;
    dct:source ex:Source2;
    dct:subject "https://purl.org/linsearch/ver";
    skos:altLabel "null"^^rdf:langString;
    skos:definition "null"^^rdf:langString;
    skos:editorialNote "null"^^rdf:langString;
    skos:changeNote "null"^^rdf:langString;
    skos:prefLabel "Stra\u00dfenverkehr"^^rdf:langString;
    skos:semanticRelation ex:TermRelationnone.

```

## Update vom 2025-03-11

``` turtle
@prefix dct: <http://purl.org/dc/terms/>.
@prefix foaf: <http://xmlns.com/foaf/0.1/>.
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix skos: <http://www.w3.org/2004/02/skos/core#>.
@prefix ex: <http://example.org/>.
@prefix sko: <https://www.w3.org/2008/05/skos-xl#>.
@prefix met: <http://w3id.org/nfdi4ing/metadata4ing#>.
@prefix d: <http://www.w3.org/ns/dcat#>.

ex:AltLabel2 a ex:AltLabel; dct:language "de"; sko:literalForm "Sonnabend".

ex:AltLabel4 a ex:AltLabel; dct:language "de"; sko:literalForm "Parkplatzsuche".

ex:AltLabel5 a ex:AltLabel; dct:language "de"; sko:literalForm "Parkraumsuche".

ex:AltLabel7 a ex:AltLabel; dct:language "de"; sko:literalForm "Parkverkehr".

ex:Author1
    a ex:Author;
    ex:id "1";
    met:hasOrcidId "https://orcid.org/0000-0002-0871-8995";
    foaf:firstName "Max";
    foaf:lastName "Muster".
ex:Author2
    a ex:Author;
    ex:id "2";
    met:hasOrcidId "https://orcid.org/0000-0002-0871-8994";
    foaf:firstName "Jane";
    foaf:lastName "Doe".
ex:Author4
    a ex:Author;
    ex:id "4";
    met:hasOrcidId "https://orcid.org/0000-0002-0871-8993";
    foaf:firstName "Harro";
    foaf:lastName "Maier".
ex:PrefLabel1 a ex:PrefLabel; dct:language "de"; sko:literalForm "Samstag".

ex:PrefLabel3 a ex:PrefLabel; dct:language "de"; sko:literalForm "Montag".

ex:PrefLabel6 a ex:PrefLabel; dct:language "de"; sko:literalForm "Parksuchverkehr".

ex:PrefLabel8
a ex:PrefLabel; dct:language "de"; sko:literalForm "Stra\u00dfenverkehr".
ex:PrefLabel9 a ex:PrefLabel; dct:language "de"; sko:literalForm "Schiffsverkehr".

ex:Source2
    a ex:Source;
    ex:id "2";
    dct:creator ex:Authornull;
    dct:issued "2020-07-15"^^xsd:date;
    dct:publisher "Wikidata";
    dct:title "parking search traffic"^^rdf:langString;
    d:accessURL
        "https://www.wikidata.org/w/index.php?title=Q97379970&oldid=1936875884"^^xsd:anyURI.
ex:Source500
    a ex:Source;
    ex:id "500";
    dct:creator ex:Author4;
    dct:issued "2022-05-01"^^xsd:date;
    dct:publisher "TIB";
    dct:title "Lexikon"^^rdf:langString;
    d:accessURL "http://www.example.com/quelle"^^xsd:anyURI.
ex:TermRelation1
    a ex:TermRelation;
    ex:id "1";
    rdf:object skos:Concept4;
    rdf:predicate "http://www.w3.org/2004/02/skos/core#broader";
    rdf:subject skos:Concept3 .
skos:Concept1
    a skos:Concept;
    ex:editorialStatus "draft";
    ex:exampleSentence "Satz als Benutzungsbeispiel"^^rdf:langString;
    ex:id "1";
    ex:mathSymbol "Bsp.";
    dct:created "12.12.2023"^^xsd:date;
    dct:creator ex:Author1;
    dct:modified "12.12.2024"^^xsd:date;
    dct:source ex:Source500;
    dct:subject "cet";
    skos:altLabel "Sonnabend"^^rdf:langString;
    skos:definition
    "sch\u00f6nster Tag der Woche an dem man alles machen kann"^^rdf:langString;
    skos:editorialNote "Samstag ist gro\u00dfartig"^^rdf:langString;
    skos:changeNote "2025-03-13 englischsprachige Definition ergänzt"^^rdf:langString;
    skos:prefLabel "Samstag"^^rdf:langString;
    skos:semanticRelation ex:TermRelation3;
    sko:altLabel ex:AltLabel2;
    sko:prefLabel ex:PrefLabel1 .
skos:Concept2
    a skos:Concept;
    ex:editorialStatus "draft";
    ex:exampleSentence "Montag nervt"^^rdf:langString;
    ex:id "2";
    ex:mathSymbol "null";
    dct:created "2023-01-01"^^xsd:date;
    dct:creator ex:Author1;
    dct:modified "2024-02-03"^^xsd:date;
    dct:source ex:Source500;
    dct:subject "cet";
    skos:altLabel "null"^^rdf:langString;
    skos:definition "weniger sch\u00f6ner Tag"^^rdf:langString;
    skos:editorialNote "Text f\u00fcr eine Anmerkung"^^rdf:langString;
    skos:changeNote "2025-03-13 englischsprachige Definition ergänzt"^^rdf:langString;
    skos:prefLabel "Montag"^^rdf:langString;
    skos:semanticRelation ex:TermRelation3;
    sko:altLabel ex:AltLabelnull;
    sko:prefLabel ex:PrefLabel3 .
skos:Concept3
    a skos:Concept;
    ex:editorialStatus "null";
    ex:exampleSentence
        "Der Parkraumsuchverkehr ist in Ballungsr\u00e4umen besonders hoch."^^rdf:langString,
        "null"^^rdf:langString;
    ex:id "3";
    ex:mathSymbol "null";
    dct:created "2025-03-10"^^xsd:date, "null"^^xsd:date;
    dct:creator ex:Author2;
    dct:modified "2025-10-03"^^xsd:date, "null"^^xsd:date;
    dct:source ex:Source2;
    dct:subject "https://purl.org/linsearch/ver";
    skos:altLabel
        "Parkplatzsuche"^^rdf:langString, "Parkraumsuche"^^rdf:langString,
        "Parkverkehr"^^rdf:langString;
    skos:definition
        "Anteil am Stra\u00dfenverkehr der durch die Suche nach verf\u00fcgbarem Parkraum entsteht"^^rdf:langString,
        "null"^^rdf:langString;
    skos:editorialNote
    "TODO: weitere Synonyme suchen"^^rdf:langString, "null"^^rdf:langString;
    skos:changeNote "null"^^rdf:langString;
    skos:prefLabel "Parksuchverkehr"^^rdf:langString, "null"^^rdf:langString;
    skos:semanticRelation ex:TermRelation4, ex:TermRelationnone;
    sko:altLabel ex:AltLabel4, ex:AltLabel5, ex:AltLabel7;
    sko:prefLabel ex:PrefLabel6, ex:PrefLabelnull.
skos:Concept4
    a skos:Concept;
    ex:editorialStatus "null";
    ex:exampleSentence "null"^^rdf:langString;
    ex:id "4";
    ex:mathSymbol "null";
    dct:created "null"^^xsd:date;
    dct:creator ex:Author2;
    dct:modified "null"^^xsd:date;
    dct:source ex:Source2;
    dct:subject "https://purl.org/linsearch/ver";
    skos:altLabel "null"^^rdf:langString;
    skos:definition "null"^^rdf:langString;
    skos:editorialNote "null"^^rdf:langString;
    skos:changeNote "null"^^rdf:langString;
    skos:prefLabel "Stra\u00dfenverkehr"^^rdf:langString;
    skos:semanticRelation ex:TermRelationnone;
    sko:altLabel ex:AltLabelnull;
    sko:prefLabel ex:PrefLabel8 .
skos:Concept5
    a skos:Concept;
    ex:editorialStatus "null";
    ex:exampleSentence "null"^^rdf:langString;
    ex:id "5";
    ex:mathSymbol "null";
    dct:created "null"^^xsd:date;
    dct:creator ex:Author2;
    dct:modified "null"^^xsd:date;
    dct:source ex:Source2;
    dct:subject "https://purl.org/linsearch/ver";
    skos:altLabel "null"^^rdf:langString;
    skos:definition "null"^^rdf:langString;
    skos:editorialNote "null"^^rdf:langString;
    skos:changeNote "null"^^rdf:langString;
    skos:prefLabel "Schiffsverkehr"^^rdf:langString;
    skos:semanticRelation ex:TermRelationnone;
    sko:altLabel ex:AltLabelnull;
    sko:prefLabel ex:PrefLabel9 .

```