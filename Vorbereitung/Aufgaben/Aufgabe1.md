# Aufgabe 1 - Node-RED, AAS, REST
In dieser Aufgabe werdet ihr einen AAS Server via REST-API aus Node-RED mit Daten befüllen.

## Grundlagen
* Ihr benötigt eine [lokale Node-RED Instanz](../Installation/node-RED.md)
* Beachtet die [Hinweise zu dem BaSyx Video](../Installation/BaSyx.md)
* Die Daten einer fiktiven [Pumpe](../Dateien/Pumpendaten) werden benötigt
* [Simulations-Flow](../Dateien/node-RED) für Node-RED
* [Konfigurationsdateien](../Dateien/BaSyx) für BaSyX
* [BaSyx AAS Repository HTTP REST-API](https://app.swaggerhub.com/apis/BaSyx/basyx_asset_administration_shell_repository_http_rest_api/v1)
* [AASX Package Explorer Screencasts](https://admin-shell-io.com/screencasts/) 
* Grundsätzlich ist die [Videos.md](../Videos.md) Datei zu beachten
* Folgende Videos stehen in direktem Zusammenhang mit der Aufgabe:
  * E1: [Node-RED - JavaScript Objekt aus XML Datei erzeugen](https://www.youtube.com/watch?v=Lc5fmeFqGl4&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=2)
  * E2: Fraunhofer IESE: [Getting started with Eclipse BaSyx: Easy AAS setup with off-the-shelf components](https://www.youtube.com/watch?v=nGRNg0sj1oY&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=3)
  * E3: [Node-RED - BaSyx AAS Server per REST API mit Daten befüllen](https://www.youtube.com/watch?v=bhNZlhZ4J8s&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=4)
  
## Aufgabenstellung
* Richte anhand der bereitgestellten Daten einen AAS Server für die *Master Pump 420* ein.
  * Nutze den BaSyx AAS Server Docker Container.
* Bilde in dem AAS Server statische sowie dynamische Daten ab.
  * Die statischen Pumpendaten sind aus einer XML-Datei auszulesen und dürfen nicht bereits im Modell enthalten sein.
  * Die dynamischen Daten können aus einer Node-RED-internen Simulation entnommen werden, grundsätzlich ist die Quelle jedoch freigestellt.
* Bilde unterschiedliche Merkmals- und Datentypen in dem AAS Server ab.
  * Beispielsweise könnte der Produktname in unterschiedlichen Sprachen vorliegen und somit ein Multi Language Property sein.
* Erkunde den AAS HTTP Server mit einem Browser, um sicherzustelölen, dass alle Daten korrekt angezeigt werden.
* Erstelle einen weiteren Node-RED Flow und ließ die AAS aus.
  * Optional kannst du ausprobieren, die ausgelesenen Daten in eine neue Datei zu schreiben.
* Füge das Node-RED contribution package für Modbus hinzu und analysiere die verfügbaren Nodes
  * node-red-contrib-modbus ist [hier](https://flows.nodered.org/node/node-red-contrib-modbus) verfügbar. Es wird entweder über das Node-RED CLI via `npm install node-red-contrib-modbus` oder über das [Node-RED UI](https://nodered.org/docs/user-guide/runtime/adding-nodes) hinzugefügt.

## Hinweise
* Für die Projektarbeit im Labor wird das Informationsmodell vorgegeben.
* Tauscht euch untereinander aus!
* Im Rahmen der Aufgabe bietet es sich an, verschiedene Methoden und Herangehensweisen zu testen und grundsätzlich mit Node-RED sowie den Daten *zu spielen*.

## Tipps
<details>
  <summary>Hier findest du ein paar Tipps</summary>
  <ul>
    <li>Der AASX Package Explorer muss genutzt werden um eine AASX-Datei zu erstellen</li>
    <li>Die XML-Datei mit den statischen Pumpendaten muss von dir erstellt werden</li>
    <li>Die Simulation darf beliebig erweitert oder ersetzt werden</li>
  </ul>
</details>
