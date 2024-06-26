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
- Configuration Management = WICHTIG!
## Planung und Implementierung
- funktionale Anforderungen
	- Komponenten, Aufbau des Systems, Software
- nicht-funktionale Anforderungen
	- Verfügbarkeit, Durchsatz, Bandbreite, Übertragungsrate
	- Leistungsanforderungen
		- max. Verzögerung / Latenz
		- Durchsatz
	- Resilienz- & Verfügbarkeitsanforderungen
		- 100% Verfügbarkeit mit geringem Wartungsfenster
		- verfügbar ohne merkliche Ausfälle
	- Spannungsversorgung und Klimatisierung
		- Ausfallsicherheit (ausreichende Netzteile, Notstrom)
		- Ausfallvorbeugung (kein Überhitzen, längere Laufzeit, weniger Ausfälle)
	- Sicherheitsanforderungen
		- Unternehmensrichtlinien --> Datenschutz, Geheimhaltung, Cyber-Security
		- zu schützende Aspekte
			- Identifizierung der Assets
			- Identifikation
			- Authentifizierung
			- Zugriffskontrolle
		- Sicherheitsrichtlinie + Prozess zur Umsetzung
	- Verwaltbarkeitsanforderungen
		- Status, Leistung, Prüfung ordnungsgemäßer Funktion, einheitliche Schnittstelle
			- --> Dashboard und ähnliches
			- einfache Administration sehr wichtig!
	- Rückwärtskompatibilität
		- Green Field = Neuer Anfang
		- Brown Field = Upgrade / Update von Bestandssystem
	- Sonstige Anforderungen
		- Kosten --> sofort / laufend
		- Limitierung von Assets
		- Richtlinien, Zertifikate
## Design, Klassifizierung und Topologien
| Einfachheit der Verwaltung | Adaptivität | Ausbaufähigkeit | Funktionalität |
| :-- | :-- | :-- | :-- | 
| Lazy Admin<br>wichtige Dokumentation | neue Technologie | Upgrade & Lifecycle | siehe LH & PH |

- verschiedene Klassifizierungen
	- Topologien / Strukturen
	- Größe / Leistungsfähigkeit
	- Übertragungsmedien
	- Anwendungsbereich
	- Protokollebene heterogen / homogen
	- HW / SW
	- räumliche Ausdehnung
	- Betriebsmodus (Client-Server / P2P)
- heterogene Netze
	- parallel laufen verschiedener Methoden und Systeme
	- notwendig, aber nicht schön
	- NGN (Next Gen Network) = Versuch alles unter TCP/IP zu vereinheitlichen
	- Übertragungswege sind heterogen --> LAN, WLAN, Glasfaser
- physikalische Struktur von Netzwerken
	- ![[Pasted image 20231118104837.png]]
	- Bestimmung durch Einsatzort 
- logische Struktur des Netzwerks
	- Datenfluss kann von der physischen Topologie differieren
- DMZ = demilitarisierte Zone
	- Bereich für Server, der Dienste für Externe anbieten
	- nicht mehr direkt im eigenen Netzwerk
## Architekturen / Topologien für große Netze
- strukturierte Herangehensweise
	- Hierarchie, Flexibilität, Modularität, Sicherheit, Ausfallsicherheit
- Cisco-Icons
	- ![[Pasted image 20231118105747.png]]
- Three Layer Hierarchisches Design
	- Core: benötigt mehr Performance
	- Distribution: Aggregation von Verbindungen (Verbidnung mittels Vollvermaschung)
	- Access: Anbindung der Clients an das Netzwerk
	- ![[Pasted image 20231118110117.png]]
	- Was passiert an der Grenze von L2 zu L3?
		- Verwerfen von Broadcasts, Segmentierung des Netzes
	- Aufgaben / Eigenschaften Core Layer
		- Niedrige Latenz
		- Schneller Transport
		- Hohe Zuverlässigkeit
		- Hop Count
		- Fehlertoleranz
		- QoS
		- CPU Last
		- Redundanz / Ausfallsicherheit
	- Aufgaben / Eigenschaften Distribution Layer
		- Richtlinien (Policy)
		- Redundanz / Lastverteilung
		- Sicherheit / Filterung
		- QoS
		- Routing
		- Zugriffssteuerung
		- Broadcast / Multicast Domains
		- Aggregation LAN / WAN / Adressbereiche
	- Aufgaben / Eigenschaften Access Layer
		- Benutzerzugriff auf lokale Segmente im Netz
		- typischerweise mit Switches
		- Segmentierung: Erhöhung der Bandbreite durch Anzahl der Geräte pro (Ethernet) Segment
		- Funktionen:
			- Switching, High Availability, Sicherheit auf Port-Ebene, Unterdrückung Broadcasts
- Two-Tier Collapsed Core Design
	- ![[Pasted image 20231118110303.png]]
	- Distribution-Layer entfällt, oder mit Core-Layer zusammengefasst
- Hierarchical Design durch Switching oder Routing
	- hier Switching auf Distribution-Layer ![[Pasted image 20231118111752.png]]
	- hier Routing auf Distribution Layer ![[Pasted image 20231118111815.png]]
- Virtuelle Zusammenfassung von Switches
	- ![[Pasted image 20231118112348.png]]
	- STP = Spanning Tree Protocol
	- VSS = Virtual Switching System
	- **für Till: Merk dir das !!**
- Hub and Spoke
	- ![[Pasted image 20231118112715.png]]
	- Hub and Spoke = Stern
- Unternehmensnetzwerk
	- ![[Pasted image 20231118113208.png]]
	- Enterprise Campus
		- kleines Netzwerk (<1000 Clients) --> Two Layer
		- großes Netzwerk (>1000 Clients) --> Three Layer
		- = Intranetz
	- Enterprise Edge = Übergang nach Draußen / Innen
		- RAS = Remote Access Service
		- VPN = Virtual Private Network
		- ![[Pasted image 20231118114150.png]]
		- ![[Pasted image 20231118114157.png]]
		- Zugang zum Intranet
		- Übergang zum Internet Service Provider
		- MPLS = Multi Protocol Label Switching
		- PSTN = Public Switched Telephone Network
		- ![[Pasted image 20231118115143.png]]
	- Enterprise Data Center
	- Redundanzen für die Ausfallsicherheit beachten!
		- <span style="color:red">WICHTIG!</span> ![[Pasted image 20231118120024.png]]
		- RIP = Routing Information Protocol
		- ICMP = Internet Control Message Protocol
	- Redundanz bei Servern
		- kritische Unternehmensdienste: Was läuft wo?
		- Maßnahmen zur Realisierung von Redundanzen
			- doppelt auslegen und Daten spiegeln
			- verschiedene Netze
			- redundante Netzteile
			- nie nur ein Link
	- Routenredundanz
		- Load Balancing
		- Erhöhte Verfügbarkeit
			- Vollvermascht, Teilvermascht
	- Redundanzen ![[Pasted image 20231118120739.png]]
	- Data Center ![[Pasted image 20231118121202.png]]
		- Vorteile von Switches
			- einfache Bedienung
			- einfache Verwaltung
			- hoher Datendurchsatz, weil schneller als Routing
				- Interfaces, Backplanekapazität, CPU
		- STP = ungenutzte Links
			- "Lösung" durch VLANs möglich
				- ungenutzte Links werden verwendet
				- Load-Balancing der VLAN möglich, aber nicht der Daten im VLAN
		- Kritik am Three-Tier-Design
			- nicht (genug) skalierbar
				- Flooding, Anzahl VLANs, ARP nervt, Switches und STP
			- recht komplex
			- Fehler haben große Auswirkungen
			- Unvorhersagbarkeit
			- Inflexibilität
			- mangelnde Agilität
		- Vorschlag fürs Data Center = Spine and Leaf
			- ![[Pasted image 20231118122153.png]]
			- Spine = obere Switches
			- Leaf = untere Switches
			- Jeder Leaf mit jedem Spine verbunden
			- Problem: max. Anzahl der Leafs = max. Anzahl der Spine-Ports
			- ![[Pasted image 20231118122530.png]]
## Implementierung
### Operations Management
- Operations Center
	- Zentrale Einrichtung
	- Überwachung des Betriebs des Systems
	-  Eigene Infrastruktur und Software zur Systemverwaltung
	- ![[Pasted image 20231118143000.png]]
	- Verteilung von Aufgaben nach Themengebieten
		- Server & Applications, Network, Storage
- Netzwerkmanagement ![[Pasted image 20231118145716.png]]
	- Managementmöglichkeiten:
		- SNMP, CORBA, Web-Interface, Command-Line
- SNMP
	- unterschiedliche Versionen: v1, v2, v3
	- UDP-basiert
		- bessere Wahl bei Überlast
	- Manager = Network Management Station (NMS)
		- Sammeln von Informationen von anderen Geräten durch *Polling* und *Traps*
		- Polling = Abfrage eines anderen Gerätes
		- Trap = Mitteilung über ein eingetretenes Ereignis durch Agent 
			- asynchron
	- Agent = Software die auf dem abgefragten Gerät läuft
	- ![[Pasted image 20231118151516.png]]
	- SMI = Structure of Management Information (SMI)
		- Definition verwalteter Objekte und deren Verhalten
		- Agent hat eine Aufstellung aller Objekte, die er verfolgt
		- Beispiel Object: Status der Schnittstelle eines Routers (`up`, `down`, `testing`)
		- nur  die Art wie definiert wird
	- MIB = Management Information Base
		- Datenbank
		- enthält verwaltete Objekte, der der Agent verfolgt
		- Definition aller Status / Statistiken, auf die vom NMS zugegriffen werden kann
		- MIB = Definition der Objekte (SMI Syntax)
	- Communities
		- quasi Passwörter anhand derer die Zugriffsrechte erteilt werden
	- OID = Object Identifier 
		- definiert ein verwaltetes Objekt eindeutig
		- OID = numerisch oder menschenlesbar
		- Datentypen: Abstract Syntax Notation One (ASN.1)
		- Basic Encoding Rules (BER): Regeln, wie Instanzen von Objekten codiert (Oktette) werden
		- OID-Baum = Strukturierung von Objekten in einem Baum ![[Pasted image 20231118154559.png]]
			- 1.3.6.1 = iso.org.dod.internet
## Aufgaben
- ARP = Address Resolution Protocol
	- Verbindungsstelle zwischen L2 und L3
	- Ermitteln der MAC-Adresse zur IP-Adresse
	- Gratuitous ARP
		- Informiert das Netzwerk über IP-Adressänderungen oder überprüft IP-Adresskonflikte.
- VLAN = Virtual Local Area Network
	- Möglichkeit zur Aufteilung von physischen Netzen in mehrere logische Netze
	- kein Datenaustausch zwischen den logischen Netzen möglich auf L2
	- zwischen VLANs muss geroutet werden
	- tag-basiertes, port-basiertes VLAN
- DNS = Domain Name System
	- Implementierungen:
		- Dnsmasp, Unbound, BIND, Microsoft DNS
	- Port 53
	- Anwendung von UDP und TCP
	- DNS-Anfrage max. 512 Bytes (für UDP)
		- bei Überschreitung der Größe --> TCP
		- Authentizitätsprüfung über DNSSEC
	- DoT (DNS over TLS), DoH (DNS over HTTPS)
		- für Verschlüsselung
	- Befehle für DNS-Abfrage:
		- `nslookup`
		- `dig`
	- Unterschied zwischen Zone und Domain:
	- **Domain**:
		- **Definition**: Sammlung von Netzwerkressourcen unter einer gemeinsamen Namensstruktur.
		- **Beispiel**: `example.com`.
		- **Einsatz**: Organisation und Identifikation im Internet.
	- **Zone**:
		- **Definition**: Administrativer Teil einer Domain in DNS.
		- **Verantwortung**: Enthält eigene Resource Records.
		- **Beispiel**: `sales.example.com` kann eine Zone in der Domain `example.com` sein.
		- **Einsatz**: Verwaltung spezifischer Teile einer Domain.
	- SOA = Start of Authority
		- markiert den Beginn einer Zone
		- `dig domain.de SOA`
		- `nslookup -type=SOA domain.de“`
	- Ausfall-Vorsorge beim DNS
		- Primärer Server
			- Record read / write
		- Sekundärer Server
			- schreibgeschützte Kopie des Primary Servers
	- DNS-Flags:
		- Truncated
		- Non-authenticated data: Unacceptable
		- Answer authenticated: Answer [...] authenticated by server
	- Besonderheit bei der Authentifizierung von autoritativen Nameserver:
		- Er ist der autoritative Nameserver. Daher braucht und kann er die Nachricht nicht als authenticated markieren. Die Autentication bezieht sich lediglich auf die rekursiven Name Server, die die Kette zum Authority Server validieren müssen.
- LLDP
	- Link Layer Discovery Protocol ist ein standardisiertes Netzwerkprotokoll, das entwickelt wurde, um Informationen über Netzwerkgeräte in einem lokalen Netzwerk zu sammeln und auszutauschen. LLDP ist auf Layer 2 des OSI-Modells angesiedelt und ermöglicht es, Informationen über die direkten Nachbarn eines Geräts im Netzwerk zu ermitteln.
- RIP
	- Interior Gateway Protocols
		- innerhalb eines Autonomen System (AS) angewandt
	- ![[Pasted image 20231121163826.png]]
	- Funktionsweise:
		1. **Nachbarschafts-Check**: RIP-Router schnacken mit ihren direkten Nachbarn.
		2. **Abstandsmessung**: Sie messen die Distanz zu Netzwerken in Hops.
		3. **Regelmäßige Updates**: Alle 30 Sekunden teilen sie ihre Routeninfos.
		4. **Wegwahl**: Kürzester Pfad (wenigste Hops) wird bevorzugt.
		5. **15-Hop-Limit**: Alles über 15 Hops ist "too far away", Bro.
		6. **Update bei Änderungen**: Falls sich was im Netz ändert, werden die Infos ASAP aktualisiert.
	- nutzt UDP
	- verdammt viel Traffic, verdammt langsam, verdammt unzuverlässig
- Autonomes System (AS)
	- Menge von Routern die mehrere Netzwerke verbinden mit einem gemeinsamen inneren Gateway-Protocol (IGP) und gemeinsamen Metriken, die bestimmen, wie Pakete innerhalb eines AS vermittelt werden, unter einer einzigen technischen Verwaltung