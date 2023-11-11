# CAD
## Teil 1
- Digitaler Zwilling / Digital Twin
	- virtuelle Kopie des realen Objekts
	- Datenaustausch virtuelle Kopie <-> reales Objekt
	- Datenverarbeitung / Analyse anhand der virtuellen Kopie
		- Vorhersagen treffen basierend auf den Daten
- Product Lifecycle Management
	- ![[Pasted image 20231106143636.png]]
- virtuelles Produkt (= Pretotyp, Vorgänger des Digitalen Zwillings)
	- für die Planung, Entwicklung und Konstruktion
- Metaverse
	- VR-Universum
	- Interaktion durch VR & AR
	- allgegenwärtiges räumliches Internet
	- personalisierte digitale Erfahrung
	- Verschmelzen von physischer & virtueller Welt
- Ablauf Produktentwicklung:
	- ![[Pasted image 20231106150508.png]]
	- 3D-Konstruktion:
		- Entwurf des Produkts in 3D
		- Nutzung von CAD-Software
		- Erstellung von dreidimensionalen Modellen
	- NC-Simulation (Numerical Control Simulation)
		- Digitale Simulation der Bearbeitungswege
		- Verwendung in der Vorbereitung für CNC-Maschinen
		- Erkennung und Korrektur von Fehlern im Vorfeld
	- FEM-Berechnung
		- Anwendung der Finite-Elemente-Methode
		- Analyse der Produktreaktionen auf physikalische Einwirkungen
		- Identifikation von Schwachstellen im Design
	- Baugruppengenerierung
		- Zusammenstellung von Einzelteilen zu Baugruppen
		- Überprüfung der Passgenauigkeit und Funktionalität
	- Zyklischer Prozess
		- Iterative Vorgehensweise
		- Kontinuierliche Verfeinerung des Produkts
		- Rückkopplung zwischen den Phasen zur Optimierung
- NC-Datenaustausch
	- ![[Pasted image 20231106152153.png]]
	- Konstruktion:
		- Erstellen des Modells --> bspw. mit CAD
		- Ableitung einer technischen Zeichnung
	- Arbeitsplanung:
		- Festlegung der Arbeitsschritte (+ Werkzeugauswahl)
		- Einteilung der Technischen Zeichnung
	- NC-Programmierung
		- Umwandlung des Modells in Maschinenbefehle (bspw. für CNC-Maschine)
- ![[Pasted image 20231106153203.png]]

## Teil 2
- ![[Pasted image 20231106154018.png]]
- Aufbau von CAD- und DCC-Software
	- ![[Pasted image 20231106154145.png]]
- Grafische Schnittstellen (API)
	- GKS = Grafisches Kernsystem
		- Festlegung der Basisfunktionen und Weiterverarbeitung computergenerierter Bilder
		- Ausgabe 2D Vektor- und Rasterbilder
		- Bildeingabe & -bearbeitung durch Festlegen von Funktionen für die graphische Eingabe und Bildschirmstrukturierung
		- einheitliche Schnittstelle zwischen den Anwenderprogrammen und einem Grafiksystem
		- Alle Funktionen sind anwendungs- und geräteneutral definiert
		- Behandlung der grafischen Ein- und Ausgabeinheiten als virtuelle grafische Arbeitsplätze
	- PHIGS / PHIGS+ = Programmer’s Hierarchical Interactive Graphics System
	- Direct3D/DirectX bzw. DirectX Graphics
	- OpenGL = Open Graphics Library
	- Vulkan = (Khronos Group)
	- Metal (Apple)
		- Bsp.: Mac Pro Workstation Powered by AMD Radeon™ Graphics (6/2019)
- Programmierschnittstellen
	- ![[Pasted image 20231106160057.png]]
- Geometrische Schnittstellen
	- ![[Pasted image 20231106160225.png]]
	- CAD:
		- STEP = Standard for the Exchange of Product Model Data
			- keine reine geometrische Schnittstelle
			- Produkt als Ganzes und sein gesamter Lebenszyklus
			- Integriertes Produktmodell
			- Produktmodell besteht aus Partialmodellen
				- Darstellung sämtlicher Merkmale des Produkts über seinen Lebenszyklus
			- ![[Pasted image 20231106161222.png]]
		- JT = Jupiter Tesselation
			- gut geeignet für die Prozesse nach CAD
			- CAD-Informationen gehen verloren
			- enthält alle notwendigen Informationen aus dem CAD
			- schnelles Laden / sehr performant
			- optional exakte Geometrie
			- ![[Pasted image 20231106162236.png]]
		- IGES -> VDA-IS = Initial Graphics Exchange Specification
			- Grundelemente
				- ![[Pasted image 20231106160929.png]]
		- VDA-FS = Verband der Automobilindustrie-Flächenschnittstelle
		- STL = Standard Triangle Language / Standard Tessellation Language
	- DCC (Digital Content Creation):
		- OBJ = Oben Source : Wavefront Technologies
		- gITF = Graphics Language Transmission Format
			- Komprimierung
			- JSON
		- USD (OpenUSD) = Universal Scene Description
- Kernelmodellierer (Solid Modeling Kernel)
	- grundlegendes Geometriemodell für CAD-Systeme
	- Parasolid (Dateiendung: `*.x_t`, `*.x_b`)
	- ACIS (`*.sat`)

## Teil 3
- Grafische Primitive: 2D-Elemente
	- Beispiele:
		- Punkt, Linie, Polygon (Polylinie), Kreis, Rechteck, Text, Spline, Bézier
- Grafische Primitive: 3D-Elemente
	- Beispiel:
		- Quader, Kugel, Zylinder, Kegel, ...
		- Bézier-Fläche / NURBS (Non-Uniform Rational B-Spline and Surfaces)
		- Metabälle / Blob-Netz
		- Subdivision Surfaces Modeling / SubD NURBS
- Tesselierung:
> Tesselierung ist der Prozess der Unterteilung einer geometrischen Form in kleinere, oft dreieckige Flächen, um deren Darstellung und Berechnung in der Computergrafik zu vereinfachen.
- Interpolation:
> Interpolation ist das Finden von Zwischenwerten zwischen zwei bekannten Werten in einer Datenreihe.
- Transformationsfunktionen:
	- Rundung, Fase, Bohrung, Nut, Ringnut
	- Welle, Rippe, Flansch
- Volumen --> Flächen --> Kanten --> Punkte

## Teil 4
- Auge
	- Nachtsehen: Stäbchen für Helligkeit, nicht farbsehfähig
	- Tagsehen: Zäpfchen für Farbsehen
- CIE-Farbwertdiagramm
	- ![[Pasted image 20231108140330.png]]
	- Dreieck umfasst alle wahrnehmbaren Farben unter Vernachlässigung der Leuchtdichte
	- Gamut = Farbumfang der darstellbaren Farben eines Farbraumes (Range of realisable colours)
		- ![[Pasted image 20231108141731.png]]
- Wahrnehmungsbegriffe
	- Leuchtdichte = Helligkeit (Fläche im sichtbaren Bereich, Integral)
	- Farbton = dominante Wellenlänge
	- Sättigung = Erregungsreinheit, Sättigung in der Farblehre bezieht sich auf die Intensität oder Reinheit einer Farbe.
	- $\text{Sättigung} = \frac{\text{reine Farbe}}{\text{reine Farbe} + \text{weiß}}$
- Farbmodelle, Farbraum
	- RGB
		- Red, Green, Blue
		- ![[Pasted image 20231108143551.png]]
	- CMY(K)
		- Cyan, Magenta, Yellow, Key = Schwarz
	- HSV
		- Hue, Saturation, Value
		- ![[Pasted image 20231108143957.png]]
	- HLS
		- ![[Pasted image 20231108145312.png]]
		- Hue, Lightness, Saturation
		- ![[Pasted image 20231108144100.png]]
	- CIE
	- YIQ
- Gamma, Gammakorrektur
	- Gamma = Intensität des Lichts am Monitor
	- Gammakorrektur = Kompensation für die Nichtlinearitäten
- Umwandlung RGB in Graustufen:
  $Y=0.299R+0.587G+0.114B$
  - komplementär Farben berechnen verlustfrei möglich
- Lichtquellen
	- ![[Pasted image 20231108151821.png]]
	- Richtungslicht, Punktlicht, Spotlicht
		- ![[Pasted image 20231108152116.png]]
	- Sonnenlicht- und Tageslicht
		- ![[Pasted image 20231108152716.png]]
	- Skylight
		- ![[Pasted image 20231108152850.png]]
		- Das Licht kommt aus unterschiedlichen Richtungen
	- Umgebungslicht
	- Image Based Lighting (IBL) (meist im Zusammenhang mit HDR-Image)
	- Photometrische Lichtquellen (incl. IES-Profil für die Abstrahlcharakteristik)
- Reflexion:
	- ideal spiegelnde Reflexion (z.B. Spiegel)
	- gerichtet diffuse Reflexion (z.B. poliertes Metall)
	- ideal diffuse Reflexion (z.B. raues Metall)
	- Totalreflexion ==> Licht wird 1:1 zurückgeworfen
- Beleuchtungsmodelle
	- Phong-Beleuchtungsmodell
		- (glänzend, matte Oberfläche)

## Teil 5
- BMP, GIF, JPEG, TIFF, PNG, OpenEXR, DDS, HEIF, WebP, HDRI, RAW
- ![[Pasted image 20231108160539.png]]
- Bildkomprimierung
	- ![[Pasted image 20231108161520.png]]
		- DCT = Discrete Cosine Transform = diskrete Kosinustransformation
# Projektmanagement
## Zusammenfassung 1
### Sie können den Unterschied zwischen Projekt und Projektmanagement erklären! 
| Projekt | Projektmanagement |
| :---- | :---- |
| Gegenstand einer Handlung (Ziel/Aufgabenstellung) | Umsetzung des Projektes (Projektauftrag) |
| begrenzte Ressourcen | Organisation |
| hoch Komplex | Ablauf |
|Zeitrahmen | Abrechnung |
| Risiko | Dokumentation |
### Sie kennen die sieben Merkmale, die ein Projekt kennzeichnen! 
- Finanzieller Rahmen
- Personeller Rahmen
- begrenzte materielle Verfügbarkeit
- Erst- oder Einmaligkeit vergebenes Ziel
- Begrenzte Dauer 
- Hohe Komplexität
- Risiko der Unerreichbarkeit 
### Sie können die vier Grundsätze der Projektplanung erklären!
- Einheitliche Planungsmethoden
	- zur Vergleichbarkeit
	- zum Benchmark
	- Synergien nutzen
	- Transparenz
- Einheitliche Planungsstandards
	- Verständnis bei allen Beteiligten
	- Abrechenbarkeit durch Kennzahlensysteme
	- Transparenz
- Nutzung von geeigneter Projektsoftware
	- Sparsamkeitsprinzip
	- Nutzung von Bekanntem
	- Optimierung des zeitlichen Aufwandes
	- Nutzen von vorhandenen Accounts
- Nutzung von Projekterfahrung
	- Verbesserung des Verständnisses
	- Risikominimierung
	- Motivation fördern
	- Wissensmanagement
#### Planungsmethoden
- Workflow
- Ganttdiagramm
- Flussdiagramm
- Netz-Plan-Technik (Vorgangsknoten / Vorgangspfeil)

#### Vorgangsknoten-Netzplan
![[Pasted image 20231110124647.png]]

## Zusammenfassung 2
### Sie sind in der Lage die Arten der Projekte in ihren Themengebieten zu trennen und darzustellen!
- ausrichtungsbezogen:
    - revolutionär: neue Idee; gewollte Schritte, bewusst angeregt (z.B. Glühbirne)
    - evolutionär: kleine ungewollte Schritte → Weiterentwicklung einer Idee (Entwicklung) oder Verbesserung/Optimierung einer Idee (Rationalisierung)
        - z.B.: Sensomotorik beim Menschen
    - expansiv: Vergrößern/Ausweiten einer Idee (Objekte)
        - z.B.: zusätzliche Produktionsanlagen bauen, neue Märkte erschließen
    - Forschung: z.B. Trial and Error
    - Entwicklung: z.B. Rennrad als Weiterentwicklung des "normalen" Fahrrads
- ausstattungsbezogen:
    - personell: eine/mehrere Personen
    - Vollzeit: begrenzte hauptamtliche Tätigkeit
    - Teilzeit: parallel zur derzeitigen Tätigkeit
- trägerbezogen:
    - eigene Projekte: im eigenen Unternehmen
    - fremde Projekte: für ein anders Unternehmen bzw. durch ein anderes Unternehmen
    - Mischprojekte: eigene und fremde Kräfte wirken gemeinsam
- funktionsbezogen:
    - Materialwirtschaft: Supply Chain Management (bspw.: Schreiner muss Holz beschaffen)
    - Fertigung: ein Projekt zur Optimierung der Produktion (bspw. energiesparenderer Prozess)
    - Marketing (Preis-, Verteilungs- Produkt-, Kommunikationspolitik)
    - Verwaltung: Umstellung von Fax auf ein Vorgangsbearbeitungssystem (Echtzeitsystem)
    - Kombination

## Zusammenfassung 3
### Sie kennen die Zeitabschnitte/Planungszeiträume von Projekten! 
![[Pasted image 20231110125930.png]]
### Sie kennen die zwei Abschnitte der Projektumsetzung! 
| Projektfindung/-Vorbereitung | Projektrealisierung |
| :--------------------------- | :-------------------------|
|Zielfindung/-Bildung<br>Benchmark, Trends, ... | Start --> Kick off<br> Bekanntgabe des Projektes (Info) |
| Problemanalyse --> Ishikawa, FMEA, ...<br>Risikominimierung | Definitinosphase<br>Ziel und Aufgabe (SMART, Operationialisierung (festlegen: Muss-, Soll-, Kann-Ziele)) |
| Finden von Alternativen (Plan B)<br>Kreativtechniken (Brainstorming):<br>Mind-Mapping, Brain Writing, Bionic (von der Natur inspirieren lassen), Risikominimierung, Nutzwerktanalyse | Planungsphase<br>Netzplantechnik (Pakete) |
| Prognose<br>Extrapolation, Szenario-Modell | Umsetzungsphase<br>Realisierung |
| Bewertung<br>Nutzwertanalyse | Bewertung<br>Kennzahlensystem, BSC |
- Projektrealisierung --> Managementkreislauf
### Sie können den PDCA als Führungsmethodik am konkreten Beispiel anwenden! 
- Plan
	- Aufgaben, Zielsetzung (Info)
	- Analyse
	- Entscheidungen treffen (begrenzt) --> Test
- Do
	- testen, ausprobieren (Umsetzung in Teilen)
	- Daten erfassen
- Check
	- Analyse der Daten aus dem **Do**
	- Standards festlegen
	- **Loop zum Do**
- Act
	- Standards umsetzen
	- Gesamt realisieren
	- Daten -> für weitere Aktivitäten
### Sie kennen die vier Abschnitte des Gesamtprozesses der Projektumsetzung! 
1. Prozessvorbereitung
	- Problemermittlung
	- Problemanalyse
	- Alternativen
	- Erfolgseinschätzungen
	- Entscheidung
2. Projektplanung
	- Aufgabenplanung
	- Personalplanung
	- Terminplanung
	- Ergänzungen
	- Planungsergebnisse
3. Projektgestaltung
	- Projektauslösung
	- Projektarbeiten
	- Projektsteuerung
4. Projekteinführung
	- Lösungseinführung
	- Abschlussarbeiten
### Sie können zwei Methoden zum Finden von Fehlern/Problemen erläutern!
- Ishikawa
	- ![[Pasted image 20231110144553.png]]
	- Umfeld = Milieu 
		- Problem identifizieren mit ISHIKAWA
		- Probleme definieren mit SMART
		- Problem lösen
		- 7 Elemente
		- Konkrete Ursachen anfragen
		- Ziel ==> SMART
			- S = Spezifisch = Sache
			- M = Messbar => Größenordnung
			- A = Akzepitert => Bedingung
			- R = Realisitsch => Bedingung
			- T = Terminiert
	- Vorteile:
		- Vereinfacht das Problem
		- ordnet mögliche Ursachen in Kategorien
		- Erarbeitung im Team ermöglich neue Perspektiven
	- Nachteile:
		- erfordert Disziplin und Vereinfachung, damit das Diagramm nutzbar bleibt
		- Vorgefertigte Kategorien (z.B. 5M) können kreative Problemlösungswege einschränken
		- Komplexe Zusammenhänge lassen sich im ISHIKAWA-Diagramm nicht darstellen
- FMEA = "Failure Mode and Effects Analysis" = "Fehlermöglichkeits- und Einflussanalyse"
	- Funktionen:
		1. Fehler erkennen
		2. Lösungen finden
		3. Dokumentation und Abrechnung
### Sie kennen mind. drei Kreativtechniken mit denen man Ideen entwickeln kann! 
- Brainstorming
- Brain Writing - 635 Methode
	- 6 Teilnehmer, je 3 Ideen, 5mal Weitergeben
- Mindmapping
- Morphologischer Kasten
### Sie können die Risiken bei der Umsetzung an einem Ampelsystem erläutern und die Bedeutung und den Inhalt der Nachhaltigkeit darstellen! 
![[Pasted image 20231110150252.png]]
#### Nachhaltigkeit
![[Pasted image 20231110150649.png]]
### Sie kennen die fünf notwendigen Anforderungen an den Projektleiter! 
#### GitHub
- fachliche Kompetenzen
    - Lösungsorientiert
    - Projektbezogen
- soziale Kompetenzen
    - Kommunikativ, Motivierend
    - Führungskompetenzen (Methoden der Führung)
- methodische Kompetenzen
    - Methoden des Projektmanagements
#### Folien
- Aufgabe
- Ziele
- Befugnisse
- Verantwortung
- Anforderungen
### Sie kennen die Entwicklung von Gruppen! 
1. Kennenlernen, Zusammenstellung → Forming
2. Rangordnung, Rollen festlegen → Storming
3. Qualität und Quantität oder Aufgabenerfüllung → Norming
4. Doing, Erfüllung, höchste Leistungsfähigkeit → Performing
5. Verabschiedung, Auflösung → Adjourning
### Sie kennen die Institutionen zur Unterstützung eines Projektes!
- Fachausschuss
	- Kontrollorgan zur fachlichen Beurteilung der erbrachten Leistung
	- quantitative und qualitative Beurteilung, vergleichbar mit einer Stabsstelle
	- Expertise
- Lenkungskollegium
	- Koordination und Unterstützung 
	- besonders für finanzielle und materielle Bedürfnisse des Projektteams
- Lenkungsausschuss
	- Schnittstelle zwischen FK
### Sie kennen die vier Organisationsformen der Struktur einer Projektgruppe! 
![[Pasted image 20231110152450.png]]
- reine Projektgruppe = eine Sparte der Spartenorganisation
	- findet in dem Bereich statt wo es umgesetzt werden muss
- Linien-Projektgruppe
	- findet in dem Bereich statt wo es umgesetzt werden muss
- Stabsliniensystem
	- Projekt = Stabstelle (Vollzeit)
	- Mitarbeiter arbeiten nebenamtlich an dem Projekt (Teilzeit)
- Matrix
	- Projektleiter direkt im Unternehmen angebunden
	- Projektleiter löst MA aus den Bereichen heraus
	- Vollzeitbesetzung der Mitglieder des Projektes
### Sie können den Einfluss verschiedener Faktoren auf die Entwicklung eines Projektes erklären! 
- Größe des Projektes
- Dauer des Projektes
- Komplexität des Projektes
- Zusammensetzung des Projektteams (Intern/Extern-Mix)
- Bedeutung für das Unternehmen

### Sie wissen in welchem Spannungsfeld sich ein Projekt befindet und können das am Beispiel darstellen!
![[Pasted image 20231110155058.png]]

## Zusammenfassung 3
### Sie kennen die fünf Planungsinhalte eines Projektes! 
- **Aufgaben**
    - Lösungs-Konzepte
    - Projekt-Struktur
    - Tailoring
    - Projekt-Prozess
- **Personal**
    - Quantitativ
    - Qualitativ
    - Einsatz
- **Termin**
    - Aufgaben
    - Verfahren (Prozess)
    - Vergleich
- **Ergänzende Planung**
    - MR
    - FR
    - Dokumentation
    - Qualität
- **Planungsergebnisse**
    - Projektplan
    - Projektantrag
    - Projektauftrag
    - Projektvergabe
    - Förderung
### Sie kennen die Inhalte der Bestimmung der HR!
- Qualität der MA
	- fachlich, methodisch, persönlich
- Quantität
	- Menge, Ort
- Einsatz
	- Zeitraum, Termin
### Sie können den Knotennetzplan berechnen und Optimierungen begründen! 

### Sie können ein Projekt an Hand der sechs Elemente eines Planungsergebnisses darstellen! 
- Projektplan
- Planungsbericht
- Projektantrag
- Projektauftrag
- Projektvergabe
- Fördermittelantrag
### Sie beherrschen die fünf Phasen des Findens eines Projektes! 
- Zielbildung: aktive oder reaktive Prozesse
- Problemanalyse: Ishikawa, FMEA, ...
- Alternativen: Kreativitätstechniken (Brainstorming, Mindmapping, ...)
- Prognose: Szenario-Analyse, Extrapolation
- Bewertung: Nutzwertanalyse, Kosten-/Nutzungsrechnungen, BSC
### Sie können an Hand der SWOT-Analyse Lösungsansätze für ein Projekt finden!
- Untersuchung der 
- Stärken, (Strengths)
- Chancen, (Opportunities) 
- Schwächen und (Weaknesses)
- Gefahren (Threats)
### Sie beherrschen die Nutzwertanalyse zur Bewertung von Lösungsmöglichkeiten! 
- Fragen mit Punkten bewerten → zusammenrechnen (WOW)
### Sie kennen die fünf Phasen des Ablaufs eines Projektes! 
![[Pasted image 20231110162724.png]]

### Sie können die Interessenlage der acht Beteiligten an einem Firmenprojekt erläutern!
- Unternehmensleitung
	- Arbeit erledigt --> Profit
- Eigentümer
	- Marktwert bleibt oder erhöht sich 
	- Rendite, Abschreibung, ROI (= Return of Investment)
- Staat / Gesellschaft
	- Steuern, Nachhaltigkeit
- Kunden
	- Produkt
- Fremdkapitalgeber
	- Raten der Kreditvergabe
- Konkurrenz
	- Benchmark
	- Ideen kopieren
- Lieferanten
	- stabiler Umsatz
	- gute Beziehung
- Arbeitnehmer
	- Geld, Spaß, Sicherheit
### Sie können eine Zielstellung nach ihren Bedingungen und Dimensionen darstellen und deren zwingenden Zusammenhang darstellen! 
![[Pasted image 20231110163544.png]]
- SMART
### Sie sind in der Lage innerhalb der Operationalisierung einzelne Ziele nach muss, soll und kann zu bestimmen! 
- Muss-Ziele --> Mindestanforderungen
- Soll-Ziele --> geplanter Stand
- Kann-Ziele --> mögliche / wünschenswerte Ergänzungen
- Beispiel: Autobau
	- Muss: Motor, Airbags
	- Soll: Tempomat
	- Kann: Ambientbeleuchtung
### Sie kennen die fünf grundsätzlichen Risiken eines Projektes und können deren Wertigkeit bestimmen! 
- Technisches Risiko - Neue Technik / Technologie
- Finanzielles Risiko - Kostenentwicklung
- Rechtliches Risiko - Gesetzgebung, Umweltstandards
- Personelles Risiko - Personalprobleme
- Sozialer Bereich - Personalprobleme
### Sie kennen Führungsarten, Führungsstile und drei Führungstechniken mit denen ein Projektleiter das Projekt führt kann und sind in der Lage diese zu beschreiben!
- **Führungsarten**
	- Motivation
	- Aufgaben
	- Ziele
- **Führungsstile**
	- autoritär
	- kooperativ
	- Laissez Faire
- **Führungstechniken**
	- Management by Objective (MbO) → Ziele → Vereinbarung → kooperativ
	- Management by Question (MbQ) → Fragen
	- Management by Delegation (MbD) → Aufgaben übergeben
	- Management by Results (MbR) → Ziele → Anordnung → autoritär
## SCRUM
## Kanban

## Zusammenfassung 4
### Sie kennen die vier Elemente des Projektcontrollings und können diese Inhaltlich darstellen! 
- Projektplanung
- Projektkontrolle
- Information / Dokumentation
- Projektsteuerung
### Sie sind in der Lage das Berichtswesen des Controllings mit eigenen drei Argumenten zu begründen!
- Nachweise (der rechtlichen Parameter)
- aktuellen Stand erfassen
- Wissensmanagement
- Abrechnung