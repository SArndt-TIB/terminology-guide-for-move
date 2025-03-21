# Validierung, Qualitätsprüfung, FAIRness

## FAIRness eines Vokabulars

Auch Terminologien, die für das Semantic Web aufbereitet werden, sollen am Ende den [FAIR-Prinzipien](https://www.go-fair.org/fair-principles/) genügen.
Das bedeutet, sie müssen **F**indable (auffindbar), **A**ccessible (zugänglich), **I**nteroperable (interoperabel) und **R**e-Usable (nachnutbar) sein.
Die FAIR-Prinzipien legen eine Reihe von Kriterien fest, die erfüllt sein müssen, damit eine Ressource FAIR ist.
Inzwischen wurden diese Kriterien auch schon im Sinne "semantischer Artefakte" (z.B. SKOS-Vokabulare, wie wir es hier erstellt haben) interpretiert und in entsprechenden Prüftools implementiert. Ein solches Tool ist der [FOOPS Validator](https://foops.linkeddata.es/FAIR_validator.html), in den man einfach nur den Link einer Ressource eingeben muss, um eine Einschätzung ihrer FAIRness gegeliedert nach den einzelnen FAIR-Prinzipien zu bekommen.

Versuchen wir dies einmal mit dem im GitHub-Repositorium abgelegten Test-Vokabular, das wir im Schritt [Tabellarische Datenverwaltung für OpenRefine](tutorial-13.md) erstellt haben und für das wir in [Identifier erstellen](tutorial-7.md#purlorg) die PURL <http://purl.org/terminology-guide-for-move> eingerichtet hatten.

<!-- der datei fehlen noch die metadaten, und ein `a owl:Ontology` statement, da wird aktuell noch gar nichts erkannt -->

<details>
<summary>Ergebnis des FOOPS-Validators</summary>

![](images/FOOPS_eval_of_test_vocab.png)

</details>

* jskos
* SKOS Play
* Metadata validation