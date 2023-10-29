## XML (Extensible Markup Language)
- Datenaustauschformat
- Metasprache, um Datentypen zu definieren
- Hierachie von Containern
```xml
<dhge>
	<paket>
		Hallo Welt!
	</paket>
</dhge>
```
- jedes Element kann Attribute besitzen
```xml
<dhge language="de"></dhge>
<dhge language="en"></dhge>
```
- physische Struktur is OK (Syntax) => <span style="color:red">XML ist wohlgeformt!</span>
- Semantik (logische Struktur) ist OK => <span style="color:red">XML ist valide!</span>
	- SCHEMA (Strukturplan der XML-Datei)
		- Standardtypen
		- Definition von eigenen Daten (Datenstrukturen)
		- Namensräume sind verwendbar & eigene sind definierbar
		- Vererbung
### Tag-basiertes XML
```xml
<dhge schema="1.1">
	<Name>Kasche</Name>
	<ID>1715</ID>
</dhge>
```

### inhaltsbasiertes XML
```xml
<dhge schema="1.1">
	<Property Bezeichnung="Name">
		<value type="string">
			Kasche
		</value>
	</Property>

	<Property Bezeichnung="ID">
		<value type="string">
			G1715
		</value>
	</Property>
</dhge>
```
- höherer Schreibaufwand
- keine äußere Änderung des Schemas

## JSON (JavaScript Object Notation)
- Hierachien von Containern (Objekten)
	- Objekt {}
	- Array \[\]
	- string
	- number (real)
	- bool
	- null
- Key-Value-Paare: `"key":"value"`
- Beispiel
```json
{
	"Name":"Kasche",
	"ID": 1715
	"dhge": [{},{}]
}
```
- Vorteil: manuelles Festlegen meiner Daten
- Nachteil: standardmäßig kein Schema 

## CSV-Datei
- Comma-Seperated-Values
- einfach strukturierte Daten
- es gibt keinen allgemeinen Standard (RFC)
- Trennzeichen unterschiedlich `,.;`