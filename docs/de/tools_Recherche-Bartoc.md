[< Zurück zur Übersicht](tools_Recherche-intro.md)

# BARTOC - das "Basic Register of Thesauri, Ontologies & Classifications"

[BARTOC](https://bartoc.org/) ist ein Verzeichnis zur Recherche nach verschiedenen Arten semantischer Artefakte: inbesondere Thesuauri, Klassifikationen und kontrollierte Vokabulare sind hier verzeichnet; es finden sich jedoch auch weitere Formen terminologischer Dokumentation wie Wörterbücher oder Ontologien.
BARTOC ist dabei nicht auf bestimmte Sprachen oder Domänen beschränkt und erlaubt auch die Aufnahme von Ressourcen,

* die nicht nach Semantic-Web-Standards oder anderen strukturierten Datenformaten aufbereitet und deswegen nur bedingt maschinenlesbar/-verstehbar sind,
* sowie solcher Ressourcen, die einer Zugriffsschranke unterliegen.

BARTOC wird von einer kleinen [Gruppe von Kuratoren](https://bartoc.org/contact) gepflegt, an die man sich wenden kann, um neue Ressourcen aufnehmen oder vorhandene Ressourcen korrigieren zu lassen. Mehr Informationen zum Kuratierungsprozess finden sich in diesem [Video auf dem TIB AV-Portal (DOI: 10.5446/51813)](https://doi.org/10.5446/51813).

Die Recherche in BARTOC erfolgt über die Eingabe freier Suchausdrücke, kann aber auch mit einem Filtersystem durchgeführt werden.
Mit diesem kann man zum Beispiel

* alle Ressourcen mit einer [bestimmten Lizenz](https://bartoc.org/vocabularies?license=http%3A%2F%2Fcreativecommons.org%2Fpublicdomain%2Fzero%2F1.0%2F) oder
* alle Ressourcen, die einem [bestimmten Fach](https://bartoc.org/vocabularies?subject=http%3A%2F%2Fdewey.info%2Fclass%2F0%2Fe23%2F%7C) zugeordnet sind, oder
* alle Ressourcen, die eine [bestimmte Sprache](https://bartoc.org/vocabularies?languages=nl) bedienen, ermitteln.

Die Metadaten der verzeichneten Ressourcen können über eine [API](https://bartoc.org/api/) abgerufen werden.

Neben semantischen Artefakten beinhaltet BARTOC auch eine [Liste vergleichbarer Services](https://bartoc.org/registries), die ebenfalls semantische Artefakte verzeichnen oder sogar durchsuchbar machen und deren (Meta-)Daten über eine Maschinenschnittstelle verfügbar machen.
Auch eine [Liste mit Software](https://bartoc.org/software) zur Bearbeitung von semantischen Artefakten findet sich hier.

Sofern die Vokabulare in einem maschinenlesbaren Format angeboten werden, erlaubt BARTOC für einen Teil der maschinenlesbaren Vokabualare auch die Recherche in ihren Inhalten (das Feature ist noch nicht für alle Vokabularquellen implementiert und gilt noch als experimentell).
Auf dem nachfolgenden Screenshot ist zum Beispiel der Eintrag zu einer im Bibliothekswesen verbreiteten Fächerklassikation, der _Basisklassifikation_, abgebildet.
Im Reiter _Content_ dieses Eintrags kann diese Fachklassifikation dann exploriert werden.
Geöffnet ist hier das Konzept mit der Notation _55.20_ und der Benennung _Straßenfahrzeugtechnik_.
Die Begriffe innerhalb der Basisklassifikation bilden eine Begriffshierarchie, die hier auch navigiert werden kann, zum Beispiel kann man vom Eintrag _55.20 Straßenfahrzeugtechnik_ zu den untergeordneten Begriffen _55.21 Kraftfahrzeuge_, _55.23 Kraftfahrzeugwartung, Kraftfahrzeugreparatur_, _55.24 Fahrzeugführung, Fahrtechnik_ springen.
Dem Eintrag kann zugleich eine persistente ID für das Konzept entnommen werden, in diesem Fall die URI <http://uri.gbv.de/terminology/bk/55.20>.

<a href="de/images/bk@Bartoc.png" target="_blank"><p align="center"><img src="de/images/bk@Bartoc.png" alt="Screenshot von BARTOC, der die Ansicht zur Navigation durch die Basisklassifikation zeigt, insbesondere die Systemstelle 55.20 Straßenfahrzeugtechnik" width="1000" /></p></a>

[< Zurück zur Übersicht](tools_Recherche-intro.md)