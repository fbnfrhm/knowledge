## IT-Sicherheitsgesetz
- SIEM-Systeme = Security Information and Event Management
		- Zentralisierung, Korrelierung, Analyse der Daten im gesamten System
		- Logverwaltung / -zentralisierung
## Meldepflichten kritischer Infrastrukturen
- „Störungen der Verfügbarkeit, Integrität, Authentizität und Vertraulichkeit ihrer informationstechnischen Systeme, Komponenten oder Prozesse, die zu einem Ausfall oder zu einer erheblichen Beeinträchtigung der Funktionsfähigkeit der von ihnen betriebenen Kritischen Infrastrukturen geführt haben, erhebliche Störungen der Verfügbarkeit, Integrität, Authentizität und Vertraulichkeit ihrer informationstechnischen Systeme, Komponenten oder Prozesse, die zu einem Ausfall oder zu einer erheblichen Beeinträchtigung der Funktionsfähigkeit der von ihnen betriebenen Kritischen Infrastrukturen führen können."
- Die Meldung muss unverzüglich, d.h. ohne schuldhaftes Zögern, erfolgen
- KRITIS-Unternehmen:
	- 1. den Sektoren Energie, Informationstechnik und Telekommunikation, Transport und Verkehr, Gesundheit, Wasser, Ernährung, Finanz- und Versicherungswesen sowie Siedlungsabfallentsorgung angehören und
	- 2. von hoher Bedeutung für das Funktionieren des Gemeinwesens sind, weil durch ihren Ausfall oder ihre Beeinträchtigung erhebliche Versorgungsengpässe oder Gefährdungen für die öffentliche Sicherheit eintreten würden.
- Das Melden eines IT-Sicherheitsvorfalls ist für einen Forensiker nicht verpflichtend. Er kann den Prozess aber anstoßen und mit Genehmigung durchführen. 
- Vorfälle sind nur meldepflichtig, sobald personenbezogene Daten oder eines der Schutzziele betroffen sind.

## Digitale Forensik
>„IT-Forensik ist die streng methodisch vorgenommene Datenanalyse auf Datenträgern und in Computernetzen
   zur Aufklärung von Vorfällen unter Einbeziehung der Möglichkeiten der strategischen Vorbereitung insbesondere aus der Sicht des Anlagenbetreibers eines IT-Systems. “

- Ziele der forensischen Analyse:
	- Identifikation des Angreifers
	- Erkennen der Methode
		- Sicherheitslücke schließen
	- Ermittlung des Schadens
		- relevant für Versicherung und Strafverfahren
		- Ermittlung des Ausmaßes
	- Sicherung der Beweise
		- relevant für Strafrecht, Dokumentation und Nachweis
- Multimedia-Forensik:
	- Auswertung von Bildern & Videos
	- Detektion von Manipulationen
	- Detektion von Personen anhand von Laufverhalten
- Herausforderungen
	- Datenmenge
	- Zeit (Entdeckung eines Vorfalls)

### Digitale Spuren
- Spuren...
	- materielle Veränderungen an Personen oder Objekten
	- stehen im Zusammenhang mit relevanten Ereignissen
	-  können zur Tataufklärung beitragen, da sie Rückschlüsse auf den Tatablauf und den Täter geben
- Digitale Spuren...
	-  basieren auf Daten, welche in Computersystemen gespeichert sind oder übertragen wurden
	- … werden erst durch ihre Interpretation von physischen Spuren über unterschiedliche Interpretationsebenen zu verwertbaren Spuren
- Es gibt keinen Tatort ohne Spuren!

### Locard'sche Prinzip
![[Locardsches Prinzip.png]]
- Alles / Jeder / Immer hinterlässt Spuren!
- Alles kann Spuren enthalten

### Einordnung
- Modell
	- genereller Ablauf einer Untersuchung
- Prozess
	- detaillierter Ablauf einer Untersuchung
	- Reproduzierbarkeit
- Methode
	- Herunterbrechen der Schritte auf Werkzeuge oder verwendete Tools

### Der forensische Prinzip
- Anforderungen an die Vorgehensweise:
	- Akzeptanz : Methoden sind in der Fachwelt anerkannt
	- Glaubwürdigkeit: Funktionalität der Methoden ist nachweisbar
	- Wiederholbarkeit: Ergebnisse ist durch Dritte reproduzierbar
	- Integrität: Spuren werden durch Untersuchung nicht verändert
	- Ursache und Auswirkungen: Verbindung zwischen digitalen Spuren, Ereignissen und Personen sind herstellbar
	- Dokumentation: Ermittlungsprozess ist nachvollziehbar dokumentier

## Forensic Readiness
> ...  beschäftigt sich mit Maßnahmen zur Vorbereitung auf digitale forensische Untersuchungen innerhalb Organisationen

- Ziele der Forensic Readiness
	- Systeme sollen in der Lage sein, bessere und belastbarere digitale Spuren zu sammeln
	- Die Kosten für eine forensische Untersuchung sollen verringert werden

- technische Maßnahmen: Konfiguration für umfangreiches Logging zur vereinfachten Analyse des Systems
### Dimensionen 
- Grundlage:
	- rechtlich
- Maßnahmen & Methoden:
	- personell 
	- technisch
	- organisatorisch

### forensischer Arbeitsplatz
- 3 Rechner für unterschiedliche Aufgaben
	- Forensische Workstation
		- bessere HW auf aktuellem Stand der Technik
		- Dualboot 
		- Virenscanner und Firewall
	- Office Computer für Schriftsachen
		- Verschlüsselung notwendig
		- Interne Netzwerkanbindung, kein Internetzugang!
	- Internet Computer
		- keine sensiblen Daten eingeben oder speichern
		- Aktuelle Anti-Viren-SW
		- auch als VM einsetzbar!

## Datensammlung
- Vorauswahl an geeigneten Werkzeugen für ausgewählte Datenquellen treffen
- eigene Forensik-Datenträger: von Daten aus früheren Vorgängen "säubern
- Forensisches Duplikat der Daten erstellen
- Integrität der Beweiskette sichern und somit Sicherung der Beweiskraft!

### Beweisführung im Zivil- oder Strafverfahren
- Die Sicherung von digitalen Beweisspuren kann auf zwei Arten geschehen:
![[Beweisführung.png]]

### Post Mortem Forensics
- Physikalsiche Ebene
- Datenträgerkopie

| Vorteile                             | Nachteile               |
| ------------------------------------ | ----------------------- |
| Vollständiges Abbild                 | Datensicherungsdauer    |
| Virtualisierung nachträglich möglich | Größe                   |
| Formatwandelbarkeit                  | Externe Spezialhardware |

- Wie und wohin?
	- Schreibgeschützt extern auf extern
	- Schreibgeschützt intern auf extern
	- Live Boot CD / USB

### Live Forensik
- Dateien
- gelöschte Daten?
- Datenbanken
- Cloud Speicher
- Entschlüsselte Inhalte
- RAM
- Netzwerkverbindungen

| Vorteile                     | Nachteile                 |
| ---------------------------- | ------------------------- |
| Schnell und effizient        | Veränderung am System     |
| geringe Größe                | Selektierter Datenbestand |
| Ohne externe Spezialhardware | Formatauswahl             |
| Sicherung flüchtiger Daten   |                           |
- Wie und wohin?
	- logisch / physikalisch selektiv
	- Externe Datenträger / Netzwerk

### Sicherung digitaler Beweismittel und Spuren
- keine Veränderungen am System + Dokumentation
- forensische Untersuchungen müssen nachvollziehbar und reproduzierbar sein!

### Analyse digitaler Beweismittel
- mögliche forensische Methoden
	- Wiederherstellen gelöschter Objekte
	- Hashwertüberprüfungen
	- File Carving
		- Untersuchung von Dateien anhand der reinen Dateiinformationen / -daten, ohne Verwendung des Betriebssystems
	- Textsuchen
	- Slack-Untersuchungen
		- Chatverläufe und Co. untersuchen

# Wiederholung I
- Schreibschutzadapter
	- HW-Bauteil, das nur einen Lesezugriff auf das angeschlossene System ermöglicht, verhindert eine Veränderung der Daten auf ebendiesen.
- Post-mortem Forensik
	- Analyse von Datenträgern, derer Trägersystem nicht mehr läuft. Bspw. über Live USB Stick
- Live Forensik
	- Analyse auf aktivem System, Analyse & Sicherung von flüchtigen Daten, Umgehen möglicher Sicherheitsmaßnahmen (Anmeldung + Verschlüsselung)
- Forensic Readiness
	- Vorbereitung eines Systems zur Erleichterung der Analyse, Konfiguration von Logging
- Digitale Spuren
	- Veränderungen / Hinterlassenschaften an physischen / virtuellen Objekten
	- Auswertung von Daten auf zu untersuchenden Geräten und Netzwerken, können teilweise flüchtig sein
- Locard'sche Prinzip
	- Jede Interaktion hinterlässt Spuren
	- kein Tatort kann ohne Spuren von Täter / Opfer / Anderen verlassen werden
- S-A-P-Modell
	- Secure: Daten sichern & Erfassen
	- Analyse: Auf die relevanten Daten spezifizieren, analysieren und Fehler / Probleme / Spuren finden
	- Present: Rückschlüsse darstellen und dokumentieren
- Dunkelfeld
	- nicht-gemeldete Vorfälle, aus Angst vor Konsequenzen (Prestigeverlust) oder für die schnellere Lösung
- Multimedia-Forensik
	- Analyse von Multimedia-Inhalten (Bilder / Videos)
	- Erkennen von Manipulation, Personen, etc.

# ISO 27037
- Grundsätze der digitalen Beweisführung:
	- Relevanz
	- Vollständigkeit
	- Verlässlichkeit
- Grundlegende Aspekte bei der Bearbeitung von digitalen Beweismitteln:
	- Auditierbarkeit
	- Wiederholbarkeit
	- Begründbarkeit
	- Reproduzierbarkeit

## Prozess zur Handhabung von digitalen Beweismitteln
1. Überblick
	- Welche Beweise gibt es?
2. Identifikation
	- Physischer und logischer Beweis
3. Mitnahme (oder Sicherung)
	- Entscheidung / Beachtung der Systemzustände (an / aus)
	- Kosten- & Zeitfaktor beachten
1. Sicherung (oder Mitnahme)
	- Ausreichend Kopien
2. Erhaltung
	- Schreibschutzadapter
	- Hash-Werte
- Dabei sollten die Veränderungen der Beweise auf ein Minimum beschränkt werden

## Obhutskette
- Prozess der Beweismittelübergabe an Weitere muss dokumentiert werden:
	- eindeutige Beweismittelkennzeichnung
	- Wer hat wann was mit dem Beweismittel gemacht?

## Grundregeln für das Verhalten am Tatort
- ruhig und überlegt vorgehen
- je unklarer die Lage, desto weiträumiger die Sicherung
- Einsatzfahrzeuge nicht an unmittelbaren Tatort bringen
- nur Ausrüstung/persönliche Dinge an den Tatort bringen, die benötigt werden
- keine Einrichtungen am Tatort nutzen
- nicht essen, trinken, rauchen!
- grundsätzlich nichts anfassen, verändern, verlegen etc.
- Kontaminationen vermeiden
- keine eigenen Spuren hinterlassen
- erforderliche Veränderungen markieren und dokumentieren

## ISO 27037  Vorkehrungen am Untersuchungsort
- Allgemeine Schritte:
	- Sichern und Kontrollieren des Bereichs, in dem sich die Geräte befinden
	- Bestimmung der Person, die für den Ort die fachliche Verantwortung trägt
	- Sicherstellen, dass Personen von den Geräten und von der Stromversorgung ferngehalten werden
	- Alle Personen dokumentieren, die Zugang zum Ort haben oder für die ein Motiv für eine Beteiligung am Untersuchungsort vorliegen könnte
	- Ist das Gerät eingeschaltet, darf das Gerät nicht ausgeschaltet werden und umgekehrt, falls das Gerät ausgeschaltet ist, darf es nicht eingeschaltet werden
	- Untersuchungsort mit allen Komponenten und Kabeln in seiner ursprünglichen Position dokumentieren
	- Falls zulässig: Bereiche nach Gegenstände, wie Haftnotizen, Terminkalender, Akten, Laptops oder Handbücher für Hard- und Software durchsuchen
- Personal:
	- Sind Personen, gegen die ermittelt wird, anwesend? Falls ja, sind sie gewaltbereit?
	- Zu welcher Tageszeit erfolgt der Einsatz?
	- Kann der Untersuchungsort vor unbeteiligten Dritten abgeschirmt werden?
	- Befinden sich Waffen in diesem Bereich?
	- Bestehen objektive Risiken für anwesende Personen?
	- Könnte irgendetwas in der Nähe, einschließlich des Gerätes, so konfiguriert worden sein, dass es zu Körperverletzungen führen kann, falls es auf unangemessene Weise bearbeitet wird, z. B. versteckte Falle?
	- Ist es wahrscheinlich, dass das zu sammelnde Beweismaterial psychische Schäden oder eine anstößige Wirkung hervorruft?
	- Kann der Untersuchungsort als unsicher betrachtet werden?
- Potentielle digitale Beweismittel:
	- Risikobeurteilung durchführen und folgende Fragen stellen:
		- Welche Art von Mitnahme-/Sicherungsmethode wird angewendet?
		- Welche Ausrüstung wird möglicherweise vor Ort benötigt?
		- Inwieweit sind die Daten und Informationen im Hinblick auf die potentiellen digitalen Beweismittel flüchtig?
		- Ist ein Fernzugriff auf irgendein digitales Gerät möglich und stellt er eine Bedrohung für die Beweismittelintegrität dar?
		- Was passiert, wenn der Datenbestand beschädigt ist?
		- Könnte der Datenbestand beeinträchtigt worden sein?
		- Könnte das digitale Gerät so konfiguriert worden sein, dass Daten zerstört (z. B. eine sogenannte „Logik-bombe"), vereitelt oder verschleiert werden, wenn das Gerät ausgeschaltet wird oder ein unkontrollierter Zugriff darauf erfolgt?

## ISO 27037 – Computer, Peripheriegeräte und digitale Speichermedien 
- Identifikationsphase
	- zusätzliche Informationen zur Erleichterung des weiteren Untersuchungsprozesses sollten berücksichtigt und dokumentiert werden, z.B. Passwörter, Handbücher, etc.
		- Informationen dürfen von den Verantwortlichen erfragt werden
- Mitnahme
	- eingeschaltete digitale Geräte:
		- ![[Mitnahme_eingeschalteter_Geräte.png]]
		- Verschlüsselung beachten
		- ![[Mitnahme_digitaler_Geräte_Live_Daten.png]]
	- ausgeschaltete digitale Geräte:
		- ![[Mitnahme_ausgeschaltete_Geräte.png]]

## Besonderheiten
- Totmannschaltungen
	- Bluetooth, NFC, USB-Sticks, etc.
- Verschlüsselungen
	- Bitlocker, VeraCrypt
- Online Connections / Speicher
	- Cloud-Verbindungen (Dropbox, iCloud, MagentaCloud)
	- Remote Verbindungen

# Ransomware
- Ransomware gibt dem Angreifer häufig Zugriff auf die Daten und schränkt die Verfügbarkeit ein
- Meldepflichtig sobald Abfluss personenbezogener Daten

# Incident Response - Technisches Vorgehen
- Keine Anmeldung auf potenziellen infizierten Systemen mit Administratorkonten
- Erste wichtige Maßnahmen:
	- Validierung aller Accounts!
	- Prüfen von Netzwerkmitschnitten auf ungewöhnlichen Netzwerkverkehr
	- Für Analyse des Angriffs notwendige Daten sichern
- Stichwörter: Forensische Images, Speicherabbilder, Netzwerkmitschnitte

# Bereinigung
- alle kompromittierten Systeme gleichzeitig vom Netz nehmen
- Alles neu aufsetzen und Zugangsdaten ändern

# Dokumentation
- Best Practices
	- Die Urkopie wird archiviert und an den anderen Kopien wird gearbeitet.
	- Handschriftlich dokumentieren
- Was sollte dokumentiert werden?
	- Welche Schritte wurden durchgeführt?
	- Wer war wann anwesend und was hat derjenige gemacht?
	- Auffällige Reaktionen der Anwesenden!
	- Skizze der vorgefundenen EDV Netzwerke
- manuelle und maschinelle Datensicherung möglich:
	- Protokoll der maschinellen Datensicherung anhängen
	- Seriennummern notieren
- Kennzeichen eines aussagekräftigen Forensik-Gutachtens:
	- Formulierung des konkreten Untersuchungsgegenstandes
	- Definition von (potenziell missverständlichen / unklaren) Fachbegriffen
	- Ggf. Formulierung getroffener Annahmen
	- Zusammenfassung der wichtigsten Untersuchungsergebnisse
	- Detaillierte Untersuchungsergebnisse
- Keine darüber hinaus gehenden Arbeiten durchführen, da ansonsten Gefahr der Befangenheit