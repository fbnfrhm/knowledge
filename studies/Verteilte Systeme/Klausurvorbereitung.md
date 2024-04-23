# Foliensatz 1
## Unterschied Verteilt und Dezentralisiert
![[Centralized-Decentralized-Distributed.png]]

### Centralized
- Systeme können nach außen hin zentralisiert erscheinen, auch wenn sie "im inneren" verteilt sind
	- Stichwort: logische / physische Zentralisierung
### Dezentralisiert
>A decentralized system is a networked computer system in which 
>processes and resources are **necessarily** spread across multiple 
>computers.
- Core-Nodes die untereinander kommunizieren
- z.B. 
	- GPS --> mindestens 3 Satelliten notwendig 
	- Machine Learning (ChatGPT)
	- Tsunami-Warn-Bojen 
### Distributed
> A distributed system is a networked computer system in which processes 
> and resources are **sufficiently** spread across multiple computers.
- Einzelne Nodes die untereinander kommunizieren können, aber nicht müssen
- Nicht alle Distributed Systems sind auch dezentralisiert
- Erstellen verteilter Systeme:
	- integrativ:
		- Verbindung zweier vernetzter Computer Systeme untereinander
	- expansiv:
		- Verbindung neuer Computer an ein vernetztes Computer System
- z.B. 
	- Streaming Services,
	- Fediverse,
	- Cloud, IoT, Autos
- Mehrere Systeme, die sich wie eines verhalten
	- Ressourcen teilen:
		- Storage, Compute Power, Files
		- Economics, billiger
		- Beispiele:
			- Cloud-based storage and files
			- Peer-to-peer assisted multimedia streaming (Spotify, Napster)
			- Shared mail services (Outlook, Exchange)
			- Shared Web Hosting (CDN)

### Design Goals
- Ressource sharing unterstützen
- Distribution Transparency
- Openness
- Scalability

#### Transparency
> The phenomenon by which a distributed system attempts to hide the fact that
> its processes and resources are physically distributed across multiple
> computers, possibly separated by large distances.

![[Transparency.png]]

- 🛑**Transparenz hier: Undurchsichtigkeit**🛑
	- der Versuch zu Verstecken, dass ein System aus mehreren Systemen besteht
- Distribution Transparency wird durch **Middleware Layer** gehandelt
![[Transparenz_Typen.png]]
- Transparenz ist nicht immer gut!
	- Latenzen können nicht immer versteckt werden
	- Keine Unterscheidung zwischen langsamer und failing Computer
	- erschwertes Debugging
	- zu viel Aufwand
	- nicht immer sinnvoll
- Distribution offenzulegen kann gut sein
	- Location-based Services
	- Handling von Nutzern in unterschiedlichen Zeitzonen
	- vereinfachtes Verständnis über den Ablauf
> Distribution transparency is a nice goal, but achieving it is a different Story, and it should often not even be aimed at.

#### Openness of distributed systems
> system that offers components that can easily be used by, or integrated into other systems. An open distributed system itself will Often consist of components that originate from elsewhere.
- Schnittstellen, Schnittstellen, Schnittstellen...

### Dependability
- Komponenten können die Services anderer Komponenten beanspruchen
- Komponenten können voneinander abhängig sein, wenn ihre Korrektheit auf der Korrektheit anderer Komponenten aufbaut.

| Requirements    | Description                                                  |
| --------------- | ------------------------------------------------------------ |
| Availability    | Readiness for usage, No Down Time                            |
| Reliability     | Continuity of service delivery<br>Correctness of the service |
| Safety          | Very low probality of catastrophies                          |
| Maintainability | How easy can a failed system be repaired                     |
#### Terminology

| Term    | Description                                        | Example                            |
| ------- | -------------------------------------------------- | ---------------------------------- |
| Failure | A component is not living up to its specifications | Service is not respond latest data |
| Error   | Part of a component that can lead to a failure     | Data can not be synced             |
| Fault   | Cause of that error                                | Network not responding             |

| Term              | Description                                                             | Example                                                                                                                         |
| ----------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Fault prevention  | Prevent the occurrence of a fault                                       | Good and safe programming,<br>Don't hire sloppy programmers                                                                     |
| Fault tolerance   | Build a component and make it mask the occurrence of a fault            | redundancy,<br>Build each component by two independent programmers                                                              |
| Fault removal     | Reduce the presence, number, or seriousness of a fault                  | Cable repair,<br>Get rid of sloppy programmers                                                                                  |
| Fault forecasting | Estimate current presence, future incidence, and consequences of faults | Forecast which connection will be at load cap and upgrade it,<br>Estimate how a recruiter is doing by hiring sloppy programmers |
- Transient Fault = vorübergehender Fehler
	- temporäres Problem
	- Funkitoniert beim nächsten Versuch
	- Kommt nur einmal vor
	- z.B. Netzwerkfehler 
- Intermittent Fault = sich wiederholender Fehler
	- temporär, tritt in Intervallen auf
	- z.B. Wackelkontakt im Kabel
- Permanent Fault = permanenter Fehler
	- z.B. zerschnittenes Kabel
#### On Security
- Confidentiality, Integrity
- Authentication, Authorization, Trust
- Verschlüsselung, Hashing 
![[digital_signatures.png]]
- Achtung $H$ = Hash-Algorithmus

### Scale in distributed systems
#### Size scalability 
- Unterstützung von mehr Nutzern
- Probleme bei der Skalierung
	- Rechenpower, (Speicher-)Kapazitäten, 
	  (Netzwerk-/ interne) Verbindungen
### Geographical Scalability
- Probleme:
	- Latenzprobleme
	- WAN links are unreliable --> TCP
	- fehlende Multipoint Kommunikation
### Administrative Scalability
> Conflicting policies concerning usage (and thus payment), management, and security

- Beispiel: 
	- Computational grids: share expensive resources between different domains.
	- Shared equipment: how to control, manage, and use a shared radio telescope constructed as large-scale shared sensor network?
- Ausnahme: Peer-to-Peer Netzwerke

### Scaling
- vertikale Skalierung
	- Upgrade des aktuellen Systems --> besserer RAM, CPU, mehr Speicher
- horizontale Skalierung
	- Erweitern des aktuellen Systems --> neue Computer an das System anbinden

#### Techniques for scaling
- Hide communicaiton latencies
	- asynchrone Kommunikation
		- nicht-blockierend
	- unterschiedliche Handler für Incoming-Responses
	- Nicht für alle Applikationen geeignet
- Aufteilen von Daten und Berechnungen
	- Auslagern der Berechnung an die Clients
	- Decentralized naming services (DNS)
	- Decentralized information systems (WWW)
- Replikation und Caching
	- Kopien auf mehreren Geräten bereitstellen
	- Inkonsistenzen behandeln & Synchronisierung beachten

## Klassifikation von verteilten System
- Parallel Computing
	- Multi-Prozessor & Multi-Core: geteiltes Memory
	- Multi-Computer: eigenes Memory
- Cluster Computing
	- Homogene Struktur: Selbes OS, fast gleiche Hardware
	- ![[Cluster Computinh.png]]
- Grid computing
	- Heterogene Struktur
	- (Zusammenfassung mehrerer Cluster)
	- geografische Verteilung

## Enterprise Application Integration
![[Pasted image 20240414120213.png]]

## TPM: Transaction Processing Monitor
![[Pasted image 20240416103911.png]]
- TP Monitor = Verantwortlich für die Koordination der Ausführung von Transaktionen auf unterschiedlichen Servern

## Middleware
![[Pasted image 20240416104130.png]]
- RPC (Remote Procedure Call):
	- Aufruf einer lokalen Prozedur
	- Verpacken als Nachricht
	-  Verarbeitung
	- Antwort als Nachricht
	- Ergebnis als `return` vom Aufruf
- MOM (Message Oriented Middleware)
	- An logischen Kontaktpunkt senden (Publish)
	- Weiterleitung an `subscribed` Applications (Subscription)

## Wie integriert man Applikationen
- Dateiaustausch
- Geteilte Datenbanken
- RPC
- Messaging
	- Voraussetzung für RPC: Aufrufer und Aufgerufener müssen zeitlich synchronisiert sein
	- Voraussetzung hier: entfällt, entkoppelt

## Verteilte, allgegenwärtige Systeme
- verteilte Systeme mit kleinen, mobilen Nodes die in einem großen System integriert sind
- Charakteristisch: Integriert sich fließend in die Umgebung des Nutzers
- Stichwort: **Internet of Things**
- überlappende Subtypen:
	-  Ubiquitäre Computersysteme: 
		- ständige Aktion zwischen System und Nutzer
		- Kernelemente:
			- Verteilung
				- Geräte sind vernetzt und verteilt
			- Interaktion
				- Interaktion zwischen Nutzern und Geräten
			- Context Awareness
				- System kennt den Kontext des Nutzers
			- Autonomie
			- Intelligenz
				- System kann viele Aktionen und Interaktionen handhaben
	- Mobile Computing Systeme: 
		- Geräte sind von Natur aus mobil
		- Geräte verändern ihre Position --> Discovery
		- Probleme mit instabilen Verbindungen
		- Verbindung zu Servern --> Cloud Computing
	- Sensor- (und Aktuator-) Netze: 
		- Erfassen und Interaktion (mit) der Umgebung
		- Eigenschaften:
			- viele Sensoren
			- Einfacher Aufbau (kleine Memory- / Rechen- / Kommunikationskapazität)
			- oft Batterie betrieben (oder Batterielos)

# Architektur
Aufbau eines Styles:
- (replaceable) components With well-defined interfaces
- the way that components are connected to each Other
- the data exchanged between components
- how these components and connectors are jointly configured into a system

Connector:
- Mechanismus zur Vermittlung der Kommunikation, Koordination oder Kooperation unter Komponenten.
- Beispiel: Facilitites für (Remote) procedure call, Messaging oder Streaming

## Layered Architecture
![[Pasted image 20240416111621.png]]
- Request / Response downcall = ähnlich zu ISO/OSI
- One-way Call = Wie Request / Response downcall mit Skipppen von Layers
- Down & Up calls = Erlauben von Upcalls

### Protokoll, Services und Interfaces
![[Pasted image 20240416112028.png]]
- Interface = Schnittstelle für das Layer darüber
- Service = Funktion eines Layers
- Protokoll = Kommunikation zwischen 2 Systemen auf dem gleichen Layer

## Two-party communication
```python
s = socket(AF_INET, SOCK_STREAM)
```
- `AF_INET` = Internet-Socket
- `SOCK_STREAM` = TCP-Socket
- `SOCK_DGRAM` = UDP-Packet

## Three-layered View
- Application-interface layer
- Processing layer
- Data layer

## Application Layering
![[Pasted image 20240416113346.png]]

## Service-oriented Archtecture (SOA)
![[Pasted image 20240416113504.png]]
- Komponenten = Objekte, verbunden durch Procedure Calls
	- können auf unterschiedlichen Maschinen sein
- Encapsulation = Objekte halten ihre Daten selbst und machen diese nur über Methoden zugänglich
![[Pasted image 20240416113953.png]]

## Resource-based (RESTful) Architectures
- Verteiltes System als eine Kollektion von Ressourcen, die individuell von Komponenten gemanaged werden
	- Ressourcen sind identifizierbar durch ein einziges naming scheme
	- All services offer the same interface
	- Messages von einem Service sind selbsterklärend
	- Komponenten vergessen alles über einen Aufrufer nach Erledigung der Aufgabe

## Publish-Subscribe Architecture
![[Pasted image 20240416114703.png]]
- zeitliche Kopplung:
	- wird vorgehalten (Mailbox)
	- wird verworfen (Direct) wenn Kommunikationspartner nicht erreichbar
- referentielle Kopplung:
	- gekoppelt: direkte Nachricht
	- entkoppelt: zur Verfügung stellen einer Information (für alle)
- topic-based subscription = bspw. `device.temperature`
- content-based subscription = Inhalt der Nachricht, bspw. alle Nachrichten mit `°C` als Inhalt --> ernsthafte Skalierungsprobleme, weil Blick in die Nachrichten notwendig ist

## Middleware
![[Pasted image 20240416120242.png]]
- enthält häufig genutzte Komponenten und Funktionen die nicht separat von den eigentlichen Applikationen implementiert werden müssen.

### Wrapper / Adapter und Broker
- Wrapper = Schnittstelle zu einer Applikation
- Broker = Vereinigung von Schnittstellen an einen zentralen Punkt
	- Ziel: Reduzierung / Vereinheitlichung von Wrappern
![[Pasted image 20240422170714.png]]

## Interceptor
- Unterbrechung des eigtl. Aufrufes durch den Aufruf einer weiteren Funktion (`Interceptor`) zur Vorbereitung, Authentifizierung, Logging oder sonstiges Funktionen

## Layered Architecture 2
### Basic Client-Server Model
![[Pasted image 20240416121650.png]]
- Servers = Bereitstellung von Services
- Clients = Nutzen von Services

### Multi-tiered centralized system architectures
![[Pasted image 20240416122008.png]]

### Three-tiered Architecture
- Client und Server zur selben Zeit:
![[Pasted image 20240416122139.png]]
- AS = Applicaiton Server
- DS = Database Server
- CGI = Common Gateway Interface

## Alternative Organisationen
- Vertikale Verteilung 
	- Aufteilung einer Applikation in 3 logische Layer
	- Layer werden auf unterschiedlichen Servern ausgeführt
- Horizontale Verteilung
	- Client oder Server kann physisch in mehrere logische equivalente Teile geteilt werden
	- Jeder Teil arbeitet auf eigenen Ausschnitt der Daten
- Peer-to-Peer Architekturen
	- Prozesse sind alle gleich
	- Prozesse sind Client und Server zugleich 

# Processes
## Threads
- virtuelle Prozessoren in Software, basierend auf physischen Prozessoren
	- Prozessor: Bereitstellung von möglichen Instruktionen mit der Möglichkeit die automatisch ausführen zu können
	- Thread: minimaler Software Prozessor in dessen Kontext eine Serie von Instruktionen ausgeführt wird. Wird der Kontext eines Threads gespeichert, wird dieser gestoppt und dessen Daten gespeichert für die Ausführung in einer weiteren Stage. 
	- Prozess: Software Prozessor in dessen Kontext mehrere Threads ausgeführt werden können.
- Vorteile:
	- avoid needless blocking
	- exploit paralellism
	- avoid process switching
### Context
- Process context: The minimal collection of values stored in registers and memory, used for the execution of a thread (i.e., thread context, but now also at least MMU register values).
	- MMU = Memory Management Unit
- Processor context: The minimal collection of values stored in the registers of a processor used for the execution of a series of instructions (e.g., stack pointer, addressing registers, program counter).
- Thread context: The minimal collection of values stored in registers and memory, used for the execution of a series of instructions (i.e., processor context, State).

## Threads in Distributed Systems
- Dispatcher / Worker Model:
	- Verteilung von Aufgaben einer Request / mehrerer Requests auf verschiedene Worker Threads
![[Pasted image 20240416124634.png]]

## Processes on the Server Side
### Object Servers
![[Object_Servers.png]]
- Activation Policy: Ausführen unterschiedlicher Schritte abhängig von der aufrufenden Anfrage
	- Wo sind der Code und die Daten des Objekts?
	- Welches Threading-Modell soll verwendet werden?
	- Soll der veränderte State des Objektes behalten werden?
- Object Adapter:
	- Implementierung einer spezifischen Activation Policy
### Server Clusters: Three different tiers
![[Server Clusters.png]]
- First Tier: Verteilen von Anfragen - Request Dispatching

### Request Handling
- Kommunikation (hin und zurück) nur im First Tier: mögliches Bottleneck
- mögliche Lösung: TCP handoff
![[Pasted image 20240419094533.png]]

### When servers are spread across the Internet (Wide Area Clusters)
- Bei Servern mit mehreren IP-Adressen Verteilung der Anfragen über DNS an nächstgelegenen Server
- DNS behält Replikas im Blick
- siehe: Content Delivery Networks und Akamai Edge DNS
![[Akamai_CDN.png]]

### Middleware Layer
- Bereitstellung von allgemeinen Services und Protokollen für unterschiedliche Applikationen:
	- Kommunikationsprotokolle
	- (Nicht-)Zusammenführung von Daten, die für integrierte Systeme erforderlich sind
	- Naming Protokolle
	- Sicherheitsprotokolle
	- Scaling Mechanisms

### An Adapted Layering Scheme for Communication in Distributed Systems
![[Pasted image 20240419103555.png]]

### Types of communication
#### Persistent vs. Transistent communication
- Persistent:
	- Nachricht wird von Kommunikationsserver (Middleware) gespeichert so lange wie die Zustellung dauert
- Transistent:
	- Kommunikationsserver verwirft die Nachricht, wenn sie nicht zugestellt werden kann
#### Asynchronouns vs. Synchronous  communication
- asynchron:
	- Sender arbeitet nach Nachrichtenübermittlung weiter
- synchron:
	- Sender ist nach Nachrichtenübermittlung blockiert, bis die Anfrage angenommen wird
	- Stellen zur Synchronisation:
		- at request submission
		- at request delivery
		- Nach request processing

#### Client / Server
- Client Server Kommunikation: transient synchronous communication
	- Client & Server müssen aktiv sein während der Kommunikation
	- Client wird durch Anfrage blockiert solange er auf Rückfrage wartet und anschließend verarbeitet
	- Server wartet nur für eingehende Anfragen und 
- Nachteile synchroner Kommunikation:
	- Client kann nicht weiterarbeiten beim Warten auf die Antwort
	- Fehler müssen sofort behandelt werden
	- Modell kann nicht für alles geeignet sein (E-Mail, Nachrichten)

#### Messaging
- Message-oriented middleware
	- persistent asynchronous communication
	- Prozesse versenden Nachrichten aneinandner, die in einer Wartschlange aneinander gereiht werden
	- Sender muss nicht auf eine sofortige Antwort warten und kann andere Dinge bearbeiten
	- Middleware stehlt Fehlertoleranz sicher

#### RPC
- Basic RPC operation:
![[Pasted image 20240419110522.png]]
- Was muss bei der Übertragung von Parametern bei RPC beachtet werden?
	- Byte-Interpretation 
	- Unterschiedliche Daten Repräsentation (Little Endian / Big Endian)
	- Umwandlung von Parametern zu Bytesequenzen
	- Codierung
		- Representation von Basis-Datentypen (interger, float, character)
		- Representation von erweiterten Datentypen (Arrays, Unions)
