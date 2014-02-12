# Front-End Development

## 21.02.2014 @ next level GmbH

### Die Basics

#### HTML in Blitzgeschwindigkeit

#### CSS in Blitzgeschwindigkeit

#### JavaScript in Blitzgeschwindigkeit

#### Semantisches HTML

#### HTML5

#### CSS 3 und mehr

### Für Fortgeschrittene

#### Im Browser

##### CSS-Floats

##### CSS-Präprozessoren

Seit ein paar Jahren groß im Kommen sind CSS-Präprozessoren. Erwähnenswert sind hier zum Beispiel LESS, Sass und Stylus. All diesen Tools gemein ist, dass nicht mehr reines CSS geschrieben wird. Vielmehr schreibt der Entwickler eine Datei in einer dem jeweiligen Präprozessor eigenen Syntax. Diese wird dann vor der Auslieferung an den Browser von einem Tool auf der Kommandozeile, einem JavaScript oder einem PHP-Skript in CSS umgewandelt.

Was ist an Präprozessoren jetzt so toll? Auf großen Seiten kann CSS schnell ausufern. Selektoren können ewig lang werden. Viel zu viele Elemente teilen sich gemeinsame Styles, die sich nun immer wieder wiederholen. Werte, z.B. Farben, die aufeinander abgestimmt sind, müssen bei Änderung des Grundwertes neu berechnet und eingetragen werden, gerne auch wieder an 50 Stellen im Code.

Präprozessoren können hier sehr bei der Übersichtlichkeit des zu bearbeitenden Codes helfen. Sie bieten Features wie **verschachtelte Regeln**:

```
#header {
	color: black;
	.navigation {
		font-size: 12px;
	}
	.logo {
		width: 300px;
	}
}

wird zu

#header {
	color: black;
}

#header .navigation {
	font-size: 12px;
}

#header .logo {
	width: 300px;
}
```

**Variablen:**

```
$text-color: #444444;

body, a {
	color: $text-color;
}

wird zu

body, a {
	color: #444444;
}

```

**Mixins:**

```
.demo-box() {
	border: 1px solid #000000;
	// noch mehr Zeug
}

#sidebar {
	.box {
		.demo-box();
	}
}

footer {
	.node-otherthing {
		.demo-box();
	}
}

wird zu 

#sidebar .box {
	border: 1px solid #000000;
	// noch mehr Zeug
}

footer .node-otherthing {
	border: 1px solid #000000;
	// noch mehr Zeug
}
```

**Berechnungen und Helfer aller Art:**

```
a:hover {
	color: lighten(10%, $text-color);
	padding: 13px + 0.5em;
}

wird zu

a:hover {
	color: #5E5E5E;
	padding: 19px;
}
```

Diese und andere Features von CSS-Präprozessoren (im Fall dieser Beispiele LESS) bieten dem Developer ein sehr mächtiges Werkzeug, um den an sich starren CSS-Code dynamischer und effizienter zu entwickeln.

##### AJAX

#### Auf dem Server


### Toolchain

#### Was **muss** ein Front-End Entwickler beherrschen?

Die Frage lässt sich leider beim besten Willen nicht allgemeingültig beantworten. Wäre ja auch viel zu einfach. Es folgen stattdessen ein paar Hinweise und Nice-to-haves, die helfen dürften, einen Entwickler besser einzuschätzen.

Es gibt keine spezifischen Tools, die *jeder* Developer beherrschen sollte, weil der Workflow jeder Firma, jedes Teams, jedes Entwicklers grundverschieden sein kann. Jenseits von der Erwartung, dass der Entwickler mit absoluter Standardsoftware wie Office und Photoshop umgehen können sollte, wird es schnell schwammig. Arbeitet der Entwickler in TextMate? BBEdit? Textpad++? Eclipse? NetBeans? Letztlich ist es egal, solange am Ende guter Code dabei herumkommt.

Der dabei entstehende Output sollte valide sein (HTML ist ein Muss, CSS wäre schön). Der Code sollte so gut es geht selbsterklärend sein (Was macht Variable i?) und wenn’s geht auch ein wenig dokumentiert, zumindest an potentiellen Knackpunkten.

Der Entwickler sollte auch eine Strategie für Cross-Browser-Output haben. Sei es, dass er gezielt per Conditional Comments Internet Explorer Versionen anspricht. Oder dass er über Progressive Enhancement / Graceful Degradation mit Tools wie Modernizr dafür sorgt, dass Browser immer nur versuchen, eine Seite so darzustellen, wie ihre Fähigkeiten es auch zulassen.

Kaum vermeiden lässt sich heutzutage auch, dass der Entwickler Ideen hat, mit dem mobile Web umzugehen. Soll heißen, er kann Seiten für Tablets und Smartphones umsetzen, z.B. unter Verwendung von Media Queries. Er weiß, welche Bedienkonzepte für Touch-Displays geeignet sind. Er hat Lösungen parat für Problemfälle wie die Darstellung von großen Tabellen auf kleinen Bildschirmen.

Zu guter letzt ist es nur hilfreich, wenn der Entwickler mit mindestens *einem* Versionierungssystem wie CVS, SVN / Subversion oder Git gearbeitet hat. Welches genau? Egal, solange er sich überhaupt angewöhnt hat, seine Arbeit brav und wie ein echter Teamplayer einzuchecken.

#### Mein ganz persönliches Toolkit

Mein persönlicher Arbeitsablauf unterscheidet sich von Projekt zu Projekt, je nachdem ob der Schwerpunkt der Arbeit mehr im Front-End oder im Back-End liegt. Generell kann ich sagen, dass ich Webseiten mit einer Handvoll Tools entwickele:

* TextMate 2 für Mac OS X ist der Code meiner Wahl
* als Textumgebung verwende ich einen MAMP-Server (Mac, Apache, MySQL, PHP)
* jQuery kommt in fast jedem Projekt zum Einsatz, ist bei CMS wie Drupal sowieso mit dabei
* LESS ist der CSS-Präprozessor in unserem Haus
* LESS Elements ist eine bezaubernde Sammlung an LESS-Mixins für Standard-Aufgaben wie Schatten, Animationen etc.
* mit Modernizr befrage ich den Browser nach seinen Fähigkeiten und kann diese gezielt per CSS und JavaScript ansprechen
* als CSS Reset verwende ich Normalize, da es das Default-Styling von Elementen erhält und lediglich für alle Browser angleicht
* Selectivizr ermöglicht den Einsatz moderner CSS-Selektoren auch auf älteren Browsern

Diese Bibliotheken und Skripte finden sich eigentlich in jedem Projekt wieder, dass ich bearbeite, egal ob sie in einem Drupal-Theme liegen oder einer PHP-Anwendung.

### Recruiting

#### Wie erkennt man einen guten Front-End Developer?

Ein wasserdichtes System, um einen wirklich guten Front-End Developer zu finden, kann ich hier leider nicht offerieren. Was folgt sind jedoch einige Beobachtungen aus den letzten Jahren, die vielleicht in die richtige Richtung weisen mögen.

Es empfiehlt sich selbstverständlich immer, ein wenig das relevante Grundwissen abzuklopfen. Es ist klar, dass der technische Sachverstand des Kandidaten den des Recruiters übersteigt (hoffen wir es mal!), aber mit Grundkenntnissen in den relevanten Themengebieten sollte es zumindest möglich sein, absoluten Bullshit zu erkennen.

Überhaupt sollte ein Kandidat in der Lage sein, aus dem Stegreif über aktuelle Entwicklungen in seiner Branche zu sprechen, die ihn interessieren. Was zählt ist das Interesse, der Wille zur Weiterentwicklung.

Oft fällt es Bewerbern schwer, zu ihren Schwächen zu stehen. Einfach mal einräumen, dass man sich mit HTML5 vielleicht noch nicht so sehr auseinandergesetzt hat? *Undenkbar!* Dann lieber erzählen, dass, ja klar, man sich mit HTML5 auseinander gesetzt hat, es aber noch voller gefährlicher, unerprobter Technologien stecke und somit höchste Vorsicht geboten sei. Bei solchen Spinnereien, und generell bei sehr absolut formulierten Aussagen, wirkt eine einfache Bitte, das doch mal näher zu erklären, wahre Wunder.

Überhaupt ist es das Sahnehäubchen auf dem Entwickler-Cupcake, wenn er nicht nur 50 Fachbegriffe pro Minute absondern kann, sondern auch in der Lage ist, die gleichen Themen auch mal verständlich zu erklären. Fast, als wäre er ein ganz normaler Mensch.

Darüber hinaus enden meiner Meinung nach aber auch schnell die Recruiter-seitigen Möglichkeiten, die Befähigung eines Entwicklers im Gespräch abzuklopfen. Hier beginnt schon bald der Zuständigkeitsbereich des suchenden Unternehmens, den Kandidaten in Tests oder Workshops genauer unter die Lupe zu nehmen. Selbst erfahrenen IT-Leuten kann ich im Gespräch sonst etwas erzählen, was zählt ist auf dem Keyboard.

#### Beispiele für gute / schlechte Front-Ends

Auch dieses Thema lässt sich (leider, leider) nicht gut allgemein abhandeln. Gute Beispiele wie schlechte Beispiele können oft subjektiv sein. Zudem kann eine schlechte Seite über Nacht durch ein gutes Redesign ersetzt werden. Genauso gut kann eine gute Seite schlagartig zu absolutem Schrott werden. Deswegen folgen auch hier nur Dinge, auf die man achten kann.

Ist die Referenzseite zweckmäßig und navigierbar? Der Punkt sollte sich von selbst verstehen. Vermittelt der Kandidat mit seiner Referenz den Eindruck, er könnte eine Seite herstellen, die gut zu bedienen ist? Bei der schnell klar wird, was die Funktion der Seite ist und wie ich diese Funktion nutzen kann?

Ist der Code valide? Niemand freut sich über invalides HTML. Google bestraft diesen Unfug. Browser zeigen Inhalte falsch an oder rechnen sich einen Wolf, um die Fehler im Code zu erkennen und zu kompensieren. Evtl. nicht semantisches Markup erschwert es z.B. Screenreadern, die Inhalte vernünftig zu verarbeiten. *Niemand* freit sich über invalides HTML.

Hat die Seite einen akzeptablen PageSpeed Score? Was nützt die schönste Seite, wenn sie aus welchen Gründen auch immer völlig unperformant ist? PageSpeed, so wie z.B. auch YSlow, ist ein praktisches Hilfsmittel, Optimierungsbedarf an Webseiten festzustellen. Seien es zu große Bilder, langsame Skripte oder verschenkte Bandbreite durch unkomprimierte Inhalte. Wenn ein Kandidat Referenzen mit PageSpeed Resultaten im roten Bereich vorlegt, sollte er besser eine verdammt gute Ausrede parat haben.

Wie viel Selbstgemachtes steckt in der Seite? Will der Kandidat uns gerade weismachen, er könnte CMS *und* Responsive, weil er mal bei Joomla ein fertiges responsives Theme installiert und eine Farbe geändert hat? Einfach mal Firebug oder den WebInspector von Chrome / Safari aufmachen. Einfach mal die Stylesheet-Links anschauen, den Theme-Namen ermitteln, durch Google jagen und das ursprüngliche Theme mit der Referenz vergleichen.

### Der Referent

**Marc-Oliver Teschke** (* 1984) verließ 2004 die romantische Fachwerkstadt Celle, um am *b.i.b. International College* in der romantischen Weltmetropole Paderborn seine Ausbildung zum **staatlich geprüften Informatiker Multimedia** zu absolvieren.

Die Gelegenheit, sich die zwei Ausbildungsjahre anrechnen zu lassen und in nur einem Jahr an der *Southampton Solent University* in der romantischen Engländerstadt Southampton den **BSc Internet Application Development** draufzusetzen, konnte er sich nicht entgehen lassen.

Seit 2007 ist er bei der *PLANWERK 6 websolutions GmbH* in der romantischen Nicht-Köln-Stadt Düsseldorf als **Entwickler für Internet-Anwendungen**, professioneller HTML-Schubser, CSS-Friseur, JavaScript-Bändiger, PHP-Töpfer und Datenbank-Datenbanker tätig und in alle Schritte der Entstehung von Webseiten eingebunden, von Akquise und Planung, Design und Entwicklung bis zu Übergabe und Support.

### Links

#### Für Fortgeschrittene

LESS
Sass
Stylus

#### Toolchain

Conditional Comments
Conditional HTML
Progressive Enhancement
Graceful Degradation
Modernizr
TextMate
MAMP
LESS
LESS Elements
jQuery
Modernizr
Normalize
Selectivizr

#### Recruiting

* [„How to hire a programmer when you're not a programmer” - Basecamp (ehem. 37signals), 2010](http://signalvnoise.com/posts/2628-how-to-hire-a-programmer-when-youre-not-a-programmer)
* [W3C Markup Validation Service](http://validator.w3.org)
* [PageSpeed Insights](http://developers.google.com/speed/pagespeed/insights/)
* [YSlow](https://addons.mozilla.org/de/firefox/addon/yslow/)
* [Firebug](http://getfirebug.com)