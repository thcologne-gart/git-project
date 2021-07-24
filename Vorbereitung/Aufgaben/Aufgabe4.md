# Aufgabe 4 - Dynamische Dashboards
In dieser Aufgabe werdet ihr mehrere Assets in einem dynamischen Dashboard abbilden.

## Grundlagen
* Ihr benötigt den [AAS Server aus Aufgabe 1](Aufgabe1.md) und den [OPC UA Server aus Aufgabe 2](Aufgabe2.md)
* Der opcua-logger muss [installiert](../Installation/opcua-logger.md) sein
* InfluxDB muss [installiert](../Installation/InfluxDB.md) sein
* Grafana muss [installiert](../Installation/Grafana.md) sein
* Grundsätzlich ist die [Videos.md](../Videos.md) Datei zu beachten
* Folgende Videos stehen in direktem Zusammenhang mit der Aufgabe:
  * E10: [Grafana - Dynamische Panels und Dashboards auf Grundlage von Variablen erstellen](https://www.youtube.com/watch?v=biAnjcLIkxc&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=11)
  
## Aufgabenstellung
* Erstelle eine zweite Asset Instanz und lade die Daten analog der ersten Instanz in die InfluxDB.
* Erkunde die Daten in dem Grafana UI und stelle sicher, dass die *lokalen* Instanzen korrekt abgebildet werden.
* Erstelle in Grafana ein neues Dashboard oder überarbeite das bestehende, um beide Asset Instanzen abzubilden.
* Lege sinnvolle Variablen für das Dashboard fest und integriere diese in die Monitoring Anwendung.
* Simuliere folgende Szenarien und analysiere das Verhalten deines Dashboards:
  * Eines der Assets lädt keine Daten mehr in die Datenbank
  * Die Verbindung zwischen allen Assets und der Datenbank bricht ab
  * Ein neues, unbekanntes Asset lädt Daten in der gewohnten Struktur in die Datenbank
  * Ein neues, unbekanntes Asset lädt *andere* Daten in die Datenbank
* Definiere das ideale Verhalten eines Dashboards bei den simulierten Szenarien und implementiere dieses.
* Teste deine Implementierung gegen die Szenarien und verbessere iterativ.

## Hinweise
* Tauscht euch untereinander aus!
* Im Rahmen der Aufgabe bietet es sich an, verschiedene Methoden und Herangehensweisen zu testen und grundsätzlich mit dem opcua-logger, InfluxDB, Grafana sowie den Daten *zu spielen*.

## Tipps
<details>
  <summary>Hier findest du ein paar Tipps</summary>
  <ul>
    <li>Die zweite Asset Instanz kann aus einer Kopie des Flows, AAS Servers und OPC UA Servers bestehen</li>
	<details>
      <summary>Noch ein Tipp</summary>
      <ul><li>Netzwerk Ports sowie Datenquellen der beiden Asset Instanzen müssen unterschiedlich sein</li></ul>
    </details>
    <li>Die definierten Variablen sollten zur Identifizierung der Assets dienen und jeweils einzigartig sein</li>
  </ul>
</details>