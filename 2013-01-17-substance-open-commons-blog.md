## Inhalte als Daten: Offenes digitales Publizieren mit Substance

Die Erstellung von Inhalten sowie deren Verteilung stellt uns im digitalen Zeitalter vor eine Reihe neuer Herausforderungen. In diesem Artikel werden zunächst Anforderungen skizziert, die an moderne Publikationssysteme gestellt werden. In einem weiteren Schritt werden Lösungsansätze dargestellt, wie diese Anforderungen mit Hilfe Benutzer-orientierter Software umgesetzt werden können.

Mit [Substance](http://interior.substance.io), einer offenen Plattform zur kollaborativen Erstellung und Verteilung von digitalen Inhalten möchten wir ausserdem ein Projekt vorstellen, das diese Lösungsansätze aufgreift und umsetzt. Die in Linz entwickelte Software ist [Open Source](http://github.com/substance) und wird mittels [Crowd-Funding](http://pledgie.com/campaigns/18902) finanziert. Es soll schon bald als moderne Alternative zu existierenden Publikationssystemen bereitstehen.

## Anforderungen an moderne Publikationssysteme

### Inhaltserstellung

Inhalte müssen zunächst erstellt werden. Dabei wird Text verfasst, annotiert und strukturiert. Bilder, Tabellen und Listen sind zu ergänzen. Heutzutage wird auch die Unterstützung für interaktive Inhalte (Visualisierungen, interaktive Karten) immer wichtiger und sollte vom Publikationssystem unterstützt werden.


### Qualitätsmanagement

Um die Qualität und Konsistenz von digitalen Inhalten zu gewährleisten, müssen Verleger sogenenannte [Peer-Review](http://de.wikipedia.org/wiki/Peer-Review) Workflows implementieren. Publikationssysteme müssen solche Workflows untersützten. Dabei muss es möglich sein Änderungen vorzuschlagen, Fehler zu melden, sowie mit dem Autor über einen direkten Kommunikationsweg in Verbindung zu treten.


### Publikation

Sobald die Inhalte in angemessener Qualität zur Verfügung stehen werden Sie der Öffentlichkeit zugänglich gemacht. Das Publizieren von Inhalten war in der Vergangenheit ein relativ langwieriger und kostspieliger Prozess, der manuelles eingreifen von Experten erforderte. Mit Hilfe von Software-Werkzeugen kann dieser Teil automatisiert werden. Autoren sollten dabei in der Lage sein, ihre Arbeit selbstständig zu veröffentlichen, ohne die Notwendigkeit von manuellen Schritten.

### Change Management

Selbst nach Anwendung aufwendiger und ausgereifter Review-Prozesse sind Inhalte immer anfällig für Unstimmigkeiten und Fehler. Über die Zeit müssen Teile des Inhalts aktualisiert, zusätzliche Informationen hinzugefügt, und neue Editionen des Dokuments publiziert werden. Aus diesem Grund müssen Publikationssysteme inkrementelle Updates unterstützen, sowie einen einfachen Weg neue Editionen zu veröffentlichen.

### Inhaltsverteilung

Die Verteilung 

In der Vergangenheit galt es Inhalte auf Papier zu drucken, während Informationen heute ebenso elektronisch auf unterschiedlichsten Plattformen (Web, Ebook Readers, Smartphones, etc.) konsumiert werden. Diese Plattformen unterscheiden sich grundlegend. Wünschenswert wäre ein intelligenter Mechanismus der eine Publikation automatisch in eine Vielzahl von Formaten konvertiert (z.B. ePub, HTML, PDF). Damit müssten nicht länger einzelne versionen für jede Plattform manuell erstellt werden.

## Solutions

Im Rahmen der Arbeit an [Substance](http://substance.io) fanden viele Untersuchungen statt. Basierend auf diesen Recherchen möchten wir hier einige Lösungsansätze anführen, die bei der Entwicklung eines digitalen Publikationssystem wichtig sind.


### Trennung von Inhalt und Darstellung

Viele traditionelle Publikationssysteme speichern Text mittels spezieller Auszeichnungssprachen wie HTML. Diese Systeme sind zumeist auf eben dieses eine Ausgabeformat beschränkt, was eine große Limitierung bedeutet. Wie soll ein HTML Dokument in eine ansprechende druckbare Version umgewandelt werden? Wie sollen diese Dokumente für Ebook Reader optimiert werden, die spezielle Formate erfordern (z.B. Amazon Kindle)? Abhilfe schafft die separate Speicherung von Struktur, Plaintext und Annotationen. Dadurch können Benutzer ihre Dokumente in beliebige Ausgabeformate konvertieren.


### Strukturierte Komposition

Herkömmliche Textverarbeitungssysteme betrachten Dokumente als einen durchgehenden Fluss von Text mit Formatierungen, Tabellen und zusätzlichen grafischen Elementen. Im Gegensatz dazu bestehen inhalts-orientierte Dokumente aus einer Sequenz von Inhalselementen. Das dokument wird in einzelne semantisch struktuierte Bereiche geteilt (Überschrift, Text, Bild, Tabelle etc.). Durch das Fehlen von Formattierungswerkzeugen erleichtern solche Systeme dem Benutzer die struktierte Erstellung von Inhalten.


![](http://interior.substance.io/images/illustrations/semantic-writing-elements.png)

### Offline Editing

Rein web-basierte Lösung haben oft den Nachteil langer Antwortzeiten und Datenverlust über unstabile Leitungen. Offline Editoren können die Benutzerfreundlichkeit empfindlich verbessern und zudem Datensicherheit bieten. Informationen bleiben solange privat bis der Benutzer entscheidet seine Publikation mit einem öffentlichen Webserver zu synchronisieren. Benutzer können mit dem Schreiben des Dokuments fortfahren auch wenn keine aktive Internetverbindung besteht.

### Support for Collaboration

Die Erstellung einer Publikation ist ein iterativer Prozess der oft durch mehrere Autoren bewerkstelligt wird. Dies passiert teilweise simulatan. Daher ist es wichtig den Benutzern Werkzeuge zur Kollabation bereitzustellen. Textteile sollen individuell markiert und kommentiert werden können.

### Extensibility

Die Anforderungen an die Inhaltserstellung variert stark zwischen unterschiedlichen Anwendungsdomänen. Während Buchautoren mit traditionellen Inhaltstypen (Überschrift, Text, Bild) arbeiten können, benötigen Wissenschaftler für ihre Publikationen erweiterte Inhaltstypen wie Formeln und Visualisierungen um deren Ergebnisse untermauern zu können. Aus diesem Grund sollten Publikationsysteme hinsichtlich deren unterstützer Inhaltstypen erweiterbar sein. Dadurch können technisch versierte Benutzer fehlende Funktionalität selbst nachrüsten und der Community zur Verfügung stellen.

# Substance

Substance ist ein Sotware-System zur Erstellung und Publikation digitaler Inhalte. Substance untersützt die Erstellung von Büchern, Dokumentationen und wissenschaftlichen Publikationen gleichsam. Es besteht aus einem Editor (Substance Composer) und einer Online-Publikationsplattform (Substance.io).

![](http://interior.substance.io/images/campaign/substance.png)

Das Projekt folgt der Idee von Freiem Wissen, und eignet sich beispielsweise für die Erstellung und Veröffentlichung von Public Domain Texten.


### Open Source

Substance besteht aus mehreren Komponenten die fast gänzlich frei als [Open Source Module](http://interior.substance.io/modules/composer.html) zur Verfügung stehen. Diese Module werden unter der Open Souce MIT Lizenz veröffentlicht und können von jedermann weiterentwickelt werden. Ziel ist es Substance als offene Plattform zu etabliern. Die Infrastruktur kann ohne Einschränkungen genutzt werden und ermöglicht die Entwicklen von spezialiserten Anwendungen.


### Inhalte als Daten

Substance behandelt **Inhalte als Daten**, wodurch sie auch für die elektronsische Weiterverarbeitung zugänglich werden. Dadurch ergeben sich vielfältige neue Möglichkeiten der Verwendung. Dokument können nicht länger nur angezeigt, stattdessen wie eine Datenbank abgefragt werden.


### Inhaltsorientiertes Editieren

Substance Dokumente bestehen aus Content Elemementen. Während existierende Lösungen (wie Google Docs) traditionelle Textverarbeitung für das Web implementieren, konzentriert Substance sich auf rein auf den Inhalt, in dem das Layouting vom System übernommen wird und dem Benutzer diese Aufgabe bewusst abgenommen wird. Die Abwesenheit von Formatierungswerzeugen fördert struktuiertes inhalts-orientiertes Schreiben.


### Erweiterbare Inhaltstypen

Substance comes with a predefined set of element types. Out of the box you can choose from headings, text and images. However, it is easy to implement your own element types, and use it with your tailored version of the Substance Composer.

# Substance needs your help!

After an experimental phase of two years now, our next goal is getting it ready for production. So we sat down, worked out a roadmap and launched a campaign to back development costs.

http://pledgie.com/campaigns/18902

With the help of your donation we could make it happen, which is exciting! If you like the ideas proposed and want to see them in action, please support us.

Lastly, here's how the Substance Composer looks in action:

<iframe src="http://player.vimeo.com/video/56703462" width="500" height="281" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
