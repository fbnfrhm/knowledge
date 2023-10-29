## [[Entwicklungskonzepte|Kriterien für einen guten Entwurf]]
- [[Grundsatzentscheidungen|6 Metriken wären formulierbar]]

## Metriken für modulare Entwürfe
![[media/pi/modules/Systementwicklung/modulare_Entwuerfe.drawio.svg]]
### FAN-IN / FAN-OUT Metrik
#### FAN-IN
> Anzahl der Stellen, wo der Kontrollfluss in das Modul geht
> Anzahl globaler Variablen in Modul
- - **FAN-IN ist HOCH** ==> Hinweis auf hohe KOHÄSION

#### FAN-OUT
> Anzahl der Stellen, wo der Kontrollfluss aus dem Modul herausgeht
> Anzahl globaler Variablen, die das Modul ändert
- **FAN-OUT ist HOCH** ==> Hinweis auf hohe KOPPLUNG

## Metrik für Objektorientierte Entwürfe
### Kapselung
- Anzahl an (variablen) Attributen die keine Getter/Setter haben

### Tiefe des Ableitungsbaumes  
  ![](https://www.planttext.com/api/plantuml/png/SoWkIImgAStDuU9AJ2ekAKfCBb58paaiBbPGSYmjoLTII2nMSCGYbP89aJB4a7Fo3OT86N4vAjZeweBKG1b6N5mm0yoWsWtX8gPG4Q0sGwW-GmGJg9NB8JKl1UXI0000)
  ```c++
  void fkt(AUTO &a) {
  // ...
  // some code
  // ...
  }
  A5 a5; // Instanz von A5 erzeugen
  fkt(a5); // wird trotzdem ausgeführt, weil A5 [is A] AUTO
  ```

### Lack of Cohesion in Mehtods (LOCM)
- Anzahl von Methoden-Paaren, die keine gemeinsamen Daten verwenden
- skaliert auf die Anzahl an Methoden & Attributen
- _"Ist das was zusammengehört auch wirklich zusammen?"_  
![[media/pi/modules/Systementwicklung/LOCM.drawio.svg]]

1. Betrachten der Methodenpaare:

| Methoden | Status |
| :---- | :------- |
| m1 & m2 | <span style="color:green">✓ (Attribut 1 gemeinsam)</span>  |
| m1 & m3 | <span style="color:red">∅</span> | 
| m1 & m<mark style="background-color:red">4</mark> | <span style="color:red">∅</span> | 
| m2 & m3 | <span style="color:green">✓ (Attribut 4 gemeinsam)</span>  |
| m2 & m<mark style="background-color:red">4</mark> | <span style="color:red">∅</span> | 
| m3 & m<mark style="background-color:red">4</mark> | <span style="color:red">∅</span> |   

- LOCM(Klasse A) = 4  
- Methode 4 + v3 in separate Klasse