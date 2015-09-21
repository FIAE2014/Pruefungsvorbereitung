# FIAE Kompendium Cheat-Sheet zur Prüfung

Inhalte werden anhand alter Prüfungen erstellt!

## GA2

## Hardware

### Speicher

*F* : Vorteile und Nachteile *SSD* gegenüber *HDD*
*A* : 
* Vorteile:
    - Schneller als HDD (Faktor 50-200 %)
    - Erschütterungsunempfentlich
    - Weniger Platz bedarf im Gehäuse da meist 2,5" Normgröße
* Nachteile:
    - Kosten sind deutlich größer
    - Weniger Schreibzyklen als HDD

*F* : Whats *SATAe*?
*A* : 
- Externe SATA Schnittstelle
- 6 Gbit/s Bandbreite
- Unterstützt SATA und PCIe Speicher
- PCIe untersützt mehrere Versionen und meherer PCIe Lanes

#### RAID (mainstream)

- RAID 0
    - Stripping 
    - Hohe Transferraten
    - =Verketten von Platten zu einer größeren virtuellen Platte
    - Brutto = Nettokapazität
    - ![RAID0](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9b/RAID_0.svg/220px-RAID_0.svg.png)
- RAID 1
    + Mirroring
    + Spiegel von einer Platte auf eine andere
    + mind. 2 Platten nötig
    + Netto = 50 % vom GesamtBrutto
    + ![RAID1](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b7/RAID_1.svg/220px-RAID_1.svg.png)
- RAID 3
    + Parität auf extra Platte
    + mind 3. Platten nötig
    + Paritätsplatte wird bei jedem Schreibvorgang der anderen mind. 2 Platten beschrieben **ergo** Flaschenhals
    + wurde durch RAID 5 ersetzt
    + ![RAID3](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/RAID_3.svg/220px-RAID_3.svg.png)
- RAID 5 
    + Parität wird auf alle Platten verteilt
    + Netto = (Anzahl Platten - 1) x Größe der kleinste Platte
    + ![RAID5](https://upload.wikimedia.org/wikipedia/commons/thumb/6/64/RAID_5.svg/220px-RAID_5.svg.png)
- RAID 10
    + Kombiert RAID 1 und RAID 0
    + mind. 4 Platten da im unterem Level Raid 1 passiert also gespiegelt wird
    + Oberes Level = RAID 0 = Zwei Mal RAID 1 im unterem Level
    + ![RAID10](https://upload.wikimedia.org/wikipedia/commons/thumb/b/bb/RAID_10.svg/170px-RAID_10.svg.png)

*F* : "Beispielberechnung Aufgabe:" 
- Zur Berechnung der Nettospeicherkapazität des NAS liegen folgende Daten vor:
    + Es gibt vier Schulungsräume. 
    + Jeder Schulungsraum ist mit einem Dozentenarbeitsplatz und 14 Schülerarbeitsplätzen ausgestattet. 
    + Jeder Dozentenarbeitsplatz eines Schulungsraums ist mit einem Notebook ausgestattet. 
    + Es gibt sechs Dozenten und bis zu 50 Schüler insgesamt. 
- Folgender Speicher soll im NAS zur Verfügung stehen: 
    + 64 GiByte je Dozent für Unterrichtsmaterial 
    + 20 GiByte je Notebook für Images 
    + 16 GiByte je Schüler zur Datensicherung 
    + 40 % Reserve 
- Berechnen Sie die Nettospeicherkapazität des NAS in TiByte.

```java
    6 Dozenten * 64 GiByte Unterrichtsmaterial = 384 GiByte
    4 Schulungsr. == 4 Dozentenplätze Notebook * 20 Gbitye Images = 80 Gibyte
    50 Schüler * 16 GiByte = 800 Gibyte Datensicherungen
    //------
    Sum = 384 + 80 + 800 = 1264 Gib + 40% Reserve (505,6 Gib) = 1769,6 GiByte
    1769,6 GiByte / 1024 = 1,9 TiByte = Netto = 2,0 TiByte Kapa
    //------

```

### Mobile

*F* : Tabletbeschaffung für Außendienst Mitarbeiter
*A* :
- **Merkmal**: Tablet sollte ein Betriebssystem haben welches zum Unternehmen passt
- **Nutzen** : Workflow lässt sicher besser integerieren. 
- Beispiel: Das Unternehmen hat nur Microshit rumstehen inkl. Share Point, Server und den ganzen Kram. Dann wäre ein Tablet mit Windows 10 eventuell sinnvoll.
- **Merkmal** : Garantierzeit
- **Nutzen** : geringeres Kostenrisiko
- **Merkmal** : Hotspotfähig
- **Nutzen** : andere Geräte können I-Net Zugang nutzen


### Networking

#### [VLAN](https://de.wikipedia.org/wiki/Virtual_Local_Area_Network) - Virtual Local Area Network
##### statisch
- Port des Switches wird fest zugeordnet
- Konfiguration fest durch Admin vorgegeben
- Ein Port kann mehere VLAN zugeordnet werden

##### dynamisch
- unsicher
- Zugehörigkeit wird anhand von [IP](#ip) oder MAC gemacht

### Glossar

#### <a id="ip"></a>IP (Internet Protokoll)


