
# Microservice
- Architekturmuster der IT
- Anwendungssoftware wird aus unabhängigen Prozessen komponiert
	- Notwendigkeit einer Sprachenunabhängigen Programmier-Schnittstelle
- **Dienste**, die entkoppelt sind

## Dienste 
1. i.d.R. überschaubar, klein, einfach ersetzbar
2. haben eine abgegrenzte Geschäftsfunktion
3. Schnittstellen:
	- HTTP-Request
		- gut testbar
		- von allen Programmiersprachen unterstützt
		- etablierte Technologie
		- selbstsprechend
		- **Aufbau:** HTTP-Adresse + Request
4. Dienste sind voneinander unabhängig
	- Programmiersprachen
	- Datenbanken
	- Technologie-Stack
	- Fehlerzustände werden nicht weitergeleitet
	- eigener Lebenszyklus

## SOA = Service Orientierte Architektur
![[SOA.drawio.svg.svg]]  
- bei Microservices: jeder Service kann eigenes UI haben
- hier: ein geteiltes UI

# REST = Representational State Transfer
- weder Protokoll noch Standard
- dient zur Kommunikation von verteilten Systemen
- mit HTTP 1.1 parallel entwickelt
	- (WWW liefert eine REST-konforme Infrastruktur)
- **Aufbau:** `http(s)://adresse:port/beliebigeDaten`
	-  z.B. `https://itt.kasche.dhge-web.de/register?name=Kasche&email=bernd.kasche@dhge.de&login=Kasche Be`
		- `.../register`
			- Request --> HTML-Seite
		- `.../login`
			- Request --> JSON

## Eigenschaften von REST:
1. Client-Server-Modell (UI ist von Datenhaltung getrennt)
2. Zustandslos
3. gleiche Anfragen dürfen **gecached** werden
4. Schnittstelle einheitlich
5. Schichten-System
6. Code nach Bedarf nachladbar

# Anwendung von Microservices
siehe [[Docker]]
