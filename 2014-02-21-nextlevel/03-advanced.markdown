# Für Fortgeschrittene

### Im Browser

#### CSS-Floats

* Elemente folgen der Dokumentstruktur
* Inline folgt dem Textfluss
* Block nimmt sich seinen Platz
* Text soll um ein Bild fließen
* Floats lassen Block-Element links oder rechts "schweben", Fluss orientiert sich darum herum
* angefangen, Floats für Layouts zu verwenden
* mehr Flexibilität als mit Tabellen
* natürlich nur ein Hack
* neuere CSS-Layout-Modelle
	* inline-block => folgt Textfluss, stylebar wie ein Block
	* Flexbox => Möglichkeit, einer Seite ein Box-Layout zu verpassen, Kinder in Spalten anzuordnen

#### CSS Präprozessoren

* der neue heiße Scheiß
* SASS
* LESS
* Stylus
* ewig viele mehr
* was soll das?
	* Variablen
	* Verschachtelung
	* Auslagerung gemeinsamer Styles in Funktionen
	* mehr wie richtiger Code

#### AJAX

* Webseiten normalerweise synchron
* Anfrage => Antwort => Seite fertig
* laaangweilig
* Asynchronous JavaScript and XML
* Seitenteile dynamisch anfragen
	* z.B. Newsbox aktuell halten
	* Chats
	* FB lädt ganze Komponenten asynchron
* ja und wie?
	* XMLHttpRequest
	* seit IE 5, andere Browser haben's nachgemacht
	* schickt per JavaScript eine Anfrage an den Server, kann die empfangenen Daten direkt verarbeiten
* jQuery und andere Libraries haben eingebaute AJAX-Wrapper

### Close to the Metal

* Front-End im Browser, Back-End auf dem Server
* Was wo liegt, ist ganz unterschiedlich
	* klassisch
		* alles liegt auf dem Server
		* Anfrage auf Server z.B. in PHP verarbeitet
		* Datenbankabfragen
		* HTML-Seiten werden gebaut
		* HTML wird an Browser geschickt
		* Browser fragt verlinktes CSS, JS, Medien ab
	* moderner
		* Server liefert fast leere HTML-Seite aus
		* CSS, JS
		* JS enthält Großteil der Anwendungslogik
		* JS fragt vom Server Daten ab
		* JS injiziert Templates für Seitenelemente
	* oder auch
		* Datenbank im Browser, ggf. Synchronisierung mit Remote Storage
* Was läuft wo?
	* im Grunde egal, es muss nur eine Runtime geben
		* Client
			* JavaScript
			* Flash
			* Java
		* Server
			* PHP
			* ASP
			* Java
			* JavaScript
* JavaScript?
	* node.js
		* seit 2009
		* nutzt die JavaScript-Engine von Chrome
		* node verteilt seine Arbeit (I/O, Rückgabe) asynchron, schnell
		* kann Websockets => Push vom Server an den Browser
* CMS für HTML-Schubser
	* CMS sind wichtig
	* die meisten Seiten basieren auf CMS
	* Front-End-Entwickler müssen verstehen, welchen Output das CMS produziert
	* Front-End-Entwickler müssen die Möglichkeiten des CMS verstehen, um ggf. Alarm schlagen zu können
	* Front-End-Entwickler müssen zumindest das Templating System ihres CMS verstehen
* Server-Musts für CSS-Friseure
	* kommt auf die Arbeitsteilung im Unternehmen an
	* bei völliger Trennung kann dem Front-End-Dev egal sein, was im Back-End passiert
	* i.d.R. sinnvoll das System zu verstehen, auf dem man arbeitet => Templating, Abbildung von Workflows, Kommunikation mit Back-End-Devs
