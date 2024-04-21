# Einstieg
### Bayes-Klassifikator
- wahrscheinlichkeitsbasierte Klassifikation:
	- Ordne *x* der Klasse mit der höchsten Wahrscheinlichkeit zu

### Anwendungsbereiche
- E-Commerce / Retail:
	- Produktempfehlungen
- Finanzwirtschaft:
	- Analyse von Finanzdaten
- Industrie:
	- prädiktive Instandhaltung
- Transport/Mobilität:
	- selbstfahrende Fahrzeuge
- Gesundheitswesen:
	- Analyse med. Bilddaten

--> Data Mining, Data Science, Maschinelles Lernen, KI

### Daten & Wissen
- Was sind Daten?
	- einzelne Objekte
	- individuelle Merkmale
	- riesige Fallzahlen
	- verwirrende Vielfalt
	- preiswerte Beschaffung
- Was ist Wissen?
	- Klassen von Objekten
	- globale Muster
	- allgemeine Gesetze
	- einfache Prinzipien
	- schwer zu bekommen
- Daten --> Information --> Wissen --> Einsicht?

### Analyse-Arten
- deskriptive Analyse -> Was ist passiert?
	- Verständnis verbessern
- diagnostische Analyse -> Warum passiert das?
- prädiktive Analyse -> Was wird als nächstes passieren?
	- Vorhersagen verbessern
- präskriptive Analyse -> Wie können wir etwas erreichen?
	- Handlungen und Entscheidungen verbessern

### Künstliche Intelligenz, Maschinelles Lernen, Deep Learning
- Künstliche Intelligenz: *Techniken die Maschinen erlauben Probleme lösen die im Allgemeinen die Intelligenz von Menschen erfordern*
- Maschinelles Lernen: *Teilgebiert der Künstlichen Intelligenz, das sich mit Algorithmen zum Lernen von Mustern in Daten mittels statistischer Methoden beschäftigt*
- Deep Learning: *Teilgebiet des Maschinellen Lernens, das zum Erlernen von Mustern mehrschichtige neuronale Netzwerke nutzt*

### verallgemeinerndes Lernen aus endlich vielen Beispielen
- Deduktion: Schluss vom Allgemeinen aufs Einzelne
	- Als einziges logisch korrekt
- Induktion: Schluss vom Einzelnen aufs Allgemeine
- Abduktion: Schluss vom Ergebnis über eine Regel auf einen Fall

### Lern-Arten
- unüberwachtes Lernen
	- Algorithmen zur Aufdeckung von versteckten Mustern in Daten
- überwachtes Lernen
	- Algorithmen für Vorhersagen und Prognosen auf unbekannten Daten, Muster werden dabei auf bereits bekannten Daten erlernt
- verstärkendes Lernen
	- Algorithmen interagieren mit einer Umgebung und lernen anhand eines Belohnungssystems

### Anwendung von maschinellem Lernen
- Klassifikation
	- Klassen sind für eine kleine Anzahl an Lerndaten bekannt
	- Suche nach Funktion/Modell, die Klassen von bekannten Eingabedaten unterscheidet und die Klassenzugehörigkeit für unbekannte Eingabedaten vorhersagt
- Gruppierung
	- Objekte ohne bekannte Klassenzugehörigkeiten
	- Ähnlichkeitsfunktion/-modell für Objekte
	- Suche nach Gruppierung die Abstände der Objekte in einer Gruppe minimiert (Kohäsion) und Abstände zwischen den Gruppen maximiert (Separierung)
- Regression
	- numerische Ausgabedaten sind für eine kleine Anzahl an Lerndaten bekannt
	- Suche nach Funktion/Modell die/dass Beziehung zwischen bekannten Ein-/Ausgabedaten beschreibt und Ausgabedaten für unbekannte Eingabedaten vorhersagt
- OLAP
	- multidimensionale Objekte mit hierarchischen Merkmalen
	- Analyse von Zusammenhängen auf aggregierte Merkmalen entlang Dimensionshierarchien
	- Data Cube-Ansatz: Slicing, Dicing, Drill-down/up, Pivoting, etc.

# Daten und Datenaufbereitung I 
Datensatz
> Menge oder Folge von Objekten (Beispiele, Instanzen) mit ihren Merkmalen und Beziehungen

Merkmal
> Attribut (Eigenschaft, Variable) eines Objekts als Element eines Wertebereichs (Skala)

Beziehung
> Relation zwischen oder Ähnlichkeit von Objekten

## Skalentypen
| Typ                          | Art                  | Mittelwerte           | Operationen, Eigenschaften                                                                                  | Beispiele                                                                                                                                               |
| ---------------------------- | -------------------- | --------------------- | ----------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nominalskala<br>(nominal)    | diskret / kategorial | Modus                 | Gleichheit, Ungleichheit,<br>alle Werte gleichberechtigt                                                    | Booleans, Zeichensätze (A,G,T,C),<br>Farben (rot, grün)<br>Gruppen, Prädikate                                                                           |
| Ordinalskala<br>(ordinal)    | diskret / kategorial | Median                | Gleichheit, Ungleichheit, Vergleichbarkeit,<br>Rangordnung möglich                                          | Notenskala (sehr gut, gut, befriedigend),<br>unscharfe Prädikate (kalt, kühl, lau, warm, heiß),<br>eingefrorene Quantitäten (2-türig, 4-türig, 5-türig) |
| (Ordnungsrelation)           | diskret / kategorial |                       |                                                                                                             | -                                                                                                                                                       |
| (Abstandsfunktion)           | diskret / kategorial |                       |                                                                                                             | -                                                                                                                                                       |
| Intervallskala<br>(absolut)  | numerisch / kardinal | arithmetisches Mittel | Gleichheit, Ungleichheit, Vergleichbarkeit, Differenzbildung,<br>Unterschiede quantifizierbar               | Temperaturen (20°C, 451°F),<br>Zeitangaben<br>(1966, 469 v. Chr.)                                                                                       |
| Verhältnisskala<br>(relativ) | numerisch / kardinal | geometrisches Mittel  | Gleichheit, Ungleichheit, Vergleichbarkeit, Differenzbildung, Quotientenbildung,<br>Nullpunkt wohldefiniert | absolute Temperaturen (bspw. 273K),<br>Zeitdauer (10 Jahre, 45min)<br>Prozentangaben<br>Mengenangaben                                                   |
| proportional                 | numerisch / kardinal |                       |                                                                                                             |                                                                                                                                                         |
## CRISP-DM Vorgehensmodell
![[Pasted image 20240421105759.png]]

## Weiter bei Satz 7