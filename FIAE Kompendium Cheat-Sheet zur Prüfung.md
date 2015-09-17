# FIAE Kompendium Cheat-Sheet zur Prüfung

Inhalte werden anhand alter Prüfungen erstellt!

## GA1

### Lasten- und Pflichtenheft

1. Lastenheft
    - Verfasser: Auftraggeber
    - Inhalt: Foderungen an das Projekt

2. Pflichtenheft
    - Verfasser: Auftragnehmer
    - Inhalt: Realiesierungsvorgaben auf Grund des Lastenhefts

------------

### Gant
![Gant-Diagramm](https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/Gantt_diagramm.svg/500px-Gantt_diagramm.svg.png)
- Aufgaben*blöcke* werden hintereinandern gereiht um die Ablauf eines Projekts zu strukturieren.
- *Blöcke* können Vorgänger und Nachfolger haben
- *Blöcke* haben eines Mindest und Maximallänge (können auch gleich sein)
- *Kristischer Pfad* sind quasi die längsten anzunehmeden Pfade aufgrund der Maximallänge jedes Blockes
- *Blöcke* können auch parallel abgearbeitet werden, wenn sie nicht von einander abhängig sind.

---------

### UML

1. Anwendungsfall / Use-Case
    - Außenbereiche enthalten Akteure
    - Innenbereiche Anwendungsfälle
    - ![Beispiel](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Uml-UseCase-Beispiel3.svg/300px-Uml-UseCase-Beispiel3.svg.png)
    - Anwendungsfälle können sich selber *extend*en oder auch andere *include*n
    - Generalieserung = Zwei spezielle Anwendungsfälle werden von einem generellerem abgeleitet

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
    - Bspw. Durchlauf eines Bücher Arrays mit sammeln der kosten jedes einzelnen
    ```js
        int krasseSumme = 0;
        
        for buch in bucharray[];
            krasseSumme += buch.kosten;
    ```

5. Bedingungen bewusst werden
    - Bedingungen runterschreiben
    - ggf. nochmal über **&&** (UND) , **||** (ODER) etc. Verknüpfungen nachdenken.


6. Bei OOP (Objektorientieren Aufgaben)
    
    1. Wiederfinden von Schlagwörter aus der Aufgabenstellung in der z.b. Klassenübersicht
        - *Aus allen Berufen...* == *getBerufe(): Beruf[ ]*
        - *Das Gehalt des Berufes abrufen* == Klasse Berufe -> Methode getGehalt()

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
    