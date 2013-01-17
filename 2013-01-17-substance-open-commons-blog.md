## Inhalte als Daten: Offenes digitales Publizieren mit Substance

Die Erstellung von Inhalten sowie deren Verteilung stellt uns im digitalen Zeitalter vor eine Reihe neuer Herausforderungen. In diesem Artikel werden zunächst Anforderungen skizziert, die an moderne Publikationssysteme gestellt werden. In einem weiteren Schritt werden Lösungsansätze dargestellt, wie diese Anforderungen mit Hilfe Benutzer-orientierter Software umgesetzt werden können.

Mit [Substance](http://interior.substance.io), einer offenen Plattform zur kollaborativen Erstellung und Verteilung von digitalen Inhalten möchten wir ausserdem ein Projekt vorstellen, das diese Lösungsansätze aufgreift und umsetzt. Die Entwicklung von Substance erfolgt öffentlich, finanziert wird das Projekt mittels [Crowd-Funding](http://pledgie.com/campaigns/18902). Es soll als moderne Alternative zu existierenden Publikationssystemen dienen.


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


### Separate content from presentation

Many traditional publishing systems store rich markup (such as HTML) and thus only allow publishing in that same format, which is a serious limitation when it comes to multi-platform publishing. How would you turn an HTML document into a printable version? How would you optimize it for Ebook Readers that use special document formats (e.g. Amazon Kindle)? By storing content (plain text) and annotations separately, users gain the ability of transforming their documents into any format they need.

### Structured Composition

By considering a document a sequence of content elements rather than one big chunk of formatted text, document editors can provide a better way of writing semantically structured content, as opposed to visually optimized layouts as we know them from traditional word-processors.

![](http://interior.substance.io/images/illustrations/semantic-writing-elements.png)

### Offline Editing

We've seen the drawbacks of fully web-based publishing solutions, such as high latency and data loss. It turned out that providing an offline editor can significantly improve the user experience during editing and guarantee data security. Importantly information will stay private until users synchronize their publication with a public web-server. Moreover, authors can continue editing even if there's no internet connection.

### Support for Collaboration

Authoring a publication is an iterative process that may involve many authors that are able to simultaneously edit a single document. During that process users should be enabled to add markers and comments to certain text fragments. Markers and comments should stay out of the user's way, and only be shown contextually (e.g. when the text cursor is matching the corresponding marker).

### Extensibility

Editing requirements are fundamentally different among application domains. While book authors are comfortable with headings, text and images, scientists may demand more advanced content types such as formulas, data-tables and visualizations to prove their research findings. Publishing systems should feature a simple plugin system in order to allow user-specific content types.


# Substance

Substance is a content creation tool and a simple multi-format publishing platform. Whether you produce stories, books, documentations or scientific papers, Substance provides the tools that allow you to create, manage and share your content. It is being built with the idea of Open Knowledge in mind. So if you'd like to publish, comment on and collaborate around public documents, open access research or public domain texts, Substance may be for you.

![](http://interior.substance.io/images/campaign/substance.png)

The Substance eco-system consists of an offline editing tool (The Substance Composer) and an online multi-platform publishing system (Substance.io).

### Open Source

Behind the scenes Substance is mainly composed by a stack of [open source modules](http://interior.substance.io/modules/composer.html) that are publicly released under the Open Source MIT license, so anyone can contribute and help developing an open standard for annotated text. Substance is meant to be an interoperable platform, rather than a product. It's infrastructure can be used by anyone to build specialized applications on top of it.

### Content is data

Substance considers **content as data**, which makes them accessible to computers and allows new ways of processing them. Documents can not only be viewed, they can be queried, just like a database. 

### Semantic editing

Instead of editing a big canvas, Substance documents are composed of content elements. While existing solutions (like Google Docs) bring traditional word-processing to the web, Substance focusses on content, by leaving the layout part to the system, not the user. Because of the absence of formatting utilities, it suggests structured content-oriented writing.

### Custom Element Types

Substance comes with a predefined set of element types. Out of the box you can choose from headings, text and images. However, it is easy to implement your own element types, and use it with your tailored version of the Substance Composer.

# Substance needs your help!

After an experimental phase of two years now, our next goal is getting it ready for production. So we sat down, worked out a roadmap and launched a campaign to back development costs.

http://pledgie.com/campaigns/18902

With the help of your donation we could make it happen, which is exciting! If you like the ideas proposed and want to see them in action, please support us.

Lastly, here's how the Substance Composer looks in action:

<iframe src="http://player.vimeo.com/video/56703462" width="500" height="281" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
