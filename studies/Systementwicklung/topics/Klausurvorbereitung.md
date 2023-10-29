## Lernzielkontrolle 00
### Die 4 Säulen für Qualitätsverbesserung in der Entwicklung (z.B. Software) benennen:
| Kompetenz der Entwickler | Prozess | Muster / Wiederverwendung | Werkzeuge |
| :------ | :------ | :------ | :----- |
| Wissen und Erfahrung der Entwickler verbessert die Geschwindigkeit und Qualität der Entwickler. | Vereinheitlichung der Entwicklung um Fehler zu vermeiden und um die Schnelligkeit zu erhöhen. | Auf alte Erkenntnisse und alten Code zurückgreifen, um die Arbeit zu beschleunigen und eine gewisse Qualität zu wahren. | Unterstützung der Entwicklung durch Versionsverwaltung, Ticketsystem, und andere Dinge. |
| Systemanalyse | Systemanalyse | Systementwurf | Systementwurf | 

### Was wurde in Systemanalyse behandelt?
> Es wurden die verschieden Vorgehensmodelle, Analyseverfahren, sowie einige Hilfsmittel und Werkzeuge für den Entwicklungsprinzip besprochen.

### Was wurde in Systementwurf behandelt? 
> Es wurden Entwicklungskonzepte, allgemeine Entwurfsmuster und objektorientierte Entwurfsmuster vorgestellt, welche anhand von gewissen Metriken gemessen werden können.

## Lernzielkontrolle 01
### Hauptaufgabe des Systementwurfs
```mermaid
flowchart LR
Anforderungen --- A[Zerlegung<br>Strukturierung<br>Beziehungen zwischen Komponenten] 
A --> Architektur 
Architektur -.- B([Spezifikation der Systemkomponenten])
```

### Grundsatzentscheidungen
1. Oberflächen zum Benutzer (GUI, CLI , GUI+CLI, Toolbox, UX, …)
2. Reichweite (Sprache, Nutzungsintensität)
3. Datenhaltung
4. vorhandene Systemumgebungen nutzbar (?)
5. Hilfesystem
6. Ausbaustufen gewünscht?
7. Verteilung im Netz (Client-Server vs Web-Applikationen)
8. Kostenrahmen

### Ablauf des Entwurfsprozesses
- Grob-Entwurf:
	1. Architektur entwerfen
	2. Subsysteme entwerfen
	3. Schnittstellen festlegen
	- (bisher unabhängig von Implementierungssprache!)
- Fein-Entwurf:
	4. Komponenten
	5. Datenstrukturen
	6. Algorithmen

![[media/pi/modules/Systementwicklung/Entwurfprozess.drawio.svg]]

### Unterscheidung von Komponenten und Subsystemen
- Subsystem
	- in sich geschlossenes System
	- eigenständig funktionsfähig
	- definierte Schnittstellen
	- besteht wieder aus Komponenten  
![[media/pi/modules/Systementwicklung/Subsystem.drawio.svg]]
- Komponenten
	- Bausteine für Software-System
	- benutzt andere Komponenten
	- wird von anderen Komponenten benutzt
	- besteht aus Unterkomponenten

### Kriterien
1. Verständlichkeit + Präzision
2. Anpassbarkeit
	- Inhalt
	- Darstellung
3. Korrektheit + Vollständigkeit
4. Wiederverwendbarkeit
5. hohe Kohäsion (Maß für Zusammengehörigkeit)
6. schwache Kopplung
	- (z.B. große Klassen in kleinere Aufbrechen)

Was sind funktionale Anforderungen?
- schönes Aussehen
- Anfänger freundlich
- schnell
- usw.

### Prinzip der Software-Architektur-Sichten 
![[media/pi/modules/Systementwicklung/4+1_Sichten_Modell.drawio.svg]]

### Qualitätssicherungsprinzipien
1. Review
2. Tests --> Vergleich mit Zweitlösung
	- mittels Szenarien
		- direkte
		- indirekte: solche, die erst nach Modifikation umgesetzt sind

### Metriken für modulare Entwürfe
![[media/pi/modules/Systementwicklung/modulare_Entwuerfe.drawio.svg]]
#### FAN-IN Metrik
> Anzahl der Stellen, wo der Kontrollfluss in das Modul geht
> Anzahl globaler Variablen in Modul
- **FAN-IN ist HOCH** ==> Hinweis auf hohe KOHÄSION
- <span style="color:red">geeignetes Anwendungsgebiet?</span>
#### FAN-OUT Metrik
> Anzahl der Stellen, wo der Kontrollfluss aus dem Modul herausgeht
> Anzahl globaler Variablen, die das Modul ändert
- **FAN-OUT ist HOCH** ==> Hinweis auf hohe KOPPLUNG
- <span style="color:red">geeignetes Anwendungsgebiet?</span>

## Lernzielkontrolle 02
### [[Architekturmuster der strukturellen Sicht]]
### [[Architekturmuster der physikalischen Sicht]]
### [[Architekturmuster der Ablauf-Sicht]]
### [[Architekturmuster der logischen Sicht]]
### Mindestarchitekur
- 3-Schichten-Architektur  
 ![[media/pi/modules/Systementwicklung/3-Schichtenmodell.drawio(1).svg]]

### Vorteile von Mustern
- Zeitersparnis / generische Lösung für häufige Probleme
- größere Übersichtlichkeit bei Standard-Mustern
- Wiederverwendbarkeit
- Vereinheitlichung
- Unterstützung nicht funktionaler Anforderungen
- Dokumentation
- Kommunikation
- Dinge sichtbar machen

## Lernzielkontrolle 03
### Zweck einer Sammlung von Entwurfsmuster
> Man hat einen guten Überblick über die einzelnen Entwürfe und kann auf diese schnell zugreifen, wenn sie angewendet werden sollen. Das beschleunigt den Entwicklungsprozess.

### Vertreter der 3 großen Entwurfsmuster-Kategorien
- [[Architekturmuster der strukturellen Sicht]]
- [[Architekturmuster der physikalischen Sicht]]
- [[Architekturmuster der Ablauf-Sicht]]
- [[Architekturmuster der logischen Sicht]]

### Unterschied Interpreter-Entwurfsmuster und Interpreter-Architekturmuster (der strukturellen Sicht)
#### Architekturmuster (der strukturellen Sicht)
-  Interpreter-Muster
	- z.B. Python, (Java), PHP, bash, BAT
	- ist vergleichbar mit dem Factory-Muster
-  Muster:  
![[media/pi/modules/Systementwicklung/Interpreter.drawio.svg]]
- Vorteil: plattformunabhängig (brauche nur Interpreter)

#### Entwurfsmuster
definiert die Repräsentation einer Sprache (Grammatik) und ermöglicht die Sätze der Sprache zu interpretieren

Bsp: $(7+3)+(2 * 6)$  
![[media/pi/modules/Systementwicklung/Interpreter-Muster.drawio.svg]]

![[media/pi/modules/Systementwicklung/umgekehrte_polnische_Notation.drawio.svg]]
```c++
class TermAusdruck {
	return 5; // 5 hierbei als Beispiel
}

class NichtTermAusdruck {
	Ausdruck a;
	Ausdruck b;

	return interpretiere(
		a.interpretiere(+), 
		b.interpretiere(*)
	);
}
```

## Lernzielkontrolle 04
### Die 4 Säulen für Qualitätsverbesserung in der Entwicklung (z.B. Software) benennen:
| Kompetenz der Entwickler | Prozess | Muster / Wiederverwendung | Werkzeuge / Automatisierung |
| :------ | :------ | :------ | :----- |
| Wissen und Erfahrung der Entwickler verbessert die Geschwindigkeit und Qualität der Entwickler. | Vereinheitlichung der Entwicklung um Fehler zu vermeiden und um die Schnelligkeit zu erhöhen. | Auf alte Erkenntnisse und alten Code zurückgreifen, um die Arbeit zu beschleunigen und eine gewisse Qualität zu wahren. | Unterstützung der Entwicklung durch Versionsverwaltung, Ticketsystem, und andere Dinge. |
| Systemanalyse | Systemanalyse | Systementwurf | Systementwurf | 

### Maßnahme für eine Säule der Qualitätsverbesserung

### Maßnahmen für unterschiedliche Säulenpaare

### Unterschied zwischen der Prüfung auf Wohlgeformtheit und Validität (inhaltsbasierte XML)
```xml
<Property Bezeichnung="ID">
	<value type="string">
		G1715
	</value>
</Property>
```
- Wohlgeformtheit:
	- Alle Elemente werden auch geschlossen `<tag></tag>`
- Validität:
	- Überprüfung der Daten anhand eines XML-Schema
		- Stimmen die Datentypen, Namensräume, etc.

### Objekttypen einer JSON-Datei
- Objekt
- Array
- String, Real, bool, null

### Welches Dateiformat bei einer Datensammlung XY benutzen? Entwurfsmuster dafür erläutern.
- CSV für Daten in Tabellen-Form
- XML & JSON sind so gut wie gleich
- XML wenn Validität überprüft werden muss (XML-Schema)
	- wobei es auch (inoffizielle) JSON-Schemas gibt
#### Entwurfsmuster
## Interpreter-Muster
> definiert die Repräsentation einer Sprache (Grammatik) und ermöglicht die Sätze der Sprache zu interpretieren

Bsp: $(7+3)+(2 * 6)$  
![[media/pi/modules/Systementwicklung/Interpreter-Muster.drawio.svg]]

### Umgekehrte polnische Notation
++ 7 3 * 2 6  
--> ++ 7 3 * 12  
--> +10 12  
--> 22  

![[media/pi/modules/Systementwicklung/umgekehrte_polnische_Notation.drawio.svg]]
```c++
class TermAusdruck {
	return 5; // 5 hierbei als Beispiel
}

class NichtTermAusdruck {
	Ausdruck a;
	Ausdruck b;

	return interpretiere(
		a.interpretiere(+), 
		b.interpretiere(*)
	);
}
```
