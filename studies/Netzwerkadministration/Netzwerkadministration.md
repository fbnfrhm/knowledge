# Klausurvorbereitung
## ISO/OSI-Referenzmodell
![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/80/ISO-OSI-7-Schichten-Modell%28in_Deutsch%29.svg/1024px-ISO-OSI-7-Schichten-Modell%28in_Deutsch%29.svg.png)
![](https://dev-supp.de/fileadmin/_processed_/2/a/csm_iso-osi-schichtenmodell_3671978625.jpg)
- Transport-Layer (L4)
	- erste Ende-zu-Ende-Kommunikation
	- verbindungslos (UDP)
	- verbindungsorientiert (TCP)
		- Reihenfolge garantiert
	- bietet einheitlichen Zugriff für obere Schichten
	- Verschlüsselung möglich über TLS / IPSec 
	  (Achtung nicht ganz in ISO/OSI & TCP/IP einordbar)
- Session-Layer (L5)
	- Aufgaben
		- Dialogsteuerung
		- Token-Verwaltung
		- Synchronisation
	- Sitzung = zeitbeschränkte Zwei-Wege-Verbindung zwischen Komm.-Teilnehmern
	- Bsp.: SIP = Session Initiation Protocol
- Ablauf einer Sitzung:
	- Initialisierung / Aufbau
		- Reservierung von Ressourcen
	- Unterhalt
		- Aufrechterhaltung (Heartbeat, Timer, Keep-Alive)
	- Gesteuerter Abbau
		- Graceful Termination
		- Freigabe von Ressourcen bei erfolgreicher Beendigung
- Darstellungsschicht (L6)
	- Darstellung der Daten an den Endpunkten
		- Codierung / Decodierung
		- Kompression / Dekompression
		- Ver- / Entschlüsselung
	- Integrität, Vertraulichkeit, Verfügbarkeit
- Anwendungsschicht (L7)
	- stellt Funktionen / Protokolle für Anwendungen bereit
## Kommunikation zwischen Punkten
- Broadcast --> alle Teilnehmer 
- Unicast --> Point-to-Point
- Multicast --> Point-to-Multi-Point (Teilnehmergruppen)
- Anycast
	- Gruppe von Rechnern mit einer Adresse
	- der mit der kürzesten Route (meistens) antwortet
## Hardware / Software
### Hardware
- Switch
	- mit MAC-Adressen
	- logische Weiterleitung von Frames im L2
- Hub
	- alle an der selben Leitung
- Router
	- Verbindungspunkt zwischen zwei Netzen
	- Routing zwischen den Netzen
	- Weiterleitung von Paketen im L3
### Software
- Management
- Firmware
- Implementierung von Protokollen
## ISO/OSI-Prinzipien
1. Nicht zu viele Layer, weil sonst unübersichtlich
2. Mache Schnittstellen an den kleinstmöglichen Punkten
3. Verschiedene Schichten für verschiedene Funktionen und Technologien
4. Fasse alles Zusammengehörige zusammen


## Planung
![[Pasted image 20231113170650.png]]
1. Planung (Planning)
	- Netzwerkspezifikation 
	- Entscheidung über den physischen & logischen Aufbau des Netzwerks
	- Ressourcen + Betriebskosten
2. Umsetzung (Implementation)
	- Beschaffung
	- Installation / Entwicklung
	- Tests
3. Betrieb (Operation)
	- Erfüllen der Spezifikation
	- Netzwerkmanagement-System
4. Upgrade / Terminate
	- Übergang mit Ende der Betriebsdauer
	- System outdatet --> Update
		- zurück zur Planungsphase
	- Abbau
		- Ausleitung der Daten / Informationen
		- Übergang zu neuem System
## Netzwerkarten
- WAN mit NSP Link
	- NSP = Network Service Provider
		- Anmietung von Netzwerkinfrastruktur
- Shared Hosting Data Center
	- ![[Pasted image 20231113172511.png]]
	- Bereitstellung von Diensten an Kunden
	- Sicherstellung von Verfügbarkeit  der Anbindung über SLA (= Service Level Agreement)
- Unternehmen
	- ![[Pasted image 20231113172740.png]]
- Network Service Provider
	- ![[Pasted image 20231113172822.png]]
	- POP = Point of Presence
	- IXP = Internet Exchange Point

## Netzwerkmanagement
- SNMP
	- ![[Pasted image 20231113173636.png]]
	- MIB = Management-Information-Base
		- Standardisierung von Verwaltungsinformationen
	- MO = Managed Objects
	- OID = Object-ID
	- SMI = Structure of Management Information
		- Konzepte zur Beschreibung der MOs 
## Funktionsmodell
- F = Fault Management
	- Erkennen --> Isolieren + Analysieren --> Beheben --> Dokumentieren
- C = Configuration Management
	- Konfigurationsdaten zu allen Geräten im Netz sammeln, speichern und überprüfen
- A = Accounting Management
	- faire Verteilung der Ressourcen (CPU, Speicher, Kosten, Bandbreite)
- P = Performance Management
	- Erhebung von Metriken zur Systemleistung / Netzwerkleistung
		- Ziel: Optimierung
		- Sammeln --> Baseline festlegen --> Schwellen festlegen
- S = Security Management
	- Sicherstellung eines sicheren Betriebs
	- Zugriffskontrolle auf Ressourcen
	- Sicherheitsmaßnahmen
- ![[Pasted image 20231113175617.png]]

Fortsetzen bei 230909_2