# Aufgabe 3 - InfluxDB, Grafana
In dieser Aufgabe werdet ihr ausgewählte Daten eines OPC UA Servers in eine Datenbank laden und diese mit Grafana visualisieren.

## Grundlagen
* Ihr benötigt den [AAS Server aus Aufgabe 1](Aufgabe1.md) und den [OPC UA Server aus Aufgabe 2](Aufgabe2.md)
* Der opcua-logger muss [installiert](../Installation/opcua-logger.md) sein
* InfluxDB muss [installiert](../Installation/InfluxDB.md) sein
* Grafana muss [installiert](../Installation/Grafana.md) sein
* Grundsätzlich ist die [Videos.md](../Videos.md) Datei zu beachten
* Folgende Videos stehen in direktem Zusammenhang mit der Aufgabe:
  * E7: [OPC UA - opcua-logger für Upload in InfluxDB einrichten](https://www.youtube.com/watch?v=97MCgv7MS5I&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=6)
  * E8: [Grafana - InfluxDB als data source einrichten und Daten erkunden](https://www.youtube.com/watch?v=kok8IHcI93k&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=7)
  * E9: [Grafana - Dashboard erstellen und mit Daten der InfluxDB anreichern](https://www.youtube.com/watch?v=al9quHfWBqI&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=8)
  
## Aufgabenstellung
* Lade die Daten des *Master Pump 420* OPC UA Servers via opcua-logger in die InfluxDB.
* Unterscheide beim Upload zwischen statischen und dynamischen Daten.
  * Nutze unterschiedliche Datentypen, String Formate, Intervalle und Uploadarten.
* Erkunde die Daten sowohl in dem InfluxDB UI sowie dem Grafana UI und identifiziere mögliche Unterschiede.
* Erstelle in Grafana ein Dashboard, welches sowohl die statischen als auch die dynamischen Daten in geeigneter Weise darstellt.
* Identifiziere wichtige Merkmale eines Dashboards. Nutze dazu dir bekannte Ressourcen.
* Untersuche dein eigenes Dashboard auf die von dir identifizierten Merkmale und entwickle es anhand deines Ergebnisses iterativ weiter.

## Hinweise
* Tauscht euch untereinander aus!
* Im Rahmen der Aufgabe bietet es sich an, verschiedene Methoden und Herangehensweisen zu testen und grundsätzlich mit dem opcua-logger, InfluxDB, Grafana sowie den Daten *zu spielen*.

## Tipps
<details>
  <summary>Hier findest du ein paar Tipps</summary>
  <ul>
    <li>Die Daten müssen in der Datenbank identifizierbar sein</li>
    <li>Der opcua-logger erlaubt die Zuweisung mehrerer Tags, nutze dies, um Daten zu gruppieren</li>
  </ul>
</details>