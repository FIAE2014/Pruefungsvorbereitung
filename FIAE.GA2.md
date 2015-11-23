# FIAE Kompendium Cheat-Sheet zur Prüfung

Inhalte werden anhand alter Prüfungen erstellt!
## Else
### [EPK](https://de.wikipedia.org/wiki/Ereignisgesteuerte_Prozesskette)
![epk](https://upload.wikimedia.org/wikipedia/commons/thumb/4/43/Beispiel_ereignisorientierte_Prozesskette_%28EPK%29.png/170px-Beispiel_ereignisorientierte_Prozesskette_%28EPK%29.png)

Funktion -> Zustand
Auftrag annehmen -> Auftrag angenommen

Verknüpfungen:
 - AND -> Spitzenklammer nach oben like ^ sieht fast aus wie ein "A"
 - OR -> V 
 - XOR -> XOR

Akteure -> Blase mit senkrechte Linie an der link Seite

## Software
### Imperative Programmierung
Programmiersprachen die wirklich etwas tun like C#, C++ etc
### Deklarative Programmierung
"Programmiersprachen" die wirklich etwas aussagen like YAML, XAML, Markdown ;)
Beschreibung eines Problems im Vordergrund
### 3GL/4GL
4GL : Python, Ruby, PHP
3GL : C , Fortran
### Kyroptograhie
#### [symmetrisches](https://de.wikipedia.org/wiki/Symmetrisches_Kryptosystem)
![sy](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7b/Orange_blue_symmetric_cryptography_de.svg/300px-Orange_blue_symmetric_cryptography_de.svg.png)
 - Ein Schlüssel für beide Parteien
 - Beispiel -> AES oder Blowfish
#### [asymmetrisches](https://de.wikipedia.org/wiki/Asymmetrisches_Kryptosystem)
![asy](https://upload.wikimedia.org/wikipedia/commons/thumb/9/92/Orange_blue_public_private_keygeneration_de.svg/170px-Orange_blue_public_private_keygeneration_de.svg.png)
 - Empfänger und Absender haben unterschiedliche Schlüssel (Privat/Public Key)
 - sicherer als systemmtrische Kyptograhie
 - Bekannteste Anwendungsbeispiel (RSA)
### Linux / Unix
[vs](http://servermaniac.de/23924-unix-oder-linux-der-unterschied/)
- Unix ist nur der Betriebssystemkern
- Linux ein Bündle aus Kern und anderer Betriebsystemsoftware (Derviate wie Ubuntu)

### [RIA](https://de.wikipedia.org/wiki/Rich_Internet_Application) - Rich Internet Application
Erweiterte Funktionen im Web (z.B. Drag and Drop). Bereitgestellt durch Framework. Applikation kommuniziert mit Server.

Definition: „Reichhaltigkeit der Bedienoberfläche“ sowie „Verbindung mit dem Internet“

Barrierefreiheit
 - Inhalt ist durch Screenreader lesbar
 - Bilder müssen alternativ text haben
 - Tab Steuerbar
Suchmaschinenoptimierung
 - Bots lesen gezielt definierte Inhalt aus (meta tags etc)

Pluginbasierend:
 - Silverlight von Microsoft
HTMLbasierend:
 - Google Webtoolkit
 - Diverse JS Frameworks


### [Multitasking](https://de.wikipedia.org/wiki/Multitasking)
 - Ausführung mehrere Aufgaben paralell
 - prioritätsbasierte Ressourcenverteilung
 - Aufgaben werden in kurzen Abständen immer abwechseln ausgeführt -> Eindruck von Parallelität
 - Multicore Systeme können wirklich parallel arbeiten (Multiprocessing)

### [ACID](https://de.wikipedia.org/wiki/ACID) - Atomicity, Consistency, Isolation und Durability
Verarbeitungseigenschaften
 - Atomicity -> Kleine Häppchen von Daten
 - Consistency -> Beziehung bleiben erhalten -> PF/FK
 - Isolation -> Lese/Schreibaufgaben können sich nicht gegenseitig beeinflussen.
 - Durability -> Daten bleiben Dauerhaft in Datenbank

## Hardware
### [Strukturierte Verkabelung](https://de.wikipedia.org/wiki/Strukturierte_Verkabelung)
![skv](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4b/Strukturierte_Verkabelung.svg/200px-Strukturierte_Verkabelung.svg.png)
1. Primär -> Gebäudeverkabelung -> Lichtwelleleiter (2000m)
2. Sekundär -> vertikale Etagenverteilung -> LWL(2000m) oder Twistedpair(100m)
3. Tertiär -> horizontale Etagenverkabelung -> Twistedpair(100m)

### Lichtwelle
 - Unempfintlich gegen EM Störungen
 - Höher Datenrate
 - Längere Übertragungsweg möglich
 - ! Höhere Anschaffungskosten
 - ! Schwerer zu verlegen da nicht knickbar

### [Von-Neumann-Architektur](https://de.wikipedia.org/wiki/Von-Neumann-Architektur)
Referenzmodell für Computer, wonach ein gemeinsamer Speicher sowohl Computerprogrammbefehle als auch Daten hält
 - Komponenten
   + ALU -> Prozessor
   + Control Unit -> Interpreter (von Anweisung)
   + Memory -> Speicher -> Daten & Programme
   + I/O Unit -> steuert Ein und Ausgabe von Daten
 - Programmablauf
   + Befehle sind im Ram (1-Dim Arry)
   + Register zeigt auf Befehl
   + Befehle können geändert werden
 
### [USV](https://de.wikipedia.org/wiki/Unterbrechungsfreie_Stromversorgung) Unterbrechungsfreie Stromversorgung

Schützt vor: 
 - Stromausfall
 - Unterspannung
 - Überspannung
 - Frequenzänderungen
 - Oberschwingungen
Arten: 
 - VFD (Voltage and Frequency Dependent bzw. Offline UPS/USV)
 - VI (Voltage Independent bzw. Netzinteraktive UPS/USV)
 - VFI (Voltage and Frequency Independent bzw. Online UPS/USV)

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
Wird benutzt um Netze portweise aufzutrennen und virtual zur Verfügung zu stellen. In der Regel um Firewallregeln besser erstellen zu können. 

##### statisch
- Port des Switches wird fest zugeordnet
- Konfiguration fest durch Admin vorgegeben
- Ein Port kann mehere VLAN zugeordnet werden

##### dynamisch
- unsicher
- Zugehörigkeit wird anhand von [IP](#ip) oder MAC gemacht
 
#### [VPN](https://de.wikipedia.org/wiki/Virtual_Private_Network)
Verschlüsselung von Netzwerkverkehr

#### Arten
 - Site-to-Site -> Lan 2 Lan -> verbindet zwei Netze untereinander
 - End-to-Site -> PC 2 LAN -> Verbindet PC von außen mit VPN LAN
 - End-to-End -> PC 2 Server -> Verbindet PC direkt mit Zielserver oder Server 2 Server
#### [IPsec](https://de.wikipedia.org/wiki/IPsec)
Bei IPsec müssen alle Endpunkte vorkonfiguriert sein, da sonst keine Vertrauensbeziehung aufgebaut werden kann.
 - Site-to-Site-VPNs
 - End-to-Site-VPNs
 - SPD (security policy database) -> statische Sicherheitsregeln
 - SAD (security association database) -> Stateful, begrenzte Gültigkeit,symmetrischer Verschlüsselung
 + PSK-Authentisierung (Pre Shared Keying):Teilnehmermenge an das IPsec-VPN
 + Zertifikatsbasierte Authentisierung:Endpunkt seine CAs (Vertrauensstellen) kennt und alle Zertifikate
#### [NNTP](https://de.wikipedia.org/wiki/Network_News_Transfer_Protocol) Network News Transfer Protocol
Übertragungsprotokoll in Newsgruppen wie Usenet
 nntp://<host>:<port>/<newsgroup-name>/<article-number>
<table border="0" cellspacing="3" class="float-right">
<caption>NNTP im <a href="/wiki/Internetprotokollfamilie#TCP.2FIP-Referenzmodell" title="Internetprotokollfamilie">TCP/IP‑Protokollstapel</a>:</caption>
<tbody><tr>
<td align="center" bgcolor="#FFCC99"><b>Anwendung</b></td>
<td colspan="5" align="center" bgcolor="#9999FF"><b>NNTP</b></td>
</tr>
<tr>
<td bgcolor="#FFEEBB" align="center"><i>Transport</i></td>
<td colspan="5" align="center" bgcolor="#EEEEFF"><a href="/wiki/Transmission_Control_Protocol" title="Transmission Control Protocol">TCP</a></td>
</tr>
<tr>
<td align="center" bgcolor="#FFEEBB"><i>Internet</i></td>
<td colspan="5" align="center" bgcolor="#EEEEFF"><a href="/wiki/Internet_Protocol" title="Internet Protocol">IP</a> (<a href="/wiki/IPv4" title="IPv4">IPv4</a>, <a href="/wiki/IPv6" title="IPv6">IPv6</a>)</td>
</tr>
<tr>
<td rowspan="2" align="center" bgcolor="#FFEEBB"><i>Netzzugang</i></td>
<td rowspan="2" align="center" bgcolor="#EEEEEE"><a href="/wiki/Ethernet" title="Ethernet">Ethernet</a></td>
<td rowspan="2" align="center" bgcolor="#EEEEEE"><a href="/wiki/Token_Bus" title="Token Bus">Token<br>
Bus</a></td>
<td rowspan="2" align="center" bgcolor="#EEEEEE"><a href="/wiki/Token_Ring" title="Token Ring">Token<br>
Ring</a></td>
<td rowspan="2" align="center" bgcolor="#EEEEEE"><a href="/wiki/Fiber_Distributed_Data_Interface" title="Fiber Distributed Data Interface">FDDI</a></td>
<td rowspan="2" align="center" bgcolor="#EEEEEE">…</td>
</tr>
</tbody></table>
#### [OSI](https://de.wikipedia.org/wiki/OSI-Modell)

<table class="wikitable">
<tbody><tr>
<th colspan="2">OSI-Schicht</th>
<th>Einordnung</th>
<th><a href="/wiki/DoD-Schichtenmodell" title="DoD-Schichtenmodell">DoD-Schicht</a></th>
<th>Einordnung</th>
<th>Protokollbeispiel</th>
<th>Einheiten</th>
<th>Kopplungselemente</th>
</tr>
<tr>
<td align="center" bgcolor="#FFFF99">7</td>
<td align="center" bgcolor="#FFFF99">Anwendungen<br>
(Application)</td>
<td align="center" rowspan="3" bgcolor="#FFFF99">Anwendungs-<br>
orientiert</td>
<td rowspan="3" align="center" bgcolor="#FFCC99">Anwendung</td>
<td rowspan="4" align="center" bgcolor="#FFCC99">Ende zu<br>
Ende<br>
(<a href="/wiki/Direktverbindung" title="Direktverbindung">Multihop</a>)</td>
<td rowspan="3" align="center" bgcolor="#FFCC99"><a href="/wiki/Hypertext_Transfer_Protocol" title="Hypertext Transfer Protocol">HTTP</a><br>
<a href="/wiki/File_Transfer_Protocol" title="File Transfer Protocol">FTP</a><br>
<a href="/wiki/Hypertext_Transfer_Protocol_Secure" title="Hypertext Transfer Protocol Secure">HTTPS</a><br>
<a href="/wiki/Simple_Mail_Transfer_Protocol" title="Simple Mail Transfer Protocol">SMTP</a><br>
<a href="/wiki/Lightweight_Directory_Access_Protocol" title="Lightweight Directory Access Protocol">LDAP</a><br>
<a href="/wiki/NetWare_Core_Protocol" title="NetWare Core Protocol">NCP</a></td>
<td align="center" rowspan="3" bgcolor="#FFCC99">Daten</td>
<td align="center" rowspan="4" bgcolor="#FFCC99"><a href="/wiki/Gateway_(Computer)" title="Gateway (Computer)" class="mw-redirect">Gateway</a>, <a href="/wiki/Content-Switch" title="Content-Switch" class="mw-redirect">Content-Switch</a>, <a href="/wiki/Proxy_(Rechnernetz)" title="Proxy (Rechnernetz)">Proxy</a>, Layer-4-7-Switch</td>
</tr>
<tr>
<td align="center" bgcolor="#FFFF99">6</td>
<td align="center" bgcolor="#FFFF99">Darstellung<br>
(Presentation)</td>
</tr>
<tr>
<td align="center" bgcolor="#FFFF99">5</td>
<td align="center" bgcolor="#FFFF99">Kommunikationssteuerung<br>
(Session)</td>
</tr>
<tr>
<td align="center" bgcolor="#FFFF99">4</td>
<td align="center" bgcolor="#FFFF99">Transport<br>
(Transport)</td>
<td align="center" rowspan="4" bgcolor="#FFFF99">Transport-<br>
orientiert</td>
<td align="center" bgcolor="#FFCC99">Transport</td>
<td align="center" bgcolor="#FFCC99"><a href="/wiki/Transmission_Control_Protocol" title="Transmission Control Protocol">TCP</a><br>
<a href="/wiki/User_Datagram_Protocol" title="User Datagram Protocol">UDP</a><br>
<a href="/wiki/Stream_Control_Transmission_Protocol" title="Stream Control Transmission Protocol">SCTP</a><br>
<a href="/wiki/Sequenced_Packet_Exchange" title="Sequenced Packet Exchange">SPX</a></td>
<td align="center" bgcolor="#FFCC99"><a href="/wiki/Datensegment" title="Datensegment">TCP = Segmente</a><br>
<a href="/wiki/Datagramm" title="Datagramm">UDP = Datagramme</a></td>
</tr>
<tr>
<td align="center" bgcolor="#FFFF99">3</td>
<td align="center" bgcolor="#FFFF99">Vermittlung-/Paket<br>
(Network)</td>
<td align="center" bgcolor="#FFCC99">Internet</td>
<td rowspan="3" align="center" bgcolor="#FFCC99"><a href="/wiki/Direktverbindung" title="Direktverbindung">Punkt zu<br>
Punkt</a></td>
<td align="center" bgcolor="#FFCC99"><a href="/wiki/Internet_Control_Message_Protocol" title="Internet Control Message Protocol">ICMP</a><br>
<a href="/wiki/Internet_Group_Management_Protocol" title="Internet Group Management Protocol">IGMP</a><br>
<a href="/wiki/Internet_Protocol" title="Internet Protocol">IP</a><br>
<a href="/wiki/Internet_Protocol_Security" title="Internet Protocol Security" class="mw-redirect">IPsec</a><br>
<a href="/wiki/Internetwork_Packet_Exchange" title="Internetwork Packet Exchange">IPX</a></td>
<td align="center" bgcolor="#FFCC99"><a href="/wiki/Datenpaket" title="Datenpaket">Pakete</a></td>
<td align="center" bgcolor="#FFCC99"><a href="/wiki/Router" title="Router">Router</a>, <a href="/wiki/Layer-3-Switch" title="Layer-3-Switch">Layer-3-Switch</a></td>
</tr>
<tr>
<td align="center" bgcolor="#FFFF99">2</td>
<td align="center" bgcolor="#FFFF99">Sicherung<br>
(Data Link)</td>
<td rowspan="2" align="center" bgcolor="#FFCC99">Netzzugriff<br></td>
<td rowspan="2" align="center" bgcolor="#FFCC99"><a href="/wiki/Ethernet" title="Ethernet">Ethernet</a><br>
<a href="/wiki/Token_Ring" title="Token Ring">Token Ring</a><br>
<a href="/wiki/Fiber_Distributed_Data_Interface" title="Fiber Distributed Data Interface">FDDI</a><br>
<a href="/wiki/Media_Access_Control" title="Media Access Control">MAC</a><br>
<a href="/wiki/ARCNET" title="ARCNET">ARCNET</a></td>
<td align="center" bgcolor="#FFCC99">Rahmen (<a href="/wiki/Datenframe" title="Datenframe">Frames</a>)</td>
<td align="center" bgcolor="#FFCC99"><a href="/wiki/Bridge_(Netzwerk)" title="Bridge (Netzwerk)">Bridge</a>, <a href="/wiki/Switch_(Computertechnik)" title="Switch (Computertechnik)" class="mw-redirect">Switch</a></td>
</tr>
<tr>
<td align="center" bgcolor="#FFFF99">1</td>
<td align="center" bgcolor="#FFFF99">Bitübertragung<br>
(Physical)</td>
<td align="center" bgcolor="#FFCC99"><a href="/wiki/Bit" title="Bit">Bits</a>, <a href="/wiki/Symbol_(Nachrichtentechnik)" title="Symbol (Nachrichtentechnik)">Symbole</a>, Pakete</td>
<td align="center" bgcolor="#FFCC99"><a href="/wiki/Netzwerkkabel" title="Netzwerkkabel" class="mw-redirect">Netzwerkkabel</a>, <a href="/wiki/Repeater" title="Repeater">Repeater</a>, <a href="/wiki/Hub_(Netzwerk)" title="Hub (Netzwerk)" class="mw-redirect">Hub</a></td>
</tr>
</tbody></table>
### RDP - Remote Desktop Protokol
Übertragungsprotokoll von Bildschirmfreigaben
### ICA
Vorgänger von RDP (wurde nicht von Ms ausgekauft)

### Glossar

#### <a id="ip"></a>IP (Internet Protokoll)


