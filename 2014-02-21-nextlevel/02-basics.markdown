# Die Basics

### HTML

* Strukturierung von Dokumenten
* Beispiel eines unstrukturierten Blocks Text
* Grundstruktur
    * `<html>`
    * `<body>`
    * `<head>`
* Textauszeichnungen
	* `<p>`
	* `<a>`
	* `<img>`
	* Generics
		* `<span>`, `<div>`

### CSS

* HTML wie gesagt Strukturierung von Information
* früher Möglichkeit, direkt in HTML Optik festzulegen (font-tags, Styling-Attribute)
* führt zu Koppelung von Inhalt und Optik, macht das Dokument unflexibel, schwerer wartbar
* CSS entkoppelt Optik vom Inhalt => CSS-Zen-Garden
* Style-Tag in den Header packen
* Style-Tag-Inhalt in eigene Datei auslagern

### JavaScript

* Dynamisierung der Seite
* interaktive Elemente
* Formularvalidierung im Browser
* asynchrone Datenabfrage per AJAX
* Helfer, z.B. als LESS Runtime, Prüfung von Features (Modernizr)
* wir fügen unserem Text einen einfachen Aufklapper hinzu

### HTML-Tauchkurs

#### Semantik

* Elemente haben Bedeutung!
* `<em>` statt `<i>`, `<strong>` statt `<b>`
* `<article>`
* Microformats
	* hCard-Demo

#### HTML 5

* neuer HTML-Standard
* in Arbeit seit 2004
* im Grunde fertig
* soll 2014 offiziell verabschiedet werden

##### Elemente

* neue Elemente um den Befürfnissen von Web-Dokumenten gerecht zu werden
	* section: Repräsentiert einen beliebigen Abschnitt in einem Dokument oder einer Anwendung.
	* article: Ein selbständiges Stück Inhalt in einem Dokument, z.B. ein Blogeintrag.
	* header: Gruppierung von einleitenden oder der Navigation dienenden Informationen.
	* nav: Ein Bereich, der der Navigation dient.
	* video, audio: Multimedia-Elemente, mit Browser-internem Player und einer API für Player von Drittanbietern.
	* canvas: „Leinwand” zur dynamischen Erzeugung von Grafiken, z.B. für Graphen oder Animationen.
	* main: Der Haupt-Seiteninhalt
* alte Elemente, insbes. darstellend, entfernt
* APIs ohne Ende
	* canvas API
	* Drag-and-drop
	* Cross-document messaging
	* Browser history management
	* Web Storage: Ein Key-Value Speicher ähnlich Cookies, mit größerem Speichervermögen und verbesserter API.
	* Web Workers: Hintergrundprozesse für HTML-Anwendungen.
	* Geolocation
	* Web SQL Database
	* File API: Asynchrone Drag & Drop Dateitransfers vom Desktop ohne vorgeschalteten Upload.

### CSS für den perfekten Look rund um die Uhr

* CSS 3 seit 2000 in Arbeit
* neue Selektoren
	* E[att^=”val”]: Findet E-Elemente, deren att-Attribut mit „val” anfängt.
	* E[att$=”val”]: Findet E-Elemente, deren att-Attribut auf „val” endet.
	* E[att*=”val”]: Findet E-Elemente, deren att-Attribut „val” enthält.
	* E:nth-child(n): Findet E-Elemente, die das nte Kind ihres Elternelements sind.
	* E:first-of-type: Findet E-Elemente, die in ihrer Umgebung das Element ihres Typs sind.
* neue Features
	* Übergänge & Animationen
	* Transformationen in 2D und 3D
	* finale Version von @font-face
	* CSS-Layouts
	* Media Queries
