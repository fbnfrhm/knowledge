# Geschichte
- 1958 Gründung Advanced Research Pojects Agency
- 1969 ARPAnet vernetzt 4 Großrechner in Kalifornien und Utha
- 1972 37 Einrichtungen in USA angeschlossen
- 1974 Entwicklung TCP, später TCP/IP
- 1978 USENET, unabhängig von ARPAnet
- 1981 188 Rechner mit ca. 500 000 Nutzern im Internet
- 1986 Top Level Domains werden ins Leben gerufen
- 1988 erste deutsche Internetprovider Eunet und Xlink
- 1991 Berners-Lee veröffentlicht WWW im Internet sowie HTML
- 1992 1 Mio. Rechner im Internet
- 1994 Gründung des WWC durch Berners-Lee
- 1996 mehr als 16 Mio.
- 1998 Gründung von Google, mehr als 36 Mio.
- 2001 Wikipedia geht online
- 2003 über 50% der Deutschen hat Internet
- 2005 Youtube geht ins Netz --> erstmals wird von Web 2.0 gesprochen
- heute um die 50 Milliarden vernetzter Endgeräte
# Technologien für Webentwicklung
- Client: HTML, CSS3, JS, (Flash), Java Applet, XML
- Server: PHP, Ruby (on Rails), ASP.NET, ColdFusion, JS (NodeJS)
# HTML
- 1991 publiziert durch Entwickler Burners-Lee
- Verbreitet sich rasend schnell als „Programmiersprache“ des Internet
- letzte Version: HTML 5.2 (14.Dez 2017)
- Arbeitsentwurf für 5.3 seit 18.Okt 2018
- keine neuen Versionsnummern

## Grundgerüst
```html
<!DOCTYPE html>
<html lang="de">
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<title>Titel der Website</title>
	</head>
	<body>
		<!-- Logo, Überschrift -->
		<header></header>
		<!--- Navigationsbereich -->
		<nav></nav>
		<!-- Hauptinhalt -->
		<main></main>
		<!-- eigener Abschnitt mit header, Üebrschrift und footer -->
		<article></article>
		<!-- Abschnitt -->
		<section></section>
		<!-- Fußzeile -->
		<footer></footer>
		<!-- Fußnoten, Randnotizen -->
		<aside></aside>
	</body>
</html>
```
## Tags
| Tag                  | Attribute                                                                                                                                                                                                                              | Funktion                                                            |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `<!-- Kommentar -->` |                                                                                                                                                                                                                                        | Kommentar                                                           |
| Universal            | `id`, `class`, `accesskey`, `hidden`, `style`, `title`                                                                                                                                                                                 |                                                                     |
| `<b>`                |                                                                                                                                                                                                                                        | Text-Formatierung: fett                                             |
| `<u>`                |                                                                                                                                                                                                                                        | Text-Formatierung: unterstreichen                                   |
| `<i>`                |                                                                                                                                                                                                                                        | Text-Formatierung: kursiv                                           |
| `<del>`              |                                                                                                                                                                                                                                        | Durchgestrichen                                                     |
| `<address>`          |                                                                                                                                                                                                                                        | Container für Kontaktinformationen                                  |
| `<br>`               |                                                                                                                                                                                                                                        | Zeilenumbruch                                                       |
| `<img>`              | `src`, `alt`, `width`, `height`                                                                                                                                                                                                        | Einbinden von Bildern                                               |
| `<a>`                | `href`, <br> `target` <br>-->\_self = Selbes Fenster / Tab<br>-->**\_blank = Neues Fenster / Tab**<br>-->\_parent = Eltern-Frame<br>-->\_top = Voller Körper des Fensters,<br>`download`, `title`,<br>`type="application/msexcel"`     | Verlinkung                                                          |
| `<div>`              |                                                                                                                                                                                                                                        | eigenständiger Bereich (Block-Level)                                |
| `<span>`             |                                                                                                                                                                                                                                        | wie `<div>` (Inline-Level)                                          |
| `<p>`                |                                                                                                                                                                                                                                        | ein Textabsatz                                                      |
| `<h1>` .. `<h6>`     |                                                                                                                                                                                                                                        | Überschriften                                                       |
| `<em>`               |                                                                                                                                                                                                                                        | Emphasized, Betont, kursiv                                          |
| `<strong>`           |                                                                                                                                                                                                                                        | Hervorgehoben, fett                                                 |
| `<ol>`, `<ul>`       | `start`, `reversed`, `type`                                                                                                                                                                                                            | sortierte, ungeordnete Liste                                        |
| `<li>`               |                                                                                                                                                                                                                                        | Listenelement                                                       |
| `<dl>`               |                                                                                                                                                                                                                                        | Beschreibungsliste                                                  |
| `<dt>`               |                                                                                                                                                                                                                                        | Description Term (zu beschreibendes Wort)                           |
| `<dd>`               |                                                                                                                                                                                                                                        | Description Description (Beschreibung zum Wort)                     |
| `<table>`            |                                                                                                                                                                                                                                        | Tabelle                                                             |
| `<tr>`               |                                                                                                                                                                                                                                        | Table-Row, Zeile                                                    |
| `<td>`               | `colspan` --> verbindet Spalten<br>`rowspan` --> Verbindet Zeilen<br>`colgroup` --> Gruppierung von Spalten                                                                                                                            | Zelle / Datenfeld                                                   |
| `<th>`               | `scope` --> Zeilen oder Spaltenkopf                                                                                                                                                                                                    | Kopfzelle                                                           |
| `<thead>`            |                                                                                                                                                                                                                                        | Tabellenkopf                                                        |
| `<tfoot>`            |                                                                                                                                                                                                                                        | Tabellenfuß                                                         |
| `<tbody>`            |                                                                                                                                                                                                                                        | Tabellenkörper, mindestens einmal                                   |
| `<caption>`          |                                                                                                                                                                                                                                        | Beschriftung, Überschrift, muss nach dem öffnenden `<table>`-Tag    |
| `<form>`             | `action`, `id`, `method` --> POST, GET<br>`name`, `target`, `autocomplete`, `novalidate`                                                                                                                                               | Formular                                                            |
| `<label>`            | `for`                                                                                                                                                                                                                                  | Beschriftung für Eingabefelder                                      |
| `<input>`            | `type` --> text, search, password, tel, url, email, number, range, radio, checkbox, hidden, file, color, date, button, submit, reset, image<br>, `id`, `name`, `placeholder`, `maxlength`, `minlength`, `required`, `pattern`, `value` | Eingabefeld                                                         |
| `<textarea>`         |                                                                                                                                                                                                                                        | mehrzeilige Textfelder                                              |
| `<button>`           |                                                                                                                                                                                                                                        | Button, Schalter                                                    |
| `<select>`           | `name`, `size`, `multiple`                                                                                                                                                                                                                                       | Auswahllisten                                                       |
| `<option>`           | `selected`                                                                                                                                                                                                                                       | Option in der Auswahlliste, muss im `<select>` stehen               |
| `<optgroup>`         |                                                                                                                                                                                                                                        | Gruppierung von Optionen, über der `<option>`, unter dem `<select>` |
| `<fieldset>`         | `disabled`, `form`, `name`                                                                                                                                                                                                             | Gruppierung von Formfelder                                          |
| `<button>`           | `type` --> button, submit, reset                                                                                                                                                                                                       |                                                                     |
|                      |                                                                                                                                                                                                                                        |                                                                     |
- Character Entitites --> `&nbsp` = Non Breakable Space
# CSS
- inline-Style = `style=""` im HTML
- `<style>Definitionen</style>` im Header
- Einbinden einer CSS-Datei:
```html
<link href="myStyle.css" rel="stylesheet" />
```
## Farben
- `rgb(50 50 50);` --> RGB-Modell
- `hsl(50 50 50);` --> HSL-Modell
- `#000000` --> HEX
## Einheiten
- physische Längenmaße: `in`, `cm`, `px`
- relative Längenmaße: `em`, `ex`, `vw`, `vh`, `vmin`, `vmax`, `%`
- Winkel: `deg`, `rad`
- Zeit: `s`, `ms`
## Selektoren
| Selektor       | Beispiel                                                                                                                                                                                                                                                                                                                                                                                                        |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Typ            | `body {}`                                                                                                                                                                                                                                                                                                                                                                                                       |
| Universal      | `* {}`                                                                                                                                                                                                                                                                                                                                                                                                          |
| Klasse         | `.myClass {}`                                                                                                                                                                                                                                                                                                                                                                                                   |
| ID             | `#myID {}`                                                                                                                                                                                                                                                                                                                                                                                                      |
| Attribut       | `[Attributname]`,<br>`[name="wert"]` --> sucht Elemente, die genau "wert" sind,<br>`[name~="wert"]` --> sucht Elemente, die das Wort "wert" enhalten,<br>`[name$="wert"]` --> sucht Elemente, die mit "wert" enden,<br><code>[name\|="wert"]</code> --> sucht Elemente, die Wort "wert" mit `-` getrennt,<br>`[name^=wert]` --> beginnt mit Zeichenkette "wert",<br>`[name*=wert]` --> enthält die Zeichenkette |
| Pseudoklassen  | `:empty`, `:first-child`, `:last_child`, `:nth-child`,<br> `:link`, `:visited`, `:hover`, `:active`, `:focus`,<br>`:disabled`, `:enabled`, `:checked`,<br>`:valid`, `:invalid`, `:in-range`, `:out-of-range`                                                                                                                                                                                                    |
| Pseudoelemente | `::first-line`, `::first-letter`,<br>`::before`, `::after`,<br>`::backdrop`,<br>`::selection`, `::placeholder`                                                                                                                                                                                                                                                                                                          |
## Kombinatoren
| Kombinator            | Beispiel             |
| --------------------- | -------------------- |
| Kindkombinator        | `elem > child {}`    |
| Nachfahrenkombinator  | `elem child {}`      |
| Nachbarkombinator     | `elem + neighbor {}` |
| Geschwisterkombinator | `elem ~ bro {}`      |

```html
<div id="parent">
	<div id="child">
		<div id="descendant"></div>
	</div>
</div>
<div id="neighbour"></div>
<div id="sibling"></div>
```
## Eigenschaften
| Eigenschaft                                               | Bedeutung                                                   |
| --------------------------------------------------------- | ----------------------------------------------------------- |
| `color`                                                   | Schriftfarbe                                                |
| `background-color`, `background-image`, `linear-gradient` | Hintergrund                                                 |
| `transition`, `animation`, `offset`                       | Animation                                                   |
| `border-...`                                              | Rahmen                                                      |
| `cursor`                                                  | Mauszeiger                                                  |
| `position` --> `relative`, `absolute`                     | Position                                                    |
| `top`, `left`                                             | Position im Bezug zum Elternelement                                                            |
| `list-style`                                              | Aufzählungszeichen anpassen                                 |
| `content`                                                 | Inhalt abändern                                             |
| `display`                                                 | Anzeigetyp: `block`, `inline-block`, `none`, `flex`, `grid` |
| `margin`                                                  | Außenabstand                                                |
| `padding`                                                 | Innenabstand                                                |
| `gap`                                                     | Spaltenabstände                                             |
| `text-align`                                              | horizontale Ausrichtung (für `inline`)                      |
| `vertical-align`                                          | vertikale Ausrichtung (`inline`)                            |
| `margin-left`, `margin-right`                             | zum Horizontalen Zentrieren beides auf `auto` (`block`)     |
| `height`, `width`                                         | Höhe, Breite                                                |
| `flex-direction` --> `row`, `column`                      | horizontale o. vertikale Ausrichtung (`flex`)               |
| `flex-wrap` --> wrap, nowrap                              | Umbruch                                                     |
| `grid-template-columns`                                   | Festlegung von Spalten und deren Aufteilung                 |
| `grid-template-areas`                                     | Bestimmung welche Zelle zu welchem Bereich gehört           |
| `grid-area`                                               | Festlegung des Bereichs in dem ein Element angezeigt wird   |
| `grid-row: start / end`                                   | Zuweisung der Zeilen                                        |
| `grid-column: start / end`                                | Zuweisung der Spalten                                       |
| `@import 'pfad'`                                          | Auslagern von Formatierungsteilen                           |
| `@media(Bedingung)`                                       | Media-Queries, Spezielle Eigenschaften je nach Bedingung    |
|                                                           |                                                             |
# JavaScript
- 1995 Einführung durch Netscape
- ECMAScript = Industriestandard für JS
- Einbindung mittels `<script>`-Tag
```html
<script src="myScript.js"></script>
```
- `'use strict'` nicht vergessen!
## Variablen, Arrays
```js
// Variablen deklarieren
let myVar = "Hallo, Welt!";
//Konstanten deklarieren
const myConst = "Tschüss, Welt!";
// Arrays 
let myArr = ["Saab", "Volvo", "BMW"];
myArr[0] = "VW" // Array --> ["VW", "Volvo", "BMW"]
let matrix = new Array(3);
```
## Kontrollverzweigungen
```js
if (myVar === 1) {
	console.log("myVar ist 1");
}
else {
	console.log("myVar ist nicht 1");
}
```

```js
const expr = 'Papayas';
switch (expr) {
  case 'Oranges':
    console.log('Oranges are $0.59 a pound.');
    break;
  case 'Mangoes':
  case 'Papayas':
    console.log('Mangoes and papayas are $2.79 a pound.');
    // Expected output: "Mangoes and papayas are $2.79 a pound."
    break;
  default:
    console.log(`Sorry, we are out of ${expr}.`);
}
```
### Schleifen
```js
let n = 0;
while (n < 3) {
  n++;
}
console.log(n);
// Expected output: 3
```

```js
let result = '';
let i = 0;
do {
  i = i + 1;
  result = result + i;
} while (i < 5);
console.log(result);
// Expected output: "12345"
```

```js
let str = '';
for (let i = 0; i < 9; i++) {
  str = str + i;
}
console.log(str);
// Expected output: "012345678"
```
## Ausgabe
| Aufruf                                               | Funktion                        |
| ---------------------------------------------------- | ------------------------------- |
| `document.write(var)`                                | Auf dem DOM ausgeben            |
| `console.log(str)`                                   | Auf die Konsole schreiben       |
| `let hello = prompt("Hello World!", "defaultValue")` | Text-Eingabe über Extra-Fenster |
| `alert("AAAAALLLLLARRRMMM!!!!")`                     | Text-Ausgabe über Extra-Fenster |                                                     |                                 |
## Funktionen
```js
function ggT(a, b){
    if(b == 0)
        return a;
    return ggT(b, a%b);
}
```
## Selektion von DOM-Elementen
| Aufruf                                    | Funktion                                   |
| ----------------------------------------- | ------------------------------------------ |
| `document.getElementByID('id')`           | Element über `id`-Attribut selektieren     |
| `document.getElementsByName('name')`      | Element über `name`-Attribut selektieren   |
| `document.getElementsByTagName('name')`   | Element über `<tag>` selektieren           |
| `document.getElementsByClassName('name')` | Element über `class`-Attribut selektieren  |
| `document.querySelector('Selektor')`      | Element über CSS-like Selektoren auswählen |
| `elem2 = elem.parentNode`                 | Eltern-Element des Elements                |
| `elem2 = elem.nextSibling`                | Nächstes Geschwister-Element               |
| `elem2 = elem.previousSibling`            | Vorheriges Geschwister-Element                                           |
## Manipulation des DOM
| Aufruf                                      | Funktion                                                                               |
| ------------------------------------------- | -------------------------------------------------------------------------------------- |
| `elem.appendChild(child)`                   | Knoten an das Ende der Liste von Kindern eines Eltern-Knoten anfügen                   |
| `elem.insertBefore(newNode, referenceNode)` | Knoten vor einen Referenz-Knoten als Kind eines spezifizierten Eltern-Knoten           |
| `elem.removeChild(child)`                   | Das was passiert wenn Abtreibung                                                       |
| `document.createElement('h2')`              | `<h1>`-Element erzeugen, kann dann mit `appendChild` / `insertBefore` verwendet werden |
| `document.write("<h1>Überschrift</h1>")`    | Direkt auf den DOM schreiben                                                                                       |

# PHP
## Variablen & Kommentare
- PHP hat keine Typisierung
```php
<?php
	// Das ist ein Kommentar
	# Das ist ein Kommentar
	/*
	Das ist ein Kommentar
	*/
	
	$txt = "PHP";  
	echo "I love $txt!";
	var_dump($txt);
?>
```
## Arrays
```php
<?php  
	$cars = array("Volvo","BMW","Toyota");  
	var_dump($cars);  
?>
```
## Funktionen
```php
<?php
	function myTest() {  
	  $x = 5;
	  echo "<p>Variable x inside function is: $x</p>";  
	}  
	myTest();
?>
```
## Klassen
```php
<?php  
class Car {  
  public $color;  
  public $model;  
  public function __construct($color, $model) {  
    $this->color = $color;  
    $this->model = $model;  
  }  
  public function message() {  
    return "My car is a " . $this->color . " " . $this->model . "!";  
  }  
}  
  
$myCar = new Car("black", "Volvo");  
echo $myCar -> message();  
echo "<br>";  
$myCar = new Car("red", "Toyota");  
echo $myCar -> message();  
?>
```
## String-Funktionen
```php
<?php
	echo strlen("Hello world!"); // outputs 12
	echo str_word_count("Hello world!"); // outputs 2
	echo strrev("Hello world!"); // outputs !dlrow olleH
	echo strpos("Hello world!", "world"); // outputs 6
	echo str_replace("world", "Dolly", "Hello world!"); // outputs Hello Dolly!
?>
```
## Verzweigungen
```php
<?php
	if ($a > $b) {
	    echo "a ist größer als b";
	} elseif ($a == $b) {
	    echo "a ist gleich b";
	} else {
	    echo "a ist kleiner als b";
	}

	switch ($a) {
    case 0:
        echo "a ist 0";
        break;
    case 1:
        echo "a ist 1";
        break;
    default:
        echo "a ist weder 0 noch 1";
	}
?>
```
## Schleifen
```php
<?php
	for ($i = 0; $i < 10; $i++) {
	    echo $i;
	}
	
	$i = 0;
	while ($i < 10) {
	    echo $i;
	    $i++;
	}

	$i = 0;
	do {
	    echo $i;
	    $i++;
	} while ($i < 10);

	$arr = [1, 2, 3, 4, 5];
	foreach ($arr as $value) {
	    echo $value;
	}
?>
```
