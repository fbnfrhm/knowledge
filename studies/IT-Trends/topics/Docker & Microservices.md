# Docker (Allgemein)
- isolierte Maschine (Sandbox)
- Methode um Software zu verpacken (komplett)
- damit diese
	- bereitgestellt werden kann
	- dynamisch verteilt werden kann
	- skaliert werden kann
- um z.B. Microservices zu implementieren

## Vergleich Docker vs. VM
### Virtuelle Maschinen (VM)
![[VM.drawio.png]]

### Docker
![[Docker.drawio.svg]]
- fein granularer
- spezifischer
- alle teilen sich ein OS

## Docker Demon
- zentrale Komponente zum verwalten:
	- der Container
	- der Images
	- der Netzwerk-Komponenten
	- des Datei-Systems

## Image
- Blaupause für eine virtuelle Umgebung
- read-only Template zum Erstellen eines Containers
- können Images erweitern
	- (z.B. 
		- Image1: Linux-Betriebssystem
		- Image2: Image1 + Software)

## Container
- ausführbare Variante eines Images
	- z.B. beim Start:
		1. Erzeugung Dateisystem
		2. read-only Einbindung des Dateisystems des Images
		3. Hinzufügen eines Read-Write-Layers
- läuft in einem Prozess

## Docker Client
- ich als Anwender kann mittels Kommandozeile (CLI) mit dem *Docker Daemon* (REST-API) kommunizieren

## Registry
- zentrale Stelle, wo Images gespeichert werden

## Zusammenarbeit der Docker-Bestandteile
![[Docker_Architektur.drawio.svg]]
### Erstellung eines Dockers
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

### Docker-Files
Docker-Files $\widehat{=}$ Skript  

Aufbau:
```dockerfile
FROM ubuntu:20.04
COPY "C:/.../myapp/." /app
RUN make app
CMD python /app/myapp.py
```

| Vorteile | Nachteile |
| :------- | :-------- |
| Ressourcen schonend | Lernkurve |
| gut erweiterbar (Kubernetes) | Sicherheitsbedenken, weil alles auf eine Ressource zugreift.<br>(z.B. Host-CPU) |
| | Dokumentation nach Entwicklung<br>(Ändern, Speichern, Committen, ...)<br>kann nicht zum Inhalt passen |

## Micro-Services
- kleine, ausführbare Programme, die direkt auf Betriebssystem ausgeführt werden
	- (inkl. Abhängigkeiten, Konfiguration)
	- klein $\widehat{=}$ Programm, welches EINEN spezifischen Sachverhalt lösen kann
![[MS_Applikation.drawio.svg]]
	- es gibt Applikationsgrenze (nicht durch die verwendete Programmiertechnik gegeben) ==> Schnittstellen  

- Micro-Service Vorteile:
	- kann leicht angepasst werden, ohne den Rest in Mitleidenschaft zu ziehen.
	- thematische Kohäsion
	- geringe Kopplung
			- Dev-Ops-Ideen (d.h. Entwickler und Anwender ganz nah beieinander)

- CI/CD ... Methode / Taktik um Code kontinuierlich zu testen und bereitzustellen
	- (dafür wird eine Automatisierungspipeline verwendet)
		- manuelle Arbeit $\downarrow$
		- Hindernisse $\downarrow$
	- d.h. mindestens täglich Code
		- zusammenführen
		- zu testen <span style="color: red">(Fehler schnell erkennen)</span>
		- Endbenutzer zur Verfügung zu stellen <span style="color: red">(aktives Feedback)</span>
	- viel Visualisierung & viel Kommunikation
		- Kanban, SCRUM, agile Methoden, Infrastructure as Code
	- Beispiele für *CX*:
		- CD = Continuos Delivery
		- CT = Continuos Testing
		- CI = Continuos Integration
		- CÜ = Continuos Überwachung
	- passt sehr gut zu der Grundidee Micro-Services

# Standardisierte Schnittstellen
## REST (Representational State Transfer)
- HTTP
- URL
- URI
- Zustandlos
- einheitlich, bewährte Schnittstelle mit Standardmethoden
	- (GET, PUT, POST, DELETE, OPTIONS, HEAD, TRACE, CONNECT)

## SOAP (Simple Object Transfer Protocol)
## API-Gateway (Backend for Frontend)
![[API-Gateway.drawio.png]]
- Vorteil:
	- Authentifizierung inklusive und an einer zentralen Stelle
	- SSL-Terminierung
	- Cache
	- ist quasi ein Reverse-Proxy
- Nachteil:
	- nur eine Stelle, die Micro-Service Zugang regelt (Single Point of Failure)
	- Ressourcen-Engpässe (API Gateway Team ist für dieses alleine zuständig)
	- Zusatzaufwand
	- höhere Netzwerklast
	- Nadelöhr-Problem bei Skalierung

# Anforderungen an Micro-Service
- unabhängiges Entwicklerteam
- schnell & unabhängig auslieferbar
- funktional und datenmäßig abgegrenzt (eine Aufgabe lösen + verläßlich)
- Verfügbarkeit
- technologische Wahlfreiheit
- dynamisch skalierbar
- Umgebungsunabhängig (z.B. Docker)
- Resilienz
- Kein Micro-Service anwenden, wenn:
	- geringe Komplexität
	- keine Resilienz notwendig
	- komplexe Datenoperationen über Servicegrenzen hinweg

# Kriterien für geschickt gewählte Microservice-Architektur
- Anzahl an Verantwortlichkeiten
- Anzahl an Services
- FAN-OUT pro Service zählen
	- (gibt es einen Service mit großen FAN-OUT)
		- (FAN-OUT = Zugriff auf externe Datenbestände)
- Anzahl Testfälle pro Service
- CRUD-Funktionalitäten

# Architektur-Entwurf
- **Ziel**: abgegrenzte Aufgabe soll übernommen werden
- **IST-Stand**: komplexe Beziehungsgeflechte
- **Theorie-Lösung**: Domänen-Analyse (Zuständigkeitsbereiche suchen)
![[MS_Entwurf_1.drawio.svg]]
## zweiter Schritt
- Macro-Architektur entwerfen
  (d.h. wie einzelne Micro-Services kommunizieren)
	- Server festlegen
	- Netzwerkverteilung
	- Protokoll (z.B. HTTP)
	- APIs
	- Austausch-Format (z.B. JSON, XML)
## dritter Schritt
- Festlegung von Randbedingungen
	- Paketierung
	- Installation
	- Konfiguration
	- Logging, Monitoring
	- Sicherheitsaspekte
	- unterschiedliche Anforderungskapazitäten
## Beispiel-Architektur
![[MS_Beispiel_Architektur.drawio.svg]]
