## Lernzielkontrolle 01: Einleitung / Überblick
- [ ] Ich kann eine Liste mit mindestens 6 IT-Trends benennen und jeden Begriff kurz erläutern  

| Trend | Erläuterung |
| :----- | :-------- |
| Cloud Computing | dezentrale Verarbeitung von Daten |
| Mobile Computing | Mobile Software<br>mobile Kommunikation |
| KI / AI | Computer bekommen die Fähigkeit zu lernen und sich durch Experimente zu verbessern | 
| Blockchain | digitales Protokoll für Transfer + Aufbewahrung von digitalen Informationen<br>dezentrale Datenbank, die ganz oft dupliziert wurde
| Microservices | Architekturmuster der IT<br>Anwendungssoftware wird aus unabhängigen Prozessen komponiert<br>Notwendigkeit einer Sprachenunabhängigen Programmier-Schnittstelle<br>Dienste, die entkoppelt sind |
| AR / VR | AR: virtuelle Objekte in reale Welt projizieren<br>VR: reale Objekte in virtuelle Welt projizieren | 

- [ ] Ich kann den Unterschied zwischen Cloud-Computing und Edge-Computing erläutern  
	- Die Edge-Cloud ist "näher" an dem eigentlichen Netzwerk dran, man muss nicht, wie bei der normalen Cloud, den Umweg über das Internet gehen.

- [ ] Ich kann Anwendungsfälle für KI erläutern  

| Anwendungsfall | Erläuterung |
| :-------- | :----------- |
| Klassifikation | Erkennung von Eigenschaften in einem Bild (z.B. Ist Gruppenbild, Person ist glücklich, alt, usw.) |
| Objekt-Erkennung | Erkennung von Objekten, Gesichtern u.ä. |
| Text-Erkennung | Erkennung und Übersetzung von (handschriftlichen) Texten in digitale Formate (z.B. Word) |
| Bilderzeugung / -bearbeitung | Erstellen von Kunstwerken auf Basis eines künstlerischen Stils<br>Verschönern von Bildern (z.B. Beseitigung von Hautunreinheiten, siehe Snapchat, Instagram, usw)

- [ ] Ich kann die Grundprinzipien der IT-Sicherheit darstellen
	- Integrität (z.B. durch Prüfsummen)
	- Verfügbarkeit
	- Vertraulichkeit (z.B. durch Logins, Verschlüsselung, Einschränkung des physischen Zugangs)
	- Authentizität
	- Nicht-Abstreitbarkeit

## Lernzielkontrolle 02: REST-Schnittstellen
- [ ] Ich kann die Grundprinzipien von REST darstellen und Vorteile benennen.
	- Grundprinzipien:
		1.  Client-Server-Modell (UI ist von Datenhaltung getrennt)
		2.  Zustandslos
		3.  gleiche Anfragen dürfen **gecached** werden
		4.  Schnittstelle einheitlich
		5.  Schichten-System
		6.  Code nach Bedarf nachladbar
	- Vorteile:
		- flexibel
		- dynamisch skalierbar
		- Nutzung von vorhandenen Technologien (siehe HTTP)
- [ ] Ich kann eine Micro-Service-Architektur von einer Service-Orientierten-Architekturen unterscheiden:  
	- Service orientiert:  ![[SOA.drawio.svg.svg]]
		- bei Service-orientierter Architektur: ein geteiltes Interface
	- Micro-Service:   ![[MS_Beispiel_Architektur.drawio.svg]]
		- bei Micro-Service-Architektur: jeder Service kann eigenes Interface haben
- [ ] Ich kann ein Beispiel für eine Anwendung darstellen, die mittels einer Micro-Service-Architektur aufgebaut ist und mindestens eine REST-Schnittstelle dazu verbal beschreiben.
	- siehe COLIBRI-Architektur:
		- Microservices:
			- Diagnose,
			- Video,
			- usw.
		- REST-Schnittstelle: DWS
	- siehe [predic8](https://www.predic8.de/rest-beispiel.htm) oder [OpenWeather API](https://openweathermap.org/api)

## Lernzielkontrolle 03: Cloud Computing
- [ ] Ich kann die Entwicklung von Parallelverarbeitung in der IT-Branche technisch erläutern und motivieren.
	- Anwendungen (oder Teile einer Anwendung) werden in eine  Cloud verlagert, dort werden mehrere Instanzen der Software ausgeführt, welche Teile eines großen Datenbestandes parallel abarbeiten.
	- Motivation: 
		- Zeitersparnis / Geschwindigkeit
		- Entlastung des eigenen Rechenzentrums
- [ ] Ich kann Cloud-Computing definieren:
> Cloud Computing ist ein **Modell** das es erlaubt bei **Bedarf**, **jederzeit** und **überall** über ein Netz auf einen geteilten Pool von konfigurierbaren Rechnerressourcen zuzugreifen, die **schnell** und mit **minimalem Management-Aufwand** (inkl. ISP) zur Verfügung gestellt werden können.  
> — NIST, ENISA

![[Cloud_Eigenschaften.drawio.png]]  
![[Cloud_Eigenschaften_Comp.drawio.png]]

- [ ] Ich kann Gründe angeben, warum Cloud-Computing Vorteile hat und ebenso Nachteile darstellen:  

| Vorteile | Nachteile |
| :------ | :------- |
| “Pay as you go” | Daten-Vertraulichkeit |
| Hardware-Kosten geringer<br>Hardware-Wartung entfällt | Meta-Daten (von mir können bekannt werden) |
| Geräteunabhängig | Kosten |
| 24/7 Support | Aufgabe/Komplexität reicht für eine lokale Lösung |
| Skalierbarkeit | Abhängigkeit vom Netzwerkzugang |
| Automatisierbarkeit | Support-Probleme |
| Verfügbarkeit | |

- [ ] Ich kann Service-Modelle benennen und erläutern sowie SW-Stacks diesen zuordnen.  
![[Cloud_Services.png]]
![[Cloud_Services_Schichten.drawio.svg]]

- [ ] Ich kann die Begriffe Public-Cloud, Private-Cloud und Hybrid-Cloud einem virtuellen Kunden Vor- und Nachteilen darstellen:  
	- Public Cloud

| Vorteile  | Nachteile |
| :------- | :---------- |
| öffentlich | Datensicherheitsprobleme |
	- Private Cloud

| Vorteile | Nachteile |
| :------ | :------- |
| Anwender + Nutzer sind im selben Unternehmen | Kosten |
	- Hybrid-Cloud

| Vorteile | Nachteile |
| :------- | :-------- |
| mehrere Cloud-Infrastrukturen, die eigenständig genutzt werden | Kosten |
| | Managementaufwand |

- [ ] Ich kann von mindestens einem großen Cloud-Anbieter 5 Services benennen und deren Anwendungsmöglichkeiten darstellen.

| Services | Anwendungsmöglichkeit | 
| :-------- | :------------- |
| EC2 (Elastic Compute Cloud) | virtuelle Server/Computer in der Cloud |
| S3 (Simple Storage Service) | Skalierbare Speicherkapazität in der Cloud | 
| Route53 | Skalierbare DNS und Domain Name-Registrierung |
| Amazon Lex | Erstellen von Sprach- und Text-Chatbots | 
| Cloud9 | Eine Cloud-IDE zum Schreiben, Ausführen und Debuggen von Code |

- [ ] Möglichkeiten zur Kostenvorhersage bezüglich Cloud-Nutzung darstellen
	- AWS Pricing Calculator
		- Region (in der der Server steht)
		- Betriebssystem (Linux = kostenlos, Windows braucht Lizenz)
		- Anzahl an (virtuellen) CPUs
		- Größe des RAM
		- Größe der Festplatte
		- Anzahl der Instanzen
		- Nutzung (z.B. 2 Wochen im Monat, 3h am Tag, usw.)
		- Sparplan (z.B. 15% Rabatt bei Laufzeit von 12 Monaten)

## Lernzielkontrolle 04: Machine-Learning
- [ ] Ich kann Machine Learning definieren und Unterschiede zu Neuronalen Netzen, Künstlicher Intelligenz und Deep Learning benennen.

| Begriff | Erklärung |
| :---- | :--- |
| Machine Learning | System wird mit strukturierten und kategorisierten Daten (von Menschen bearbeitet) gefüttert und trifft darauf basierend Entscheidungen.|
| Deep Learning | System arbeitet mit unstrukturierten Daten (oder nicht vollständig kategorisierten Daten) und findet selber geeignete Unterscheidungsmerkmale, durch **Neuronale Netze**, die verschiedene Algorithmen kombinieren. |
| Neuronale Netze | System, das sich im Aufbau am menschlichen Gehirn orientiert und Computer mit Merkmalen künstlicher Intelligenz ausstattet. Sie bestehen aus mindestens 2 Schichten (Ein-/Ausgabe), den sogenannten Hidden Layers. |
| Künstliche Intelligenz | ist ein Teilgebiet der Informatik, das sich mit der Automatisierung intelligenten Verhaltens und dem maschinellen Lernen befasst. Der Begriff ist schwierig zu definieren, da es bereits an einer genauen Definition von „Intelligenz“ mangelt. Dennoch wird er in Forschung und Entwicklung verwendet.<br>**HINWEIS:** Deep Learning, Machine Learning und Neuronale Netze sind Teilgebiete der KI. |

- [ ] Ich kann den prinzipiellen Ablauf einer Machine Learning Anwendungserstellung darstellen und dabei auf Anlernphase und Anwendung des ML-Algorithmus eingehen.
	- **Anwendungserstellung**:  
![[ML_math_1.drawio.svg]]  
Menge von Funktionen (parametrisiert)  $F=\{f_p: f_p: \Omega \rightarrow \Psi\}$
		- Es gibt eine Güte-Funktion  (Fehler, Verlust, Risiko, ...)
			- $L(y,f_p(x))$  
		- Vorstellung von dieser Güte-Funktion:  
		![[ML_math_2.drawio.svg]]
		- $f_p(x)=\tilde y$, eigentlich will ich bei $y$ landen ==> Güte-Funktion gibt an, wie weit $\tilde y$ von $y$ weg ist.
		- Ziel: Suche die beste Funktion $f_*$, die den kleinsten Fehler macht
			- $f_* =\underset{f_p \in F}{\text{argmin}} \int_{\Omega} \int_{\Psi}L(y,f_p(x))\space p(x,y) \,dy\,dx$
			- Beispiel: Menge aller `.jpg`-Bilder
		![[ML_math_3.drawio.svg]]
			- Wir haben ein Cluster für $\underset{y_1}{\text{Frauen}}/\underset{y_2}{\text{Männer}}$
			- <span style="color: red">Suchen über gesamten</span> $\Psi$ <span style="color: red">und über gesamten</span> $\Omega$ <span style="color: red">die Funktionen mit dem kleinsten Fehler</span>
	- **Anlernphase**: 
		- Der ML-Algorithmus wird Daten "gefüttert", die durch Menschen strukturiert und kategorisiert worden sind. 
	- **Anwendung des ML-Algorithmus:** 
		- z.B. Unterscheidung von Hunden und Katzen, Männern und Frauen, Erkennung von Autos, usw.
- [ ] Ich kann Beispiele nennen, in denen ML-Services angewendet werden können und die sich daraus ergebenden Vorteile darstellen.

| Service | Vorteil |
| :------ | :------ |
| Objekt-Erkennung | Gesichtserkennung: automatisches Verpixeln von Gesichtern -> Datenschutz |
| Text-Erkennung | automatische Digitalisierung von (handschriftlichen Notizen) -> weniger Aufwand<br>Kennzeichen-Erkennung im Parkhaus, für Parkschranke -> geht schneller, User-Experience|
| Klassifikation | automatisches Kategorisieren / Labeln von Bildern (z.B. Gruppenfoto) -> weniger Aufwand |

- [ ] Ich kann mindestens 4 unterschiedliche ML-Services erläutern und mit welchen Tools diese ohne eine Anlernphase in eine eigene Anwendung integriert werden können darstellen.

| ML-Service | Tool |
| :----- | :----- |
| Klassifikation | AWS Detection, [ClarifAI](https://clarifai.com) |
| Objekt-Erkennung | Amazon Rekognition |
| Text-Erkennung | Amazon Textract |
| Sprach-Erstellung | Amazon Lex |
	- Integration in Anwendung durch API über Nutzung einer REST-Schnittstelle

- [ ] Ich kann erläutern mit welchen SW-Tools ich einen eigenen ML-Algorithmus "erstellen" würde und ich hierbei vorgehe.
	- SW-Tools:
		- NVIDIA-CUDA
		- Tensorflow (Google)
		- Coffee (Borklay)
	- Vorgehen:
		- Erfahrungen für ähnliche Probleme aus Communities holen
		- vortrainiertes Netzwerk benutzen
		- tiefes Neuronales Netzwerk bei vielen Eingangsdaten
		- flaches Neuronales Netzwerk wenn Laufzeit relevant ist

## Lernzielkontrolle 05: Docker
- [ ] Ich kann ein Ablauf-Bild beschreiben, wie ich vorgehen kann, um einen Docker-Container nutzbar zu machen. 
![[Erstellung_Docker.drawio.svg]]
1. Clonen 
```bash
docker pull
```
2. Build
```bash
docker container create
```
3. Ausführen "run"
```bash
docker run ubuntu
```
- interaktive Variante:
```bash
docker run -i ubuntu
```
- dort eine Bash starten:
```bash
docker run -i ubuntu /bin/bash
```
4. Starten / Testen / Modifizieren
- Hochladen
```bash
docker commit ubuntu Kasche:202211
```
- mein ehemaliger Container `ubuntu` wird in meinem Repository namens `Kasche` mit dem Tag `202211` hochgeladen

- [ ] Ich kann die Begriffe Docker‐Registry, Docker‐Daemon, Docker-Container, Docker‐Image, Docker‐Client und Docker‐File kurz erläutern.
	-  Docker Demon
		- zentrale Komponente zum verwalten:
			- der Container
			- der Images
			- der Netzwerk-Komponenten
			- des Datei-Systems

	- Image
		- Blaupause für eine virtuelle Umgebung
		- read-only Template zum Erstellen eines Containers
		- können Images erweitern
			- (z.B. 
				- Image1: Linux-Betriebssystem
				- Image2: Image1 + Software)

	- Container
		- ausführbare Variante eines Images
			- z.B. beim Start:
				1. Erzeugung Dateisystem
				2. read-only Einbindung des Dateisystems des Images
				3. Hinzufügen eines Read-Write-Layers
		- läuft in einem Prozess

	- Docker Client
		- ich als Anwender kann mittels Kommandozeile (CLI) mit dem *Docker Daemon* (REST-API) kommunizieren
	
	- Registry
		- zentrale Stelle, wo Images gespeichert werden

- [ ] Ich kann den Unterschied zwischen einer Verwendung einer virtuellen Maschine und einem Docker‐Ansatz benennen  
![[Docker.drawio.svg]] ![[VM.drawio.png]]  
	- Docker:
		- fein granularer
		- spezifischer
		- alle teilen sich ein OS

- [ ] Ich kann Vor‐ und Nachteile von Dockern motivieren und Gegenmaßnahmen bei den Nachteilen erläutern.

| Vorteile | Nachteile |
| :------- | :-------- |
| Ressourcen schonend | Lernkurve |
| gut erweiterbar (Kubernetes) | Sicherheitsbedenken, weil alles auf eine Ressource zugreift.<br>(z.B. Host-CPU) |
| | Dokumentation nach Entwicklung<br>(Ändern, Speichern, Committen, ...)<br>kann nicht zum Inhalt passen |

 - Gegenmaßnahmen:
	- Sicherheitsbedenken:
		- Quellen der Images überprüfen
			- unprivilegierte Container verwenden
			- Docker in VM ausführen
		- Dokumentation nach Entwicklung: 
			- automatische Dokumentation (durch bspw. Swagger)

- [ ] Ich kann neben der Anwendung von Dockern für Micro‐Services, noch andere Anwendungsfälle beurteilen.
	- Bereitstellung von Betriebssystem-unabhängigen Anwendungen
	- Anwendungstests vor der Bereitstellung (auf unterschiedlichen OS's) 
	- Cloud-Anwendung (portabel, können einfach umgezogen werden)

## Lernzielkontrolle 06: Mirco-Services
- [ ] Ich kann darstellen, was Micro‐Services sind und welche Vor‐ und Nachteile durch dessen Verwendung entstehen.
- Micro-Services:
	- kleine, ausführbare Programme, die direkt auf Betriebssystem ausgeführt werden
		- (inkl. Abhängigkeiten, Konfiguration)
		- klein $\widehat{=}$ Programm, welches EINEN spezifischen Sachverhalt lösen kann
		- es gibt Applikationsgrenze (nicht durch die verwendete Programmiertechnik gegeben) ==> Schnittstellen  

| Vorteile | Nachteile |
| :------- | :-------- |
| kann leicht angepasst werden, ohne den Rest in Mitleidenschaft zu ziehen | | 
| thematische Kohäsion | komplexere Softwareverteilung<br>komplexeres Testen<br>(durch die Vielzahl an Services) |
| geringe Kopplung | komplexere Architektur<br>mehr Lastverteilung notwendig<br>höhere Netzwerk-Latenzen (durch Schnittstellen) |
| Dev-Ops-Ideen (d.h. Entwickler und Anwender ganz nah beieinander) | komplexeres Logging und Monitoring<br>(durch ggf. unterschiedliche Logging-/Monitoringtechnologien) |

- [ ] Ich kann zeigen, warum Dev‐Ops Ideen geeignet sind, Micro‐Service‐Architekturen zu implementieren
	- CI/CD:
		- jeder Service kann eigenständig entwickelt, getestet und deployed ("ausgeliefert") werden
	- System, ist robuster, da die Services unabhängig voneinander sein sollen
	- Nicht das Gesamtsystem muss überwacht werden, sondern die einzelnen Services.  
	  (Einsatz von Spezialisten für jeden Service möglich.)

- [ ] Ich kann die Begriffe CI/CD, C‐Testing, C‐Überwachung, Canary‐Release, Kybernetes, Fehlerbudget bennenen und erklären.

| Begriff | Erklärung | 
| :------ | :------ |
| CI/CD | Continuous Integration: fortlaufendes Zusammenfügen von Komponenten (oder neuem Code) zu einer Anwendung (siehe `git merge`)<br>Continuous Deployment: fortlaufende Auslieferung, durch Software-Auslieferungsprozesse (z.B. Automatisierungsskripte) |
| C-Testing | Continuous Testing: fortlaufendes Testen, bspw. durch automatische Test-Frameworks (z.B. Jenkins) |
| C-Überwachung | fortlaufende Überwachung, durch Logging und Monitoring (-Software) |
| Canary-Releases | Releases, die mit den neuesten Features und Änderungen ausgestattet sind, werden Testern zur Verfügung gestellt. |
| Kubernetes | Software zur Verwaltung von Container-Anwendungen |
| Fehlerbudget | Ein Fehlerbudget ist die maximale Zeit, die ein technisches System ausfallen darf, ohne dass dies vertragliche Konsequenzen hätte. |

- [ ] Ich kann die Vorteile der Verwendung von einer REST‐Schnittstelle begründen.
	- flexibel: 
		- leicht zu verändern, da sie keinen direkten Einfluss auf die Funktionalität eines Services (einer Software) haben.
	- dynamisch skalierbar: 
		- Services (z.B. Docker-Container) können einfach mit einer REST-Schnittstelle versehen werden.
	- Nutzung von vorhandenen Technologien (siehe HTTP): 
		- HTTP wird von vielen Programmiersprachen standardmäßig unterstützt und bietet wohldefinierte Funktionen (GET, PUT, POST, DELETE, OPTIONS, HEAD, TRACE, CONNECT)

- [ ] Ich kann den prinzipiellen Ablauf des Entwurfes einer Micro‐Service-Architektur beschreiben.
	- **Ziel**: abgegrenzte Aufgabe soll übernommen werden
	- **IST-Stand**: komplexe Beziehungsgeflechte
	- **Theorie-Lösung**: Domänen-Analyse (Zuständigkeitsbereiche suchen)
![[MS_Entwurf_1.drawio.svg]]
	- erster Schritt:
		- Gliederung der Funktionalitäten in Fachbereiche
	- zweiter Schritt
		- Macro-Architektur entwerfen
		  (d.h. wie einzelne Micro-Services kommunizieren)
			- Server festlegen
			- Netzwerkverteilung
			- Protokoll (z.B. HTTP)
			- APIs
			- Austausch-Format (z.B. JSON, XML)
	- dritter Schritt
		- Festlegung von Randbedingungen
			- Paketierung
			- Installation
			- Konfiguration
			- Logging, Monitoring
			- Sicherheitsaspekte
			- unterschiedliche Anforderungskapazitäten

- [ ] Ich kann darstellen, wann Micro‐Service‐Architekturen eher nicht verwendet werden sollen.
	- Kein Micro-Service anwenden, wenn:
		- geringe Komplexität
		- keine Resilienz notwendig
		- komplexe Datenoperationen über Servicegrenzen hinweg

- [ ] Ich kann Anforderungen an einen Micro‐Service‐Architektur‐Entwurf aufzählen, die ich zur Evaluierung einer solchen benutzen kann.
	- Anzahl an Verantwortlichkeiten
	- Anzahl an Services
	- FAN-OUT pro Service zählen
		- (gibt es einen Service mit großen FAN-OUT)
			- (FAN-OUT = Zugriff auf externe Datenbestände)
	- Anzahl Testfälle pro Service
	- CRUD-Funktionalitäten (CRUD = Create, Read, Update, Delete)

- [ ] Ich kann die 12‐Faktoren‐Regel motivieren und mindestens 4 dieser Regeln benennen und begründen.
	- <span style="color:red">HINWEIS: 100%ig nicht bearbeitet während der Vorlesung</span>
	- Quellen: [dev-insider.de](https://www.dev-insider.de/was-ist-die-twelve-factor-app-a-894702/) & [12factor.net](https://12factor.net/de/)
	-   **I. Codebasis:** Das Fundament bildet ein Code, der zentral verwaltet und für verschiedene Versionen genutzt werden kann.
	-   **II. Abhängigkeiten:** Abhängige Elemente können ein System beeinträchtigen, weswegen sie benannt und möglichst isoliert werden.
	-   **III. Konfiguration:** Konfigurationsmöglichkeiten sowie unterstützende Dienste werden grundsätzlich in der Umgebung beziehungsweise als Ressourcenanhang geführt.
	-   **IV. Unterstützende Dienste:** Jeder Dienst, der von einer App für ihre normale Verwendung benötigt wird, ist als angehängte Ressource zu betrachten. Die App unterscheidet nicht zwischen lokalen und Drittanbieter-Diensten.
	-   **V. Build, Release, Run:** Die Phase des Erstellens und der Nutzung der App werden strikt separiert.
	-   **VI. Prozesse:** Eine App sollte in Form eines einzelnen oder mehrerer zustandsloser Prozesse laufen.
	-   **VII. Port-Anbindung:** Werden Dienste genutzt, werden diese über Ports professionell angebunden und exportiert.
	-   **VIII. Nebenläufigkeit:** Nebenläufigkeit wird durch das Skalieren individueller Prozesse ermöglicht.
	-   **IX. Verfügbarkeit:** Für Benutzerfreundlichkeit und hohen Komfort sorgt es gleichermaßen, dass die Software as a Service schnell gestartet und individuell gestoppt werden kann.
	-   **X. Dev/Prod-Parität:** Bei der Twelve-Factor-App wird angestrebt, dass Development (Entwicklung), Überprüfung und Produktion möglichst ähnlich umgesetzt werden. Dies dient nicht nur einer soliden Kostenreduzierung rund um die Entwicklungsarbeit der Experten. Auch eine bessere Vergleichbarkeit und optimal nutzbare Erfahrungswerte sowie das konsequente Entwickeln agiler Lösungen sind die Folge
	-   **XI. Logs:** In den einzelnen Anwendungen sollten Logs als Ereignisstrom behandelt werden.
	-   **XII. Admin-Prozesse:** Administrative Prozesse sollten grundsätzlich als einmalige Aktion behandelt werden.

## Lernzielkontrolle 07: Verschlüsselung
- [ ] Ich kann 4 HASH-Funktionen benennen und deren Verwendung erläutern.
	- HASH-Funktionen:
		- SHA256
		- <span style="color: red">MD1, MD5</span>
		- Whirlpool
		- <span style="color: red">SHA-1</span>, SHA-2, SHA-3
		- <span style="color: red">rot</span>=nicht mehr sicher
	- Verwendung bei:
		- Passwort-Speicherung
		- Integritätsprüfung  

- [ ] Ich kann erklären was eine Rainbow‐Tabelle ist und für meinen eigenen Service, den ich programmieren möchte, eine Gegenmaßnahme mit dem Schlüsselwort „SALT“ beschreiben.
	- Rainbow-Tabelle:
		- [Datenstruktur](https://de.wikipedia.org/wiki/Datenstruktur "Datenstruktur"), die eine schnelle, speichereffiziente Suche nach der ursprünglichen Zeichenfolge (in der Regel ein Passwort) für einen gegebenen [Hashwert](https://de.wikipedia.org/wiki/Hashfunktion "Hashfunktion") ermöglicht. Die Suche über eine Rainbow Table ist erheblich schneller als bei der [Brute-Force-Methode](https://de.wikipedia.org/wiki/Brute-Force-Methode "Brute-Force-Methode"), allerdings ist der Speicherbedarf höher. (- [Wikipedia](https://de.wikipedia.org/wiki/Rainbow_Table))
	- SALT:
		- Eine weitere Methode, die Generierung von Rainbow Tables unwirtschaftlich zu machen, ist der Einsatz von [Salt](https://de.wikipedia.org/wiki/Salt_(Kryptologie) "Salt (Kryptologie)"). Dabei wird an das Passwort vor dem Hashen ein – im Idealfall – zufällig generierter Wert, das Salt, angehängt. Das Salt wird zusammen mit dem Hashwert gespeichert, um das Passwort später überprüfen zu können, es ist also kein Geheimnis. (- [Wikipedia](https://de.wikipedia.org/wiki/Rainbow_Table#Salts))

- [ ] Ich kann erklären, warum es zwei prinzipiell unterschiedliche  
Verschlüsselungsverfahren gibt.
	-  symmetrische Verschlüsselung  
![[Symmetrische_Verschluesselung.drawio.png]]
		- Algorithmus:
			- schnell
			- durch Hardware beschleunigbar

-  asymmetrische Verschlüsselung  
![[asymmetrische_Verschluesselung.png]]
		- Algorithmus
			- langsamer
			- schlecht durch Hardware zu beschleunigen
		- **Grundidee**:
			- habe 2 Schlüssel
				- privater Schlüssel
				- öffentlicher Schlüssel
			- "Dateien", die mit dem öffentlichen Schlüssel verschlüsselt werden, können nur noch mit dem privaten Schlüssel entschlüsselt werden

- [ ] Ich kann ein Bild erstellen, mit dessen Hilfe die symmetrische Verschlüsselung erklärt werden kann und es erklären.  
![[Symmetrische_Verschluesselung.drawio.png]]

- [ ] Ich kann ein Bild erstellen, mit dessen Hilfe die asymmetrische Verschlüsselung erklärt werden kann und es erklären.  
![[asymmetrische_Verschluesselung.png]]

- [ ] Ich kann begründen, warum es sinnvoll ist, Digitale Zertifikate zu verwenden.
	- wird benötigt, um zu bestätigen, dass der öffentliche Schlüssel von mir ist.
	- verhindert Man-In-The-Middle-Attacken
	- (Man könnte sonst bei der asymmetrischen Verschlüsselung die mit dem <span style="color:green">public key</span> verschlüsselten Dateien abfangen und eigene stattdessen hochladen)

- [ ] Ich kann erklären, wie Digitale Zertifikate technisch funktionieren.
	- öffentlicher Schlüssel ist echt: wird durch andere **Instanz** bestätigt:
		- Instanz ist vertrauenswürdig, weil von übergeordneter Instanz bestätigt wurde, dass diese vertrauenswürdig ist
	- (ähnlich zur Signatur mit zusätzlicher Bestätigung einer Autorität)

- [ ] Ich kann erklären, was eine Blockchain ist und wie es prinzipiell technisch funktioniert.
	- digitales Protokoll für Transfer + Aufbewahrung von digitalen Informationen
	- dezentrale Datenbank, die ganz oft dupliziert wurde  
![[Blockchain.drawio.png]]

- [ ] Ich kann Vor‐ und Nachteile der Blockchain‐Technologie darstellen.

| Vorteile | | Nachteile |
| :------ | :---: | :------ |
| dezentral<br>(von zentrale unabhängig) | Eigenverantwortung | Größe
| kompletter Log aller Transaktionen | | im Allgemeinen wird Blockchain mit Bitcoin gleichgesetzt
| Rückverfolgbarkeit | | Energieaufwand |

