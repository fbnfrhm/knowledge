- für Admins
- Aufteilung der verschiedenen Funktionen auf Knoten eines Netzwerkes  
![[media/pi/modules/Systementwicklung/phys_Schicht.drawio.svg]]
## Architektur-Muster für die strukturelle Sicht
- zentrales System
- Client-Server
- Föderation
- Konfigurationsdiagramme

### zentrales System
![[media/pi/modules/Systementwicklung/zentrales_System.drawio.svg]]
- z.B. Kassensystem, Linux + SSH, klassischer Großrechner

### Client-Server
![[media/pi/modules/Systementwicklung/Client-Server.drawio.svg]]

#### Clients
| THIN Clients | THICK / (FAT) Clients | 
| :------ | :------ |
| nur UI | mehr eigenständige Aufgabenabarbeitung |
| "Server Scrapping" (RDP, VNC) | Serverentlastung |

##### ÜAfg - 1
1. FAT-Clients
2. Datenserver
3. MPI möglich (MPI = Message Parsing Interface)
4. Cloud Computing  

--> Gesucht ist eine System-Entwurfsidee in PlantUML

Lösung:
![](https://www.planttext.com/api/plantuml/png/VP11QiCm44NtSugFzrxOtfLG4cGCNHGAwGMKU6gBMfAHne5ISfFUfXUhB1TAe6GrywNt_qYpZwA3B7OYCJ8nYawVZ7ReWXujIdn_7Tw6L9zVdWgAxyRDEcYBoJYMZvdXWuoUnCyGZvCNyHQz2NmMuntHscWtvE33AzHas4aie2CwXKz2iWqi8uSiW7yDg3P7TGUfDwI-WpGRqYJaIjURnxLQs4KE5muPQezqdlpIer2vA6_dHOmRygrIH5s5NLa-feaFwtB-TFEhwrjDwR_v84MtnwrTS_Ri-dNzFm00)

```plantuml
@startuml

title "Fabian Frahm - ÜAfg - MPI"
skinparam linetype ortho
top to bottom direction

rectangle "FAT Clients" as FC {
  together {
    rectangle "FAT Client 1" as F1
    rectangle "FAT Client 2" as F2
    rectangle "FAT Client 3" as F3
  }
}

rectangle "Datenserver" as DS
cloud "Cloud Computing" as CC

F1 <--> F2: MPI
F1 <--> F3: MPI
F2 <--> F3: MPI

FC <--> DS
DS <--> CC

@enduml
```

#### Message Parsing Interface
![[media/pi/modules/Systementwicklung/MPI.drawio.svg]]

#### Three Tier Client Server
![[media/pi/modules/Systementwicklung/Three_Tier_CS.drawio.svg]]

### Föderation
- gleichberechtigte Partner (Peer-to-Peer-NW)
- Subsysteme die miteinander Kommunizieren  
![[media/pi/modules/Systementwicklung/Föderation.drawio.svg]]
- Anzahl der Verbindungen:  
  $\frac{n*(n-1)}{2}=\text{Anzahl der Verbindungen}$  
  $n = \text{Anzahl der Knoten}$

#### ÜAfg - 2
![[media/pi/modules/Systementwicklung/UE_Foederation.drawio.svg]]  
- 14 Teilnehmer-Programme  
- Aufgabe:
	- Darstellung in PlantUML
	- Vermeidung von 91 Konvertern (aka Verbindungen)

Lösung - 1:  
![](https://www.planttext.com/api/plantuml/png/TPHDReCm48NtFeN5daKWowfAe8hK1N8avm8kSS4AsCYOHbMLc_GslLZ79lm3iWIyzs4FRmo7sZ1jch90o0XJSEoTs8TW4fyqoqliux_VusS6vxDMr-PcX9Br5zTtLfX6PXwgRq9MJBCI5q9oyrrnhBJ95KAQfuR9p4uP7zyy_8CmDYhZ9kVQtKm1kq26TnvcDORRtGOGT42m0OGT46u0-mxO0_1OG3xb6bwmXUmr431iIVZ5lwgxz5zxmzQngeQhwdwkFf0xHXMGoeYRMvmi4vlKwiXdO6ItxhPfaM3TRQCYuPfRfpd74OUJI7FNQiT6oypSNEFKo90Q6MNMoIHOqS8LBPfhZsbML9HDmUoEjAlI-Pu2UrmLVKwx7UW5r59X-fwu1ovq3iIiI7ixNjZ35z93vmL4q_mkP0Q1zX1Dy9nAb3GiuyvEPkQuATRlMWBZGY6ofeB0khUD5yfveS3wCsKXH5C16k7sBwXzSyWWj10TX7QpemENL_ZJ_0C0)
```plantuml
@startuml

title "Fabian Frahm - ÜAfg - Produktionsverwaltung"
skinparam linetype ortho

rectangle "CAD" {
  together {
  rectangle "CAD Prog 1" as CAD1
  rectangle "CAD Prog 2" as CAD2
  rectangle "CAD Prog 3" as CAD3
  rectangle "CAD Prog 4" as CAD4
  }
  rectangle "CAD-Server" as CServ
  
  CAD1 <-down-> CServ
  CAD2 <-down-> CServ
  CAD3 <-down-> CServ
  CAD4 <-down-> CServ
}





rectangle "Optik" as O {
  together {
    rectangle "Optik 1" as O1
    rectangle "Optik 2" as O2
    rectangle "Optik 3" as O3
    rectangle "Optische Beschichtung" as OB
  }
  rectangle "Optik-Server" as OServ
  
  O1 <-down-> OServ
  O2 <-down-> OServ
  O3 <-down-> OServ
  OB <-down-> OServ
}



rectangle Simulation as S {
  rectangle "Sim-Server" as SServ
  together {
    rectangle "Thermo SIM" as TS
    rectangle "Calc SIM" as CS
    rectangle "Produktion SIM" as PS
    rectangle "Schwingung SIM" as SM 
    rectangle "Montage" as M
    rectangle Beschichtung as B
  }
  
  TS <-up-> SServ
  CS <-up-> SServ
  PS <-up-> SServ
  SM <-up-> SServ
  M <-up-> SServ
  B <-up-> SServ
}

CServ <--> OServ
OServ <--> SServ
SServ <--> CServ

@enduml
```


Lösung - 2:
![](https://www.planttext.com/api/plantuml/png/TPDBReCm48RtFiM8FOiybbMLHnMf2-H8pWKSue85sCWCYQegD-bjUh7waH0K1mbaFF_7p3z-h3ha1lkc9WGbrWAI7JzAhc1dUDb02d-_ww_2ZdkZJts5KglkBCo5rzYh8Y5T9LNB3M-WbahWToj06omrGTq2QZXgHDt0IHgHkvzj6Lq8B8M17mBWebmLhkvs_P7us7FKbIvWbW3lm4vdayZyZimdaSKTMKmYopkojCZLliCpeccBil8WZJrxyMQOHdQ36hpIo6bGWqqQcNHgbvS2Di8ECY_z9dXsC-sMoQQlkLjzHxBOyC5kHwE1VMO-ru55YyFhV92taVmu6mEqZo2MbnUf2cjuW5W6prIc5V92U3bx4iTDEpsqV2LarAemvvT7AmtAhG7x_M8_nmoD6RkCOu9vmbPt9-SjJTzlUMcOX0GiJ09BF32MwICG4FO8X6na9TJ9Niz_)

```plantuml
@startuml

title "Fabian Frahm - ÜAfg - Produktionsverwaltung"
skinparam linetype ortho
top to bottom direction

together {
  rectangle "CAD" {
    rectangle "CAD Prog 1" as CAD1
    rectangle "CAD Prog 2" as CAD2
    rectangle "CAD Prog 3" as CAD3
    rectangle "CAD Prog 4" as CAD4
  }
  
  
  
  rectangle "Optik" as O {
    rectangle "Optik 1" as O1
    rectangle "Optik 2" as O2
    rectangle "Optik 3" as O3
    rectangle "Optische Beschichtung" as OB
  }
  
  
  
  rectangle Simulation as S {
    rectangle "Thermo SIM" as TS
    rectangle "Calc SIM" as CS
    rectangle "Produktion SIM" as PS
    rectangle "Schwingung SIM" as SM 
    rectangle "Montage" as M
    rectangle Beschichtung as B
  }
}

rectangle Server {
  rectangle "CAD-Server" as CServ
  rectangle "Optik-Server" as OServ
  rectangle "Sim-Server" as SServ
}

CAD <--> CServ
O <--> OServ
S <--> SServ

CServ <--> OServ
OServ <--> SServ
SServ <--> CServ

@enduml
```
### Konfigurationsdiagramme 
- weit verbreitetes Hilfsmittel zur Beschreibung von Systemkomponenten
- <span style="color:red">nicht UML!</span> (teilweise von PlantUML-Programm unterstützt)  
![[media/pi/modules/Systementwicklung/Konfigurationsdiagramm.svg]]
