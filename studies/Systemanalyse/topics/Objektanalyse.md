## Objekt-Orientierung
- Objekte ... Abbildung der realten Welt auf Informatik-Denkweise
- Klasse ... Schablone, Bauplan
- Objekt ... tatsächliche Instanz

### Die 3 Säulen der Objekt-Orientierung
- **Vererbung**:
	- abgeleitete Klasse besitzt die Methoden und Attribute der Basisklasse
	- kann noch zusätzliche Methoden und Attribute enthalten
- **Datenkapselung**:
	- Verbergen von Implementierungsdetails
	- kein direkter Zugriff auf die interne Datenstruktur
	- Zugriff nur über definierte Schnittstellen
- **Polymorphie:** 
	- Fähigkeit eines Bezeichners, abhängig von seiner Verwendung unterschiedliche Datentypen anzunehmen.
	- Verschiedene Objekte können auf die gleiche Nachricht unterschiedlich reagieren.

## UML (Unified Modelling Language)
- Sprache und Notation für
	- Spezifikation -(+/-)-> <span style="color: grey">Sprachenabhängig</span> (nicht eindeutig, Begeleit-Text wird notwendig) 
	- Konstruktion -(-)-> <span style="color: red">nicht eindeutig, Begeleit-Text wird notwendig</span>
	- Visualisierung -(+)-> wenn (automatisch) generiert => OK
	- Dokumentation -(+)-> wenn (automatisch) generiert => OK  

![[media/pi/modules/Systemanalyse/objektana/UML_Diagrammarten.drawio.svg]]

### Klassendiagramm
- mehrere Klassen Können "sprachenunabhängig" dargestellt werden
- statische Informationen
- Beziehungen zu anderen Klassen  
![[media/pi/modules/Systemanalyse/objektana/Klassendiagramm.drawio.svg]]
- vor jedem Attribut/Methode wird
	- \+ ... public
	- \- ... private
	- \# ... protected
- geschrieben

- statische Methoden/Attribute werden einfach unterstrichen
- Kommentare: gestrichelte Verbindung  

#### Beispiel - Klassendiagramm
![[media/pi/modules/Systemanalyse/objektana/Klassendia_Hund.png]]

### Klassendiagramm mit Assoziation
- Assoziation = Beziehung zwischen Klassen  
![[media/pi/modules/Systemanalyse/objektana/KD_Mensch_Hund.svg]]

- Kardinalitäten:
	- \* beliebig viele
	- a .. b mindestens a höchstens b viele
	- a .. genau a viele

![[media/pi/modules/Systemanalyse/objektana/UML-Beziehungen.drawio.svg]]

#### Beispiel - Klassendiagramm mit Assoziation
![[media/pi/modules/Systemanalyse/objektana/KD_Mensch_Hund_2.svg]]
- ein Mensch hat 2 Hunde, die unabhängig von ihm leben können

### Klassendiagramm mit Vererbung
- unausgemalter Pfeil (zum Vater hin) (`S isA V`)  

![[media/pi/modules/Systemanalyse/objektana/KD_Vater_Sohn_Tochter.svg]]

#### Beispiel - Klassendiagramm mit Vererbung
![[media/pi/modules/Systemanalyse/objektana/KD_geom_Figuren.svg]]

### Zustandsdiagramme
- Verhaltensdiagrammen zugeordnet
- endliche Zustandsautomaten  

![[media/pi/modules/Systemanalyse/objektana/UML-Zustandsdia_Elem.drawio.svg]]

#### Beispiel - Zustandsdiagramm
![[media/pi/modules/Systemanalyse/objektana/ZD_Beispiel.svg]]

### Aktivitätsdiagramm mit Aktivitätsbereichen
![[media/pi/modules/Systemanalyse/objektana/AD_Beispiel.svg]]
