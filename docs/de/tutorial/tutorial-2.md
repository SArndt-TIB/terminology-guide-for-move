# Arbeitsumgebung einrichten

## Die Basics

Die Arbeit an einer Terminologie sollte als Projekt verstanden werden, aus dem diverse Produkte entstehen, die langfristig und nachhaltig zur Verfügung gestellt werden sollen.
Insofern ist es sinnvoll, diesen Prozess durch geeeignete Werkezuge zu unterstützen.
Hierbei sind git-basierte Web-Plattformen zu empfehlen.
Diese erlauben einem eine sehr genaue Versionskontrolle, mit der verschiedene Arbeitsstände eines Vokabular abgebildet und fixiert werden können.
Zugleich ermöglichen sie auch eine gute Unterstützung bei der Dokumentation von Fehlern und neuen Anforderungen, sowie bei der Planung und Verteilung von Aufgabung, der Diskussion durch verschiedene Beteiligte bis zum Treffen einer allerseitig akzeptierten Lösung, sowie das Nachvollziehen aller Änderungen.
Wird eine solche Plattform rigoros verwendet, sind zugleich alle Entscheidungen und Änderungen am Projekt transparent und nachvollziehbar dokumentiert.

Wer mit dem Konzept von git und entsprechenden Plattformen nicht vertraut ist, dem empfehlen wir, sich zunächst sich mit ein paar Konzepten vertraut zu machen, die das Arbeiten mit solchen Tools erleichtern.

* [Versionskontrolle  ↗](https://librarycarpentry.github.io/lc-git/01-what-is-git.html#what-is-version-control)
* [Versionskontrolle (Video) ↗](https://git-scm.com/video/what-is-version-control)
* [What is git? (Video) ↗](https://git-scm.com/video/what-is-git)
* [Porjektverwaltung mit Branches und Merging ↗](https://git-scm.com/about/branching-and-merging)
* [Branches auf einen Blick ↗](https://git-scm.com/book/de/v2/Git-Branching-Branches-auf-einen-Blick)
* [Unterschied zwischen git und GitHub (und GitLab) ↗](https://librarycarpentry.github.io/lc-git/01-what-is-git.html#what-are-git-and-github)
<!-- * Wikipedia-Artikel? -->

Auf Plattformen wie GitHub oder GitLab angelegte Projekte können dabei auf diesen Plattformen durch sogenannte Branches und Forks vervielfältigt werden, auf denen sie bearbeitet werden können.
Dabei können sie gleichzeitig mit dem Ursprungsprojekt synchronisiert werden, indem Änderungen vom ursprünglichen Branch in die abgezweigten Branches und Forks übernommen werden können, aber auch andersherum.
Insbesondere die Rückführung von Änderungen auf abgeleiteten Branches und Forks erfolgt über sogenannte _Merge Requests_.
Mit diesen können die Änderungen auch noch einmal durch ein Review gehen, disktuiert und verbessert werden und schlussendlich in das Ursprungsprojekt übernommen werden.
Jede Änderung wird durch einen _Commit_ nachvollziehabr und referenzierbar.

Auch eine Spiegelung des Projekts auf den eigenen Rechner ist möglich.
Man nennt eine solche Spiegelung einen Klon.
Lokal vorgenommene Änderungen können ebenfalls über Commits eingebracht und in Merge Request in das Ursprungsprojekt zurückgeführt werden.
So können Änderungen an einem Projekt in kleinen, nachvollziehbaren Schritten durchgeführt werden und auch von unterschiedlichen Bearbeitern durchgeführt werden.

Externe Personen können das Projekt ebenfalls klonen oder forken, sofern es ein öffentliches Projekt ist, und so ggf. dazu beitragen.
Auch die Einreichung von Information zu Fehlern, Erweiterungsbedarfen oder anderweitiger Vorschläge ist über einen sogenannten Isseu-Tracker möglich.
Dieser sollte nicht nur von Externen genutzt werden, sondern mit ihm sollten auch die eigenen zu erledigenden Arbeiten festgehalten und diskutiert werden.
Insbesondere auf GitLab kann man dadurch gleich noch das Projektmanagement unterstützen.

Da diese Plattformen und git insbesondere für die Softwarenentwicklung gedacht sind, unterstützen sie darüber hinaus auch weitere Aufgaben, die auch für Ressourcen relevant sind, die man nicht als Software werten kann:

* Release Management
* Test-Automatisierung
* Hosting von Websites
* Verwendung von Software wie python etc.

## Unsere Tipps

Falls Sie noch nie mit git, GitHub oder GitLab gearbeitet haben, würden wir Ihnen empfehlen, zunächst die Web-Oberflächen der Plattformen zu nutzen.
Diese bieten inzwischen bereits sehr gute Möglichkeiten zur Bearbeitung von Dateien, zum Branchen, Forken, Mergen und allem, was Sie für ein kleines Vokabularprojekt benötigen. 
Dateien können auch heruntergeladen und lokal bearbeitet werden. Es ist nicht zwingend erforderlich, dass Sie ein Kommandozeilentool verwenden, um die Dateien wieder auf den Server zu bringen - dies können Sie auch über einen Upload über das Web-Interface erreichen.
Nützlich ist auch das Anlegen eines Repositoriums, in dem Neulinge alle Funktionen testen können. Hier kann man nichts kaputt machen!
Arbeiten einmal zwei Bearbeiter an derselben Datei bzw. an derselben Stelle einer Datei, führt dies zu Konflikten. Diese müssen in einem Review aufgelöst werden. Verzweifeln Sie in diesem Fall nicht, sondern nutzen Sie die Tools zum Vergleichen der Commits auf den Plattformen.

## Konkrete Schritte

1. Lesen Sie sich in die [Basics](#die-basics) ein.
2. Registrieren Sie sich auf GitHub oder GitLab. Falls Sie können und mögen, verwenden Sie eine Instanz ihrer eigenen Institution oder anderer Dienstleister, die zu Ihrer Institution gehören oder zu denen ihre Institution gehört
3. Legen Sie ggf. eine Organisation an, in der das zuküntige Projekt abgelegt sein soll. Falls bereits eine Organisation existiert, lassen Sie sich dort durch die jeweiliegn Maintainer hinzufügen.
4. Erstellen Sie das Repositorium für Ihr Vokabularprojekt (und ggf. eines zum Üben!).
5. Fügen Sie die Mitglieder hinzu und geben Sie Ihnen die notwendigen Berechtigungen.
6. Erarbeiten Sie mit unserem Tutorial die ersten Dateien für das Projekt.
7. Fügen Sie sie dem Projekt hinzu.
8. Geben Sie ein Release heraus, wenn Sie denken, dass das Vokabular so weit ist. Wir empfehlen mindestend die Erledigung der folgenden Tutorial-Teile: [Schritt 4: Vokabular](step-4/README.md), [Schritt 5 - Metadaten](tutorial-6), [Schritt 6 - Identifier](tutorial-7.md), [Schritt 7 - Prüfung](tutorial-9.md) und ggf. [Schritt X - Dokumentation](tutorial-1.md).
9. Führen Sie das Projekt fort.


## Weiterführende Links

* Software für das lokale Arbeiten mit git
  * [git - the simple guide ↗](https://rogerdudler.github.io/git-guide/)
  * [git Download ↗](https://git-scm.com/downloads)
  * [git for Windows ↗](https://git-scm.com/downloads/win)
  * [git for Windows ↗](https://gitforwindows.org/)
* Kurse
  * [Verwendung von _git_ für ein lokales Projekt ↗](https://librarycarpentry.github.io/lc-git/02-getting-started.html)
  * [Library Carpentry: Introduction to Git ↗](https://librarycarpentry.github.io/lc-git/)
  * ["Let's Git - Versionsverwaltung und OpenSource" - Kurs bei openHPI ↗](https://open.hpi.de/courses/git2020): Der Kurs ist ursprünglich als mehrwöchiger Kurs angelegt und braucht etwas Zeit. Dafür enthält er aber auch viele Praxisübungen, sodass man am Ende wirklich mit Git gearbeitet hat. Zudem kann man hier immer wieder zu den Grundlagen zurückkehren, bis man sie verinnerlicht hat.
* Leitfäden
  * [Konfliktmanagement ↗](https://www.nnscript.de/wie-man-merge-konflikte-in-git-loest-ein-umfassender-leitfaden/): Falls einmal ein Merge-Konflikt auftritt, hilft dieser Leitfaden weiter.