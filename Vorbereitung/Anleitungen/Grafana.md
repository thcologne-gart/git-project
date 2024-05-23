# Grafana
In Grafana wird die Visualisierung der Daten aus dem OPC UA Server stattfinden. Dazu müssen der OPC UA Server als Data source konfiguriert und ein Dashboard erstellt werden.

## Data source einrichten
In der VM ist beispielhaft bereits eine OPC UA Data source eingerichtet. Anhand dieser ist erkennbar, wie eine eigene Data source eingerichtet werden kann. Letztlich muss beim Erstellen der Data source der Pfad zu dem Server angegeben werden. Da sich Grafana und der OPC UA Server beide innerhalb der VM befinden, ist der Pfad immer opc.tcp://localhost:{Port}. Der Port variiert je nachdem, was innerhalb Node-Red für die OPC UA Server Node parametriert wurde. Der Beispielserver ist auf dem Port 53880.

Weitere Data sources können eingerichtet werden, ohne die bestehenden Data sources ändern zu müssen.

## Dashboard erstellen
Es ist bereits ein (sehr) einfaches Beispiel Dashboard in der VM vorhanden. Hier werden die drei Variablen des Beispielservers abgebildet. Anhand der Einrichtung sit zu erkennen, wie für eigene Variablen in einem eigenene Server verfahren werden kann.

Ein eigenes Dashboard kann zusätzlich zu dem Beispiel erstellt werden, muss sich jedoch im Namen unterscheiden.

Die Dashboards können frei kofnigueriert werden und mit Variablen versehen werden, um dynamische Aspekte zu erlangen. Wie ausgefallen die Visualisierungen ausfallen, hängt maßgeblich von der gescahffenen Datengrundlage ab.

## Weitere Hinweise
* Über den Menüpunkt `Explore` können die Server unabhängig von einem Dashboard erkundet werden.
* Die Dashboards können im JSON Format exportiert werden, um Backups zu erstellen oder sie zu teilen. 
* Sollte ein Kennwort abgefragt werden, ist der Nutzer `admin` und das Kennwort ebenfalls `admin`.
