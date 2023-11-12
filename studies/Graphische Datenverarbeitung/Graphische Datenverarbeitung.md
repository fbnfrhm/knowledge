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
	- DCC (Digital Content Creation) = siehe 3Ds Max:
		- OBJ = Open Source : Wavefront Technologies
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
		- Berechnung der Lichtverhältnisse aus einem Bild
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

## Teil 6
### Drucktechnik
- Probleme und Lösungsansätze
	- Farbquantisierung (-> Farbtiefe)
		- Anzahl der Farben je Kanal in Bit
	- Rasterkonversion
		- ![[Pasted image 20231111141002.png]]
	- Halbtöne (Größe), Dithering (Anzahl), Fehlerdiffusion
		- ![[Pasted image 20231111141059.png]]
		- Dithering
			- ![[Pasted image 20231111141159.png]]
			- ![[Pasted image 20231111141315.png]]
- Tintenstrahldrucker:
	- Drucken von unterschiedlichen Punktgrößen
	- mehrschichtiges Drucken zum Erzeugen unterschiedlicher Farben
	- Mehrpunkt-Druck zum Erzeugen unterschiedlicher Farben
- Clipping:
	- Nicht-Sichtbares wird nicht berechnet
	- Reflexionen dürfen nicht Clipping
- Aliasing / Anti-Aliasing 
	- ![[Pasted image 20231111142350.png]]
	- Anti-Aliasing:
		- Glätten der Treppenstufen (siehe links) durch Farbübergänge
			- Folge: Unschärfe
- Grafikpipeline
	- 2D-Grafikpipeline
		- ![[Pasted image 20231111142621.png]]
		1. **Objektdefinition**: Ursprung der Grafikelemente; Definition von Formen und Linien als mathematische Gleichungen oder Datenstrukturen.
		2. **Modellierungstransformationen**: Platzieren und Skalieren der Objekte im Raum; Anwendung von Transformationen wie Rotation, Skalierung und Translation.
		3. **Ansichtstransformationen**: Anpassung der Szene an eine spezifische Ansicht oder Perspektive; Einstellung von Kamera-Position und Blickwinkel.
			1. **Fenster- und Viewport-Einstellungen**: Bestimmung des sichtbaren Ausschnitts der Szene (Fenster) und dessen Abbildung auf den Ausgabebereich (Viewport).
		4. **Schriftgröße und Farbattribute**: Definition von Texteigenschaften und Farbinformationen für die Objekte.
		5. **Scan-Conversion (Rasterkonversion)**: Umwandlung der Vektorobjekte in Pixel auf dem Rasterdisplay; endgültige Darstellung der Grafikelemente auf dem Bildschirm.
	- 3D-Grafikpipeline
		- ![[Pasted image 20231111142658.png]]
		Die Einzelschritte der 3D-Grafikpipeline in Ihrer Grafik können wie folgt zusammengefasst werden:
		1. **Objektdefinition**:
		   - Festlegung von Objekten in der Szene mittels Koordinaten und Primitiven (z.B. Punkte, Linien, Polygone).
		2. **Modellierungstransformationen**:
		   - Anwendung von Transformationen (Rotation, Skalierung, Translation) auf Objekte, um ihre Position, Größe und Orientierung im 3D-Raum zu ändern.
		3. **Ansichtstransformationen**:
		   - Einstellung der Kamera-Perspektive; Umwandlung der Szene aus der Modellansicht in die Kameraansicht.
		4. **Projektion**:
		   - Umrechnung der 3D-Szene in eine 2D-Projektion (perspektivisch oder orthographisch), basierend auf den Ansichtsparametern.
		5. **2D-Ansichtstransformation**:
		   - Anpassung der projizierten 2D-Szene an die spezifischen Koordinaten des Ausgabegeräts (z.B. Bildschirm).
		6. **Scan-Conversion**:
		   - Umsetzung der 2D-Vektorgrafik in eine Rastergrafik, wobei jeder Vektor in eine Menge von Pixeln umgewandelt wird.
		7. **Anzeige (Bildspeicher)**:
		   - Übertragung der pixelbasierten Grafikdaten in den Bildspeicher, von wo aus sie auf dem Ausgabegerät dargestellt werden.
- Illuminationsverfahren:
	- lokale Illumination: Nur von der Lichtquelle ausgehend, ohne Spiegelung, Erstellen der Schatten und Helligkeitspunkte
		- **Flat Shading (Flat)**
			- Einheitliche Farbe pro Polygon.
			- Berechnet Beleuchtung für einen repräsentativen Punkt (oft der Schwerpunkt) eines Polygons.
			- Harte Kanten zwischen Polygonen, keine Farbübergänge.
		- **Gouraud Shading (Gouraud)**
			- Beleuchtung an den Vertices (Ecken) der Polygone berechnet.
			- Farbübergänge zwischen Vertices durch Interpolation entlang der Kanten und über die Fläche des Polygons.
			- Weichere Übergänge als bei Flat Shading, aber kann Mach-Bänder-Effekte erzeugen.
		- **Phong Shading (Phong)**
			- Interpolation der Normalenvektoren über die Fläche des Polygons.
			- Beleuchtung wird an jedem Pixel berechnet, was zu einer sehr glatten und realistischen Darstellung von Highlights führt.
			- Rechenintensiver als Flat oder Gouraud, aber liefert die besten Ergebnisse für glänzende Oberflächen.
	- globale Illumination: Objekte können Licht reflektieren und selber als Lichtquelle fungieren (durch reflektiertes oder ausgestrahltes Licht)
		- Raytracing
			- Nachverfolgung der Wege von Lichtstrahlen
			- Berechnung rechen- und damit zeitaufwändig
			- ![[Pasted image 20231111153159.png]]
		- Radiosity
			-  Radiosity ist ein Verfahren, das berechnet, wie Licht in einem Raum verteilt wird, wobei es besonders gut diffuse Reflexionen zwischen Flächen simuliert
			- Berechnung der Lichtenergie (in Form von Aufnahme & Aufgabe) einer Fläche
			- ![[Pasted image 20231111153209.png]]
		- Kombination aus verschiedenen Verfahren
- Renderer
	- Scanline
	- Arnold (Autodesk)
	- Octane Render
	- Radeon ProRender
	- Workbench-Engine
	- Cycles
	- Eevee
	- RenderMan Studio
- Textur-Mapping
	- ![[Texture_mapping_demonstration_animation.gif]]
	- siehe Minecraft-Skin
- Animation
	- **Kinematische Ketten**: Sequenz von verbundenen Gliedern (wie Knochen in einem Skelett), deren Bewegungen relativ zueinander stehen.
	- **Direkte Kinematik**: Berechnet die Positionen der Glieder einer kinematischen Kette ausgehend von der Wurzel bis zu den Endeffektoren, basierend auf gegebenen Gelenkwinkeln.
	- **Inverse Kinematik (IK)**: Ermittelt die notwendigen Gelenkwinkel einer kinematischen Kette, um einen Endeffektor (z.B. eine Hand oder einen Fuß) an eine vorgegebene Position zu bringen.
	- **Stop-Motion**: Animationsform, bei der reale Objekte physisch bewegt und bildweise fotografiert werden, um Bewegung zu simulieren.
	- **Keyframe**: Einzelbild in einer Animation, das einen wichtigen Punkt oder eine signifikante Position eines animierten Objekts markiert.
	- **Bewegungspfade**: Vorgegebene Wege im Raum, entlang derer sich animierte Objekte oder Kameraeinstellungen bewegen.
	- **Motion Tracking**: Technik, um die Bewegung realer Objekte zu erfassen und diese Informationen in eine Animation zu integrieren.
	- **Motion Capture**: Erfassung von menschlichen Bewegungen durch Sensoren, um sie auf digitale Charaktere zu übertragen.
	- **Bones**: Strukturen in einem 3D-Animationsmodell, die den Gliedern in einem Skelett entsprechen und zur Definition von Bewegungen und Transformationen innerhalb des Modells verwendet werden.

## Ergänzungen aus der Themenübersicht
- **Objektraum**:
	- Bezieht sich auf die Koordinaten und Geometrie eines Objekts, wie sie unabhängig vom Betrachter definiert sind.
	- Die Modellierung und Transformationen der Objekte finden hier statt, bevor sie auf die Ansicht projiziert werden.
	- Arbeitet mit 3D-Koordinaten, die das Objekt in seiner natürlichen Größe und Form beschreiben.
- **Bildraum**:
	- Umfasst die projizierten Koordinaten eines Objekts auf die 2D-Bildebene, wie sie von einem Betrachter gesehen werden.
	- Hier finden Rendering-Verfahren statt, einschließlich Scan-Konversion und Rasterung von Bildern.
	- Arbeitet mit 2D-Koordinaten, die bestimmen, wo und wie ein Objekt auf dem Bildschirm oder anderen Medien angezeigt wird.
- Wellenlängen
	- ![[Pasted image 20231112112701.png]]
	- ![[Pasted image 20231112112724.png]]
- **Z-Abstand**: Messung der Entfernung eines Objektpunktes von der Kamera entlang der Z-Achse in einem 3D-Raum.
- **Tiefeninformation**: Wichtig für die korrekte Darstellung der räumlichen Anordnung und der Überlappung von Objekten in einer 3D-Szene.
- **Z-Puffering**: Technik, bei der für jedes Pixel der Z-Abstand gespeichert wird, um zu bestimmen, welches Objekt im Vordergrund angezeigt wird.

- Polygonzug
	- ![[Pasted image 20231112114239.png]]

- Mach-Band-Effekt
	- ![[taeuschung1.jpg]]
	- ![[Pasted image 20231112115134.png]]
	- 
### Umwandlung CMY -> CMYK
- gewählten Key (K) von dem Farbwerten (CMY) abziehen

### Umwandlung RGB -> CMYK
The R,G,B values are divided by 255 to change the range from 0..255 to 0..1:
_R_' = _R_/255
_G_' = _G_/255
_B_' = B/255

The black key (K) color is calculated from the red (R'), green (G') and blue (B') colors:
_K_ = 1-max(_R_', _G_', _B_')

The cyan color (C) is calculated from the red (R') and black (K) colors:
_C_ = (1-_R_'-_K_) / (1-_K_)

The magenta color (M) is calculated from the green (G') and black (K) colors:
_M_ = (1-_G_'-_K_) / (1-_K_)

The yellow color (Y) is calculated from the blue (B') and black (K) colors:
_Y_ = (1-_B_'-_K_) / (1-_K_)

