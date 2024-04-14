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
- Intermittent Fault = sich wiederholender Fehler
	- temporär, tritt in Intervallen auf
- Permanent Fault = permanenter Fehler
#### On Security
- Confidentiality, Integrity
- Authentication, Authorization, Trust
- Verschlüsselung, Hashing 
![[digital_signatures.png]]
- Achtung $H$ = Hash-Algorithmus

### Scale in distributed systems
#### Size scalability 
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

![[Pasted image 20240414120213.png]]

# Foliensatz 4

# Foliensatz 5

# Foliensatz 6
