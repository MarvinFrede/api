## Externes Review Marvin Frede   
   
| 1. Externes Review|  Protokoll                    |
| -------------   |:-------------------------|
| **Name des Reviewers:**           | Marvin Frede         |
| **Name des Entwicklers:**         | Enno Bublitz               |
| **Team des Entwicklers:**         | Gruppe 1               |
| **Dateien:**             | Fahrrad_1.cpp      |
| **git-Revision:**      | 12550ae531fe02d3d11f4fc201708af93fabfc50 |
| **Untersuchte Funktionalität:**  	| Lesbarkeit und Verständlichkeit des Quellcodes |
| **Reviewergebnisse:**  	        | Der Quellcode ist klar und übersichtlich aufgebaut. Die verwendeten Kommentare sind gut und verständlich geschrieben. Die Variablennamen der ifstreams sind nicht eindeutig und sollten geändert werden. Da noch die Testfunktionen fehlen und dadurch das Projekt noch deutlich wachsen wird, wären Headerdateien und extra Quellcodedatein für die Funktionsdefinition eine Überlegung wert.|     

## Externes Review Florian Zaschka  

| 2. Externes Review|  Protokoll             |
| -------------   |:-------------------------|
| **Name des Reviewers:**           |Florian Zaschka    |
| **Name des Entwicklers:**         |Jens Herbers   |
| **Team des Entwicklers:**         | Gruppe 1   |
| **git-Revision:**      | 8e25450d882b1c21f369138aad3663bf79e0872b |
| **Untersuchte Funktionalität:**  	|Benutzeroberfläche-Anwender Interaktion  |
| **Reviewergebnisse:**  	        | Die Menüführung im Programm ist intuitiv und ohne Vorkenntnisse oder Erläuterungen nutzbar. Die Logik hinter der Anwendung ist durchgängig und somit leicht verständlich. Die Namen der Menüs sind selbsterklärend. An manchen Stellen könnte das Programm eine kurze Rückmeldung geben, dass beispielsweise ein Datensatz neu angelegt wurde oder Daten importiert worden sind. Weiterhin könnte das kritische Kriterium, ab wann man als Dauerparker gewertet wird angezeigt werden. Weiterhin sollte das Programm vor dem Schließen noch 2 Sekunden geöffnet bleiben, damit der Anwender den Schlusssatz lesen kann. |     

    
    
## Externes Review Florian Siebert    
 
| 3. Externes Review|  Protokoll             |
| -------------   |:-------------------------|
| **Name des Reviewers:**           | Florian Siebert        |
| **Name des Entwicklers:**         | Enno Bublitz        |
| **Team des Entwicklers:**         | Gruppe 1   |
| **Dateien:**             | Fahrrad_1.cpp      |
| **git-Revision:**      | 8e25450d882b1c21f369138aad3663bf79e0872b |
| **Untersuchte Funktionalität:**  	| Gereviewt wurden die Funktionen erstellen(), welche einen Eintrag in der Datenbank erstellt, sowie suchen() welche die Datenbank nach bestimmten Einträgen durchsucht mit den Unterfunktionen einzel() zum Anzeigen aller Datensätze, tabelle() zum Anzeigen einer Tabelle aller Datensätze und matr() zum gezielten Suchen nach einer bestimmten Matrikelnummer. |

**Reviewergebnisse:**  	       
Einrückungen, Klammersetzung, Leerzeichen und Zeilenumbrüche sind bis auf wenige Ausnahmen sehr sinnvoll gewählt. Variablennamen spiegeln die Bedeutung der Variablen wieder, sind aber teilweise zu lang (vgl. Zeile 206) und hätten durch Abkürzungen ohne Verlust an Lesbarkeit verkürzt werden können. Insgesamt ist der Text aber sehr übersichtlich und verständlich. 

Kommentare als Überschriften, z.T. in Großbuchstaben, strukturieren den Code und erleichtern die Orientierung. Es gibt keine veraltete oder überflüssige Kommentare. Allerdings ist der Code insgesamt eher wenig kommentiert und bei einigen speziellen Funktionen bzw. Befehlen fehlt ein erklärender Kommentar (vlg. Zeile 84, 108ff, 136ff und 184). Wo Kommentare gesetzt wurden, sind sie kurz und präzise und sorgen meist für ein besseres Verständnis. Einige Kommentare sind hingegen zu kurz und damit zwecklos (vgl. Zeile 152, 230).

In der Funktion erstellen() wird die Eingabe des Vornamens nicht überprüft, sodass die Eingabe eines Leerzeichens dazu führt, dass auch bei späterer Eingabe eines Vornamens kein Eintrag in der Datenbank erstellt wird.

In der Funktion suchen() wird die Eingabe der Auswahl nicht überprüft, sodass eine Eingabe außerhalb der vorgesehenen Möglichkeiten {1, 2, 3} zum Abbruch des Programms führt. Durch eine einfache while-Schleife könnte eine sinnvolle Eingabe erzwungen werden.

In der Funktion matr() ist keine Fehlermeldung für den Fall, dass kein passender Eintrag gefunden wird, vorgesehen.

Am Ende einer jeden Funktion wird nicht zur main() zurückgekehrt sondern die Hauptfunktion wird erneut aufgerufen, sodass keine Funktion je geschlossen wird und alle reservierten Speicherplätze belegt bleiben. Bei einer längeren Nutzung des Programms kann dies zu einer Überlastung des Speichers führen.  
