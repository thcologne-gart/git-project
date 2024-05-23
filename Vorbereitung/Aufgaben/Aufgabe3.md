# Aufgabe 3 - Erweitertes Dashboard
In dieser Aufgabe werdet ihr mehrere Assets in einem dynamischen Dashboard abbilden und erweiterte Funktionalitäten Grafanas nutzen.

## Grundlagen
* Ihr benötigt den [OPC UA Server aus Aufgabe 1](Aufgabe1.md) und das [einfache Daschboard aus Aufgabe 2](Aufgabe2.md)
* Grundsätzlich ist die [Videos.md](../Videos.md) Datei zu beachten
* Folgende Videos stehen in direktem Zusammenhang mit der Aufgabe:
  * E10: [Grafana - Dynamische Panels und Dashboards auf Grundlage von Variablen erstellen](https://www.youtube.com/watch?v=biAnjcLIkxc&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=11)
  
## Aufgabenstellung
* Erstelle einen zweiten OPC UA Server mit anderen Daten.
* Erstelle in Grafana ein neues Dashboard oder überarbeite das bestehende, um beide Server abzubilden.
* Simuliere folgende Szenarien und analysiere das Verhalten deines Dashboards:
  * Einer der Server ist abgeschaltet
  * Die Verbindung zwischen allen Servern und Grafana bricht ab
  * Ein neuer, unbekannter Server steht mit ähnlichen Daten als Data source zur Verfügung
  * Ein neuer, unbekanntes Server steht mit *andere* Daten als Data source zur Verfügung
* Definiere das ideale Verhalten eines Dashboards bei den simulierten Szenarien und implementiere dieses.
* Teste deine Implementierung gegen die Szenarien und verbessere iterativ.

## Hinweise
* Tauscht euch untereinander aus!
* Im Rahmen der Aufgabe bietet es sich an, verschiedene Methoden und Herangehensweisen zu testen und grundsätzlich mit dem opcua-logger, InfluxDB, Grafana sowie den Daten *zu spielen*.

## Tipps
<details>
  <summary>Hier findest du ein paar Tipps</summary>
  <ul>
    <li>Der zweite OPC UA Server kann aus einer Kopie des ersten Flows bestehen</li>
	<details>
      <summary>Noch ein Tipp</summary>
      <ul><li>Netzwerk Ports sowie Datenquellen der beiden OPC UA Server müssen unterschiedlich sein</li></ul>
    </details>
  </ul>
</details>
