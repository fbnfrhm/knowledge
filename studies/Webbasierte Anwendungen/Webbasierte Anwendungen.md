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
- Client: HTML5, CSS3, JS, (Flash), Java Applet, XML
- Server: PHP, Ruby (on Rails), ASP.NET, ColdFusion, JS (NodeJS)
# DOM
- DOM = Document Object Model
- Baumstruktur, jeder Knoten ein Objekt
- Programmierschnittstelle für HTML- und XML-Dokumente
	- Manipulation von Webseiten
	- Interaktion mit dem Nutzer
	- Erstellung dynamischer Inhalte
# HTML
- 1991 publiziert durch Entwickler Burners-Lee
- Verbreitet sich rasend schnell als „Programmiersprache“ des Internet
- letzte Version: HTML 5.2 (14.Dez 2017)
- Arbeitsentwurf für 5.3 seit 18.Okt 2018
- keine neuen Versionsnummern
- Aufgabe: Strukturierung von Inhalten, Interaktivität und Formulare
- Ursprünglicher Zweck: Vereinfachung Informationsaustausch, Schaffung eines universellen Mediums
## Grundgerüst
```html
<!DOCTYPE html>
<html lang="de">
	<head>
		<meta charset="UTF-8">
		<meta name="description" content="Die Heimseite der DHGE">
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
|                      |                                                                                                                                                                                                                                        |                                                                     |
| Universal            | `id`, `class`, `accesskey`, `hidden`, `style`, `title`                                                                                                                                                                                 |                                                                     |
| `<!-- Kommentar -->` |                                                                                                                                                                                                                                        | Kommentar                                                           |
| `<a>`                | `href`, <br> `target` <br>-->\_self = Selbes Fenster / Tab<br>-->**\_blank = Neues Fenster / Tab**<br>-->\_parent = Eltern-Frame<br>-->\_top = Voller Körper des Fensters,<br>`download`, `title`,<br>`type="application/msexcel"`     | Verlinkung                                                          |
| `<address>`          |                                                                                                                                                                                                                                        | Container für Kontaktinformationen                                  |
| `<b>`                |                                                                                                                                                                                                                                        | Text-Formatierung: fett                                             |
| `<br>`               |                                                                                                                                                                                                                                        | Zeilenumbruch                                                       |
| `<button>`           |                                                                                                                                                                                                                                        | Button, Schalter                                                    |
| `<button>`           | `type` --> button, submit, reset                                                                                                                                                                                                       |                                                                     |
| `<caption>`          |                                                                                                                                                                                                                                        | Beschriftung, Überschrift, muss nach dem öffnenden `<table>`-Tag    |
| `<dd>`               |                                                                                                                                                                                                                                        | Description Description (Beschreibung zum Wort)                     |
| `<del>`              |                                                                                                                                                                                                                                        | Durchgestrichen                                                     |
| `<div>`              |                                                                                                                                                                                                                                        | eigenständiger Bereich (Block-Level)                                |
| `<dl>`               |                                                                                                                                                                                                                                        | Beschreibungsliste                                                  |
| `<dt>`               |                                                                                                                                                                                                                                        | Description Term (zu beschreibendes Wort)                           |
| `<em>`               |                                                                                                                                                                                                                                        | Emphasized, Betont, kursiv                                          |
| `<fieldset>`         | `disabled`, `form`, `name`                                                                                                                                                                                                             | Gruppierung von Formfelder                                          |
| `<form>`             | `action`, `id`, `method` --> POST, GET<br>`name`, `target`, `autocomplete`, `novalidate`                                                                                                                                               | Formular                                                            |
| `<h1>` .. `<h6>`     |                                                                                                                                                                                                                                        | Überschriften                                                       |
| `<i>`                |                                                                                                                                                                                                                                        | Text-Formatierung: kursiv                                           |
| `<img>`              | `src`, `alt`, `width`, `height`                                                                                                                                                                                                        | Einbinden von Bildern                                               |
| `<input>`            | `type` --> text, search, password, tel, url, email, number, range, radio, checkbox, hidden, file, color, date, button, submit, reset, image<br>, `id`, `name`, `placeholder`, `maxlength`, `minlength`, `required`, `pattern`, `value` | Eingabefeld                                                         |
| `<label>`            | `for`                                                                                                                                                                                                                                  | Beschriftung für Eingabefelder                                      |
| `<li>`               |                                                                                                                                                                                                                                        | Listenelement                                                       |
| `<ol>`, `<ul>`       | `start`, `reversed`, `type`                                                                                                                                                                                                            | sortierte, ungeordnete Liste                                        |
| `<optgroup>`         |                                                                                                                                                                                                                                        | Gruppierung von Optionen, über der `<option>`, unter dem `<select>` |
| `<option>`           | `selected`                                                                                                                                                                                                                             | Option in der Auswahlliste, muss im `<select>` stehen               |
| `<p>`                |                                                                                                                                                                                                                                        | ein Textabsatz                                                      |
| `<select>`           | `name`, `size`, `multiple`                                                                                                                                                                                                             | Auswahllisten                                                       |
| `<span>`             |                                                                                                                                                                                                                                        | wie `<div>` (Inline-Level)                                          |
| `<strong>`           |                                                                                                                                                                                                                                        | Hervorgehoben, fett                                                 |
| `<table>`            |                                                                                                                                                                                                                                        | Tabelle                                                             |
| `<tbody>`            |                                                                                                                                                                                                                                        | Tabellenkörper, mindestens einmal                                   |
| `<td>`               | `colspan` --> verbindet Spalten<br>`rowspan` --> Verbindet Zeilen<br>`colgroup` --> Gruppierung von Spalten                                                                                                                            | Zelle / Datenfeld                                                   |
| `<textarea>`         |                                                                                                                                                                                                                                        | mehrzeilige Textfelder                                              |
| `<tfoot>`            |                                                                                                                                                                                                                                        | Tabellenfuß                                                         |
| `<th>`               | `scope` --> Zeilen oder Spaltenkopf                                                                                                                                                                                                    | Kopfzelle                                                           |
| `<thead>`            |                                                                                                                                                                                                                                        | Tabellenkopf                                                        |
| `<tr>`               |                                                                                                                                                                                                                                        | Table-Row, Zeile                                                    |
| `<u>`                |                                                                                                                                                                                                                                        | Text-Formatierung: unterstreichen                                   |
- Character Entitites --> `&nbsp` = Non Breakable Space

## HTML-Beispiele
### Links
```html
<a href="seite2.html" target="_blank" title="Weiter">weiter</a>
```
- Verlinkung zu Abschnitten mittels `id` möglich, z.B.: `<a href="#absch2">Abschnitt2</a>
- zum Anfang scrollen mittels: `<a href="#">Hoch</a>`
### Tabellen
![[Pasted image 20231120142029.png]]
```html
<table border="1">
	<caption>Spielplan der U14</caption>
	<thead>
		<tr>
			<th>Spieltag</th> <th>Heim</th>
			<th>Gast</th> <th>Ergebnis</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>25.10.23</th> <td>USV Jena</td>
			<td>Gera Zwötzen</td> <td rowspan="3">&nbsp;</td>
		</tr>
		<tr>
			<th>30.10.23</th> <td>Zeulenroda</td>
			<td>Greiz</td>
		</tr>
		<tr>
			<th>11.11.23</th> <td>Weida</td>
			<td>Ronneburg</td>
		</tr>
	</tbody>
	<tfoot>
		<tr>
			<td colspan="4">Alle Ergebnisse ohne Garantie</td>
		</tr>
	</tfoot>
</table>
```
### Bilder
```html
<img src="picture.jpg" title="This is fine, but I'm not. 💀" alt="This is not fine." width="400">
```
### Listen
```html
<!-- Unordered List -->
 <ul>
	<li>Sport</li>
	<li>Zocken</li>
	<li>Rad fahren</li>
</ul>
<!-- Ordered List -->
<ol>
	<li>Cars</li>
	<li>Cars 2</li>
	<li>Free Guy</li>
</ol>
<!-- Description List -->
<dl>
	<dt>CU</dt>
		<dd>Kupfer</dd>
	<dt>AG</dt>
		<dd>Silber</dd>
</dl>
```
### Forms
```html
<form action="" method="get" name="user-registration">
	<fieldset id="intrests" disabled>
		<legend>Interessen:</legend>
		<label for="lesen">Lesen
			<input type="checkbox" name="inter" 
			value="1" id="lesen" checked>
		</label><br>
		
	</fieldset>
	<br>
	<label for="marke">Automarke:<br>
		<select name="marke" id="marke"
		  multiple size=2>
			<option value="1">Audi</option>
			<option value="2">BMW</option>
		</select>
	</label><br>
	<label for="vname">Vorname: <br>
	    <input  type="text" id="vname" name="vname" 
	            size="10" maxlength="10" minlength="4" 
	            placeholder="hier Vorname eintragen">
	</label><br><br>
	<input type="submit" value="Senden">&nbsp;&nbsp;&nbsp;
	<input type="reset" value="Zurücksetzen">
</form>
```

# CSS
- Standard des W3C
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
- `red` --> Farbnamen
## Einheiten
- physische Längenmaße: `in`, `cm`, `px`
- relative Längenmaße: `em` (Schrift), `ex`, `vw` (Viewport), `vh`, `vmin`, `vmax`, `%`
- Winkel: `deg`, `rad`
- Zeit: `s`, `ms`
## Selektoren
| Selektor       | Beispiel                                                                                                                                                                                                                                                                                                                                                                                                        |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Typ            | `body {}`                                                                                                                                                                                                                                                                                                                                                                                                       |
|                |                                                                                                                                                                                                                                                                                                                                                                                                                 |
|                |                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Universal      | `* {}`                                                                                                                                                                                                                                                                                                                                                                                                          |
| Klasse         | `.myClass {}` / `p.myClass {}`                                                                                                                                                                                                                                                                                                                                                                                  |
| ID             | `#myID {}`                                                                                                                                                                                                                                                                                                                                                                                                      |
| Attribut       | `[Attributname]`,<br>`[name="wert"]` --> sucht Elemente, die genau "wert" sind,<br>`[name~="wert"]` --> sucht Elemente, die das Wort "wert" enhalten,<br>`[name$="wert"]` --> sucht Elemente, die mit "wert" enden,<br><code>[name\|="wert"]</code> --> sucht Elemente, die Wort "wert" mit `-` getrennt,<br>`[name^=wert]` --> beginnt mit Zeichenkette "wert",<br>`[name*=wert]` --> enthält die Zeichenkette |
| Pseudoklassen  | `:empty`, `:first-child`, `:last_child`, `:nth-child`,<br> `:link`, `:visited`, `:hover`, `:active`, `:focus`,<br>`:disabled`, `:enabled`, `:checked`,<br>`:valid`, `:invalid`, `:in-range`, `:out-of-range`                                                                                                                                                                                                    |
| Pseudoelemente | `::first-line`, `::first-letter`,<br>`::before`, `::after`,<br>`::backdrop`,<br>`::selection`, `::placeholder`                                                                                                                                                                                                                                                                                                  |
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
| Eigenschaft                                                              | Bedeutung                                                   |
| ------------------------------------------------------------------------ | ----------------------------------------------------------- |
|                                                                          |                                                             |
| `@import 'pfad'`                                                         | Auslagern von Formatierungsteilen                           |
| `@media(Bedingung)`                                                      | Media-Queries, Spezielle Eigenschaften je nach Bedingung    |
| `background-color`, `background-image`, `linear-gradient`                | Hintergrund                                                 |
| `border-radius`                                                          |                                                             |
| `border: <line-width> <line-style> <color>;`<br>`border: 3px solid red;` | Rahmen                                                      |
| `color`                                                                  | Schriftfarbe                                                |
| `content`                                                                | Inhalt abändern                                             |
| `cursor` --> default, pointer, text, help, none                          | Mauszeiger                                                  |
| `display`                                                                | Anzeigetyp: `block`, `inline-block`, `none`, `flex`, `grid` |
| `flex-direction` --> `row`, `column`                                     | horizontale o. vertikale Ausrichtung (`flex`)               |
| `flex-wrap` --> wrap, nowrap                                             | Umbruch                                                     |
| `font-weight` --> normal, bold, lighter, bolder, `<number>`              |                                                             |
| `gap`                                                                    | Spaltenabstände                                             |
| `grid-area`                                                              | Festlegung des Bereichs in dem ein Element angezeigt wird   |
| `grid-column: start / end`                                               | Zuweisung der Spalten                                       |
| `grid-row: start / end`                                                  | Zuweisung der Zeilen                                        |
| `grid-template-areas`                                                    | Bestimmung welche Zelle zu welchem Bereich gehört           |
| `grid-template-columns`                                                  | Festlegung von Spalten und deren Aufteilung                 |
| `height`, `width`                                                        | Höhe, Breite                                                |
| `list-style`                                                             | Aufzählungszeichen anpassen                                 |
| `margin-left`, `margin-right`                                            | zum Horizontalen Zentrieren beides auf `auto` (`block`)     |
| `margin`                                                                 | Außenabstand                                                |
| `padding`                                                                | Innenabstand                                                |
| `position` --> `relative`, `absolute`                                    | Position                                                    |
| `text-align`                                                             | horizontale Ausrichtung (für `inline`)                      |
| `text-decoration` --> underline, overline, none                          |                                                             |
| `top`, `left`                                                            | Position im Bezug zum Elternelement                         |
| `transition`, `animation`, `offset`                                      | Animation                                                   |
| `vertical-align`                                                         | vertikale Ausrichtung (`inline`)                            |

## CSS-Beispiele
- Box Model ![[Pasted image 20231120145427.png]]
- Grid festlegen
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr; /* Drei Spalten mit unterschiedlichen Breiten */
  grid-template-rows: auto; /* Zeilenhöhe wird automatisch bestimmt */
  grid-gap: 10px; /* Abstand zwischen den Zellen */
  grid-template-areas: 
    "header header header"
    "sidebar content content"
    "footer footer footer";
}
.header {
  grid-area: header;
}
.sidebar {
  grid-area: sidebar;
}
.content {
  grid-area: content;
}
.footer {
  grid-area: footer;
}
```
- Tabellen-Zeile beim Hovern anders formatieren
```css
#die-tabelle tbody tr:hover {
    background-color: lightsalmon;
    cursor: pointer;
    transition: background-color .5s linear;
}
```
- Links formatieren
```css
/*active = beim Klicken, visited = schonmal geklickt*/
a:active, a:visited  {
  text-decoration: none;
  color : black;
  font-weight: bold;
  cursor:context-menu;
}
```

# JavaScript
- 1995 Einführung durch Netscape
- ECMAScript = Industriestandard für JS
- vielseitige Programmiersprache
- Hinzufügen von Interaktivität zu Webseiten
	- clientseitige Skriptsprache (i.d.R.)
	- Interaktivität und Dynamik
	- Asynchrones und Event-getriebenes Programmieren
	- Client-Server-Kommunikation
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
## Funktionen
```js
function ggT(a, b){
    if(b == 0)
        return a;
    return ggT(b, a%b);
}
```
## Ausgabe
| Aufruf                                               | Funktion                        |
| ---------------------------------------------------- | ------------------------------- |
| `document.write(var)`                                | Auf dem DOM ausgeben            |
| `console.log(str)`                                   | Auf die Konsole schreiben       |
| `let hello = prompt("Hello World!", "defaultValue")` | Text-Eingabe über Extra-Fenster |
| `alert("AAAAALLLLLARRRMMM!!!!")`                     | Text-Ausgabe über Extra-Fenster |                                                     |                                 |

## Selektion von DOM-Elementen
| Aufruf                                             | Funktion                                                          |
| -------------------------------------------------- | ----------------------------------------------------------------- |
| `document.getElementByID('id')`                    | Element über `id`-Attribut selektieren                            |
| `document.getElementsByName('name')`               | Element über `name`-Attribut selektieren                          |
| `document.getElementsByTagName('name')`            | Element über `<tag>` selektieren                                  |
| `document.getElementsByClassName('name')`          | Element über `class`-Attribut selektieren                         |
| `document.querySelector('Selektor')`               | Element über CSS-like Selektoren auswählen (Erstes zu treffendes) |
| `document.querySelectorAll('.styled-input input')` | siehe oben (Auswahl aller zutreffenden) --> Array                 |
| `elem2 = elem.parentNode`                          | Eltern-Element des Elements                                       |
| `elem2 = elem.nextSibling`                         | Nächstes Geschwister-Element                                      |
| `elem2 = elem.previousSibling`                     | Vorheriges Geschwister-Element                                    |
| `childElem = elem.children[n]`                   | Auswahl des n-ten Kind-Elements, bei 0 startend                                                                |
## Manipulation des DOM
| Aufruf                                                                                    | Funktion                                                                               |
| ----------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `elem.appendChild(child)`                                                                 | Knoten an das Ende der Liste von Kindern eines Eltern-Knoten anfügen                   |
| `elem.insertBefore(newNode, referenceNode)`                                               | Knoten vor einen Referenz-Knoten als Kind eines spezifizierten Eltern-Knoten           |
| `elem.removeChild(child)`                                                                 | Das was passiert wenn Abtreibung                                                       |
| `elem.setAttribute("<attribute>", "<value>")`<br>`elem.setAttribute("display", "inline")` |                                                                                        | Setzen von Attributen
| `elem.removeAttribute("<attribute>")`<br>`elem.removeAttribute("disabled")`                                                     | Entfernen von Attributen eines Elements                                                |
| `document.createElement('h2')`                                                            | `<h1>`-Element erzeugen, kann dann mit `appendChild` / `insertBefore` verwendet werden |
| `document.write("<h1>Überschrift</h1>")`                                                  | Direkt auf den DOM schreiben                                                           |

## JavaScript-Beispiele
### Style ändern / JS im `<head>` einbinden
```js
function init() {
    let art1 = document.getElementById('artikel1');
    art1.style.color = "red";
    
	let fetterText = document.getElementsByTagName('b');
	for (let elem of fetterText) {
		elem.style.textDecoration = 'underline';
		elem.style.fontStyle = 'italic';
	}
}
document.addEventListener('DOMContentLoaded', init);
```
### Event-Listener
```js
for(let elem of meineInputs){
    scaleLable(elem, true);
    elem.addEventListener('focus', function(){
        scaleLable(this, false);
    });
    elem.addEventListener('blur', function(){
        scaleLable(this, true);
    });
    elem.addEventListener('input', calcBMI, true);
}
```
## Umwandeln von Datentypen
```js
let groesse = parseFloat(document.getElementById('groesse').value.replace(",", "."));
let masse = parseInt(document.getElementById('masse').value);
let bmi = masse / Math.pow(groesse, 2);
let bmiFixed = bmi.toFixed(2); // Wegkürzen von Nachkommastellen
```
# PHP
- PHP = PHP: Hyptertext Preprocessor
- Programmiersprache
- serverseitig Skriptsprache Webentwicklung
	- Erstellung dynamischer Webseiten
	- Entwicklung von Webanwendungen (modular erweiterbar, z.B. für Datenbanken)
	- API-Entwicklung
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
	// Assoziative Arrays
	$wochentage = array("so" => "Sonntag",
                        "mo" => "Montag",
                        "di" => "Dienstag",
                        "mi" => "Mittwoch",
                        "do" => "Donnerstag",
                        "fr" => "Freitag",
                        "sa" => "Samstag");
	$wochentage["an"] = "Andrétag";
	var_dump($cars);  
?>
```
- Umwandlungen
```php
// Str --> Array | "," = Trennzeichen
$namen = "klora, jochen, ludwig, magda";
$namenAlsArray = explode(", ", $namen);
// Array --> Str | <br> = Trennzeichen
$wochentageAlsString = implode("<br>", $wochentage);
```
- Boolesche Operatoren
```php
if(in_array("Andretag", $wochentage))
    echo "Es gibt den Andretag!";
else 
	echo "Es gibt leider keinen Andretag";

if(array_key_exists("mo", $wochentage))
    echo "<p style='color:green;'>".$wochentage["mo"]."</p>";
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
