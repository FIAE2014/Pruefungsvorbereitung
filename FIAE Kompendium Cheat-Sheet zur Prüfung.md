# FIAE Kompendium Cheat-Sheet zur Prüfung

Inhalte werden anhand alter Prüfungen erstellt!

## GA1

### Projektmanagment meist(HS1)

1. Lastenheft
    - Verfasser: Auftraggeber
    - Inhalt: Foderungen an das Projekt

2. Pflichtenheft
    - Verfasser: Auftragnehmer
    - Inhalt: Realiesierungsvorgaben auf Grund des Lastenhefts

------------

#### Gant
![Gant-Diagramm](https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/Gantt_diagramm.svg/500px-Gantt_diagramm.svg.png)
- Aufgaben*blöcke* werden hintereinandern gereiht um die Ablauf eines Projekts zu strukturieren.
- *Blöcke* können Vorgänger und Nachfolger haben
- *Blöcke* haben eines Mindest und Maximallänge (können auch gleich sein)
- *Kristischer Pfad* sind quasi die längsten anzunehmeden Pfade aufgrund der Maximallänge jedes Blockes
- *Blöcke* können auch parallel abgearbeitet werden, wenn sie nicht von einander abhängig sind.

#### Modelle

1. Wasserfall-Modell
    - ![Wasser](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e8/Waterfall_model-de.svg/800px-Waterfall_model-de.svg.png)
    - Geht von oben nach unten
    - Stadien (5 Stk)
        + Anforderungen
        + Entwurf
        + Implmentation
        + Überprüfung
        + Wartung
    - Phasenerbenisse sind Vorgabe für nächste Phase
        + Wartung braucht Überprüfung braucht vorher ne Implementation welche erst da ist nachdem ein Entwurf gemacht wurde und dieser kann ja erst gemacht werden wenn man die Anforderungen weiß

2. Spiral-Modell
    - Sequel zu Wasserfallmodell ;)
    - Entwicklung läuft quasi im Kreis an den Phasen vorbei und wiederholt sich deshalb oft.
    - Phasen:
        +   Ziele festlegen
        +   Alternativen beurteilen
        +   Coden
        +   Planung des nächsten Zyklus
    - Und dann heißt es "Und täglich grüßt das Murmeltier". Quasi ist Bill Murrey hier der Coder

3. V-Modell
    - ![V](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3a/V-Modell.svg/440px-V-Modell.svg.png)
    - Geht wie ein V von links oben nach recht oben
    - linke Seite hat nur System- / Softwareshit (2x Entwurf und 2x Archtiektur)
    - rechte Seite streckt die Hand nach rechts oben mit Integrationszeug
    - Schluß ist auf jeden Fall die Abnahme
    - Fazit: Defeniert den Weg zur Qualitätssicherung phasenweise

4. Extreme Programming
    - Standard in der Praxis
    - Lösen einer Programmieraufgabe hat oberste Priorität, wenn dann langweile herscht können immer noch Diagramme gemalt werden.
    - Hat im Spiralmodell sehr kurze Zyklen da alternativen weniger Prio bekommen
    - Bill Murrey on Speed

---------

### UML

1. Anwendungsfall / Use-Case
    - Außenbereiche enthalten Akteure
    - Innenbereiche Anwendungsfälle
    - ![Beispiel](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Uml-UseCase-Beispiel3.svg/300px-Uml-UseCase-Beispiel3.svg.png)
    - Anwendungsfälle können sich selber *extend*en oder auch andere *include*n
    - Generalieserung = Zwei spezielle Anwendungsfälle werden von einem generellerem abgeleitet

2. Klassendiagramm
    1. Klassenname mit eventuell Eigenschaften wie (*abstract*, *protected*)
    2. Attribute (Variablen) nach Muster 
        1. *private* **-** / *public* **+** Operator
        2. Name des Attributes
        3. **:**
        4. Typ des Attributes (string, int, KlasseXY)
            + Bspw: ```-LSD:Drug```
            + Die Variable "LSD" ist vom Typ 'Drug' aber nicht direkt zugänglich durch den private Operator
    3. Methoden / Funktionen nach Muster
        1. *private* **-** / *public* **+** Operator
        2. Name der Methode
        3. **:**
        4. Rückgabetyp (string, int, andere Klasse, void(nix))
            + Bspw: ```+buyDrug():Drug```
            + Ist eine öffentliche Methode um Drogen zu kaufen, bei welcher man logischer Weise ein Objekt "Drug" zurückbekommt
    
    4. Klassen können Beziehungen untereinander haben. Dadurch erkennt man *Vererbung* oder *Erweiterung* einer anderen Klasse -> Stichworte: *include* , *extends*
        
3. Zustandsdiagramm
    1. ![Zustand](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1f/Uml-Zustandsdiagramm-2.svg/300px-Uml-Zustandsdiagramm-2.svg.png)
    2. ![Legende](https://upload.wikimedia.org/wikipedia/commons/thumb/2/28/Uml-Zustandsdiagramm-4.svg/200px-Uml-Zustandsdiagramm-4.svg.png)
    3. Haben Eintrittspunkt (einfacher gefüllter Kreis) und Austrittspunkt(ge füllter Kreis mit Kreis drumherum)
    4. Pfeile um den Ablauf zu deklarieren
    5. Zustände in Blöcken

4. Aktivitätsdiagramm
    1. ![Aktivtat](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/Uml-Activity-Beispiel1.svg/400px-Uml-Activity-Beispiel1.svg.png)
    2. Sieht doch fast so aus wie das Zustandsdiagramm

---

### Datenbanken

#### ERM - Entity Relationship Modell

![BSP](https://upload.wikimedia.org/wikipedia/de/thumb/a/ab/Er-diagramm.svg/300px-Er-diagramm.svg.png)

**Entity** -> Datensatz , Objekt, greifbare Sache
- Datensatz eines Kunden in der Datenbank

**Relationship** -> Beziehungen zwischen Datensätzen / Tabellen
- Der Kunde von eben ist Teil einer Kundengruppe
- Ergo n-Kunden können n-Kundengruppen haben also n-zu-n Beziehung

**Attribute** : Eigenschaften eines Kunden z.B. Alter, Hodengewicht
- Sind Teil der Entität sind 

**Ausschau halten nach**
1. mehrere = n-Beziehungen
2. ein oder mehrere = 1n-Bezieung
3. ein = 1er Beziehung

- an jedem Schritt die Beziehung (1 || n) vermerken auch wenn mann es nicht weiß 50/50 Chance!
- an jeder Beziehung Deklaration wie ("besteht aus", "gehört zu", "befindet sich in") usw. in das Rechteck hauen!

### SQL - Shit Query Language

1. AssoTabelle
    1. *Lösche* Beweise
    ```sql
    DROP TABLE Beweise;
    ```
    2. *Erstelle* Drogenverteilung
    ```sql
    CREATE TABLE DrugSharing;
    ```
    3. *Erstelle* Drogenverteilung mit Droge(FK , INT), Kosument(FK, INT), Schulden(INT)
    ```sql
    CREATE TABLE DrugSharing(
        _id INT(10) UNIQUE PRIMARYKEY,
        drug_id INT(10) FOREIGNKEY Drugs,
        customer_id INT(10) FOREIGNKEY customer,
        guilt CURRENCY  )
    ```
    4. *Ermittle* Keks
    ```sql
    SELECT Keks FROM Tüte
    ```
    5. *Sortiere* nach Blastergeschwindigkeit
    ```sql
    SELECT * FROM Blaster ORDER BY Speed
    ```
2. Beispiele
    1. Alle Rechnungen eines Kunden XY
    ```sql
        SELECT * FROM Rechnung , Kunde WHERE Rechnung.KundeID == 123
    ```
    2. Alle Rechnungen aus dem Vorjahr
    ```sql
        SELECT * FROM Rechnung WHERE Rechnung.Datum < CURRENTYEAR()
    ```
    3. Alle Rechnung aus dem Vorjahr kopieren in Tabelle Archiv
    ```sql
        INSERT INTO Rechnungsarchiv VALUES (
            SELECT * FROM Rechnung WHERE Rechnung.Datum < CURRENTYEAR();
        );
    ```
    4. Alle Rechnung löschen die eben kopiert wurden sind.
    ```sql
        DELETE FROM Rechnung WHERE Rechnung.ID  IS IN Rechnungsarchiv
    ```
    5. Alle Rechnung aus (Archiv und Normal) eines Kunden '123', sortiert nach Datum mit der Information Herkunft (welche Tabelle)
    ```sql
        SELECT 
            (DESCRIBE NAME) as Herkunft, RechnungsID, KundenID, Datum, Summe
        FROM Rechnung, Rechnungsarchiv
        WHERE Rechnung.KundenID == 123 || Rechnungsarchiv.KundenID == 123
        ORDER BY Datum
    ```
    6. Alle Kunden die noch keine Rechnung haben.
    ```sql
        SELECT * FROM Kunden WHERE Kunde.ID NOT IN Rechnungen.KundeID
    ```
    7. Scheiß aufn Rechnungsarchiv gibt ja nur 10 Jahr Aufhebepflicht
    ```sql
        DROP TABLE Rechnungsarchiv;
    ```

### Datenbankmodelle

1. Asso Tabelle:
    - **ein** Thema -> **mehrere** Dingens
        - 1:n Beziehung
        - Thema hat auf jedenfall schonmal ein *FOREIGN_KEY* zu Dingens
    - **eindeutige** Themen
        - *Primary KEY* ggf. mit *UNIQUE* Eigenschaft

---

### Pseudoshit

1. Aufgaben lesen
2. Hightlights suchen
    - übergebe 'foo' == ``` parameter foo```
    - ausgeben / zurückgeben == ```*print* oder *return*```
    - wenn / ansonsten / aber = ```if...then...[else]```
    - für jede = ```for...each..```
    - solange = ```do... while*```
    - gesamt ermitteln = ```summeX = 0;``` als Zähler definieren
3. Basics runterschreiben 
    - wenn was zurückgegeben wird, muss es auch initalsiert werden
    ```java
        int krasseZahl = 0;
        magic....
        return krasseZahl;
    ```
4. Schleifen bewusst werden
    - Schleifen initalieseren und ggf. Zähler auch
    - Zähler sind meist daran zu kennen *summieren sie A für jedes XY*
    - Bspw. Durchlauf eines Bücher Arrays mit sammeln der kosten jedes einzelnen.
    ```js
        int krasseSumme = 0;
        
        for buch in bucharray[];
            krasseSumme += buch.kosten;
    ```

5. Bedingungen bewusst werden
    - Bedingungen runterschreiben
    - ggf. nochmal über UND , ODER etc. Verknüpfungen nachdenken.

6. Bei OOP - Objektorientieren Aufgaben
    
    1. Wiederfinden von Schlagwörter aus der Aufgabenstellung in der z.b. Klassenübersicht
        - Aus allen Berufen... == getBerufe(): Beruf[ ]
        - *Das Gehalt des Berufes abrufen* == Klasse Berufe -> Methode "getGehalt()"

    1. Statische-Methoden anderer Klassen, müssen mit dem Klassennamen aufgerufen werden
        
        ```js
            KlasseXY.methodeABC();
        ```

    2. Normale Publicmethoden müssen vorher in einem Objekt initalisiert werden. Bspw: Gibt Klasse *Bar* mit Methode *magic*
        
        ```js
            Bar foo = new Bar();
            foo.magic();
        ```

    3. Falls die Methode wiederrum ein Objekt zurückgibt, sollte das auch im Pseudocode ersichtlich sein(BTW liest sich auch besser)

        ```java
            class Döner {
                getBrot(){
                    return new Brot();
                }
            }

            class Brot {
               constructor(){
                    return "Semmel"
               }
            }

            bauDönerUndGibBrot(){
                Döner dönerfürAli = new Döner();
                Brot brotdesDönerfürAli = dönerfürAli.getBrot();
                return brotdesDönerfürAli; //"Semmel"
            }
        ```
------
### More OOP

    1. Abstrakte Klassen
        - Lassen sich **nicht** initaliesieren!
        - Können z.B. in Bibliotheken verwendet werden um Methoden bereitzustellen
        ```java
            public abstract class MethCookingFormulars{
                int methamphetamin_weight = 300;

                public cookingtime(int time){
                    return this.methamphetamin_weight * 400 / 20 * time;
                }
            }

            MethCookingForumlars.cookingtime(20); // 120.000
        ```
    2. Kontruktoren
        - Enthalten den Bauablauf eines Objektes.
        - Sobald z.B. ```new KLASSE()``` aufgerufen wird, wird der Kontruktor ausgeführt
        ```java
            public class BobbyCar{
                private Color farbe;

                //Kontruktor
                public BobbyCar(int[] farbe){
                    this.farbe = Color.getRGB(farbe);
                }
            }

            BobbyCar BrunosBobbyCar = new BobbyCar({255,0,0});
            //Auch wenn wir bis jetzt nicht auf die Eigenschaft farbe zugreifen können, wissen wir sie ist rot.
        ```
    3. Überladung
        - Alle Methoden können überladen werden!  
        - Wenn wir eine Klasse mit mehreren Bauabläufen haben, **überladen** sich die Kontruktoren. Also wird der Kontruktor genutzt, welcher die gleichen Parameter (Anzahl und Typen) nutzt, wie wir sie übergeben.
        Passt einer nicht, ist halt schlecht!
        ```java
        public class BobbyCar{
                private Color farbe;

                //Kontruktor für RGB eingabe
                public BobbyCar(int[] farbe){
                    this.farbe = Color.getRGB(farbe);
                }

                //Kontruktor für HEX Wert
                public BobbyCar(string hexfarbe){
                    this.farbe = Color.getHEX(hexfarbe)
                }
            }

            BobbyCar BrunosBobbyCar = new BobbyCar({255,0,0}); //RED BOBBYCAR
            BobbyCar DannysBobbyCar = new BobbyCar("#0000FF"); //BLUE BOBBYCAR 
            

        ```

    4. Statische Methoden / Attribute
        - Wenn Attribute oder Methoden als statisch deklariert sind, können sie ohne initaliesierung eines Objektes der Klasse genutzt werden.
        - Statische Attribute sind Objektübergreifend!
        ```java
        public class BobbyCar{
                private Color farbe;
                public static int anzahlBobbyCars;

                //Kontruktor für RGB eingabe
                public BobbyCar(int[] farbe){
                    BobbyCar.anzahlBobbyCars++;
                    this.farbe = Color.getRGB(farbe);
                }

                //Kontruktor für HEX Wert
                public BobbyCar(String hexfarbe){
                    BobbyCar.anzahlBobbyCars++;
                    this.farbe = Color.getHEX(hexfarbe)
                }
            }

            BobbyCar BrunosBobbyCar = new BobbyCar({255,0,0}); 
            print BobbyCar.anzahlBobbyCars; // 1

            BobbyCar DannysBobbyCar = new BobbyCar("#0000FF");
            print BobbyCar.anzahlBobbyCars; // 2
            

        ```
    5. Vererbung
        - Klassen bedienen sich an anderen Klassen deren Eigenschaften und Methoden sind also Faule Klasse

        ```java
            public class Alkohol{
                Double alc_in_przent;
                public String securitynotice = "Dont drink and drive";
            }

            public class Vodka extends Alkohol{
                String herkunft = "Russian";
                String brand = "noname";

                public Vodka(Int volt){
                    
                }
            }

            public class AlexSixtyThree extends Vodka{
                private String herkunft = "West-Deutschland";
                public String brand = "Alex SixtyThree Vodka " + this.alc_in_prozent +"%";
                
                public AlexSixtyThree(Int volt){
                    this.alc_in_prozent = volt;
                }
            }

            //Beispiele
            //Remember:
            //Klasse variable = new Klasse([Parameter]);
            AlexSixtyThree specialVodka = new AlexSixtyThree(20);
            print specialVodka.brand //Alex SixtyThree Vodka 20 %
            print specialVodka.securitynotice // "Dont drink and drive"
        ```

