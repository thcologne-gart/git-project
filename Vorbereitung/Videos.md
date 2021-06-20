# Videos zur Vorbereitung
Die hier verlinkten Videos dienen der Vorbereitung. Wenn keine Sprungmarken angegeben sind, ist das Video in seiner Gänze relevant.

Einige Videos sind explizit für diesen Kurs entstanden und beschreiben Beispielhaft die nötigen Arbeitsschritte um die vorbereitenden Aufgaben durchzuführen. Sie sollen keine Musterlösung geben und erklären lediglich die wichtigsten Mechanismen und Vorgehensweisen. Je nach persönlichem Vorwissen in den verschiedenen Bereichen, kann es möglich sein einzelne Abschnitte zu überspringen. Es kann außerdem nötig sein, sich bestimmtes Vorwissen erst aneignen zu müssen.

Grundsätzlich sind zum Verständnis der Videos folgende Fähigkeiten vorausgesetzt:
* Grundlegende Kenntnisse in Windows 10 und der Eingabeaufforderung
* Grundlegendes Verständnis von XML-Dateien
* Grundlegendes Verständnis von Programmlogik und Skriptabläufen
* Sicherer Umgang mit EDV im Allgemeinen

Nicht notwendig aber von Vorteil sind folgende Fähigkeiten:
* Erfahrung im Umgang mit Node-RED
* Erfahrung im Umgang mit Docker Containern, insbesondere der Software Docker Desktop
* Erfahrung im Umgang mit Grafana und InfluxDB als data source
* Kenntnisse in JavaScript und NodeJS

Außerdem wird folgende Softwareausstattung vorausgesetzt:
* Windows 10 Betriebssystem
  * Viele Aspekte der Vorbereitung funktionieren auch unter MacOS oder Linux, bestimmte Schritte sind allerdings nur auf Windows 10 möglich
  * Die Erklärungen beziehen sich auf Windows 10, auf weitere Betriebssysteme wird nicht eingegangen
* [Docker Desktop](https://www.docker.com/products/docker-desktop)
* [NodeJS LTS](https://nodejs.org/en/)
* [Unified Automation UaModeler](https://www.unified-automation.com/de/downloads/opc-ua-development.html)
  * Registrierung notwendig
* [Unified Automation UaExpert](https://www.unified-automation.com/de/downloads/opc-ua-clients.html)
  * Registrierung notwendig
* Verschiedene Docker Container deren Installation und Konfiguration in der jeweiligen `.md` Datei erläutert wird. Diese sind:
  * [BaSyx AAS Server](Installation/BaSyx.md)
  * [Grafana](Installation/Grafana.md)
  * [InfluxDB](Installation/InfluxDB.md)
  * [Node-RED](Installation/node-RED.md)
* Verschiedene weitere Software deren Installation und Konfiguration in der jeweiligen `.md` Datei erläutert wird. Diese sind:
  * [NodeOPCUA](Installation/node-opcua.md)
  * [opcua-logger](Installation/opcua-logger.md)
  * [AASX Package Explorer](Installation/BaSyx.md)

## Begleitende Videos für die vorbereitenden Aufgaben
Die folgenden Videos bauen aufeinander auf und sollten während der Bearbeitung der vorbereitenden Aufgaben in der entsprechenden Reihenfolge angeschaut werden.
* [Playlist mit allen Videos](https://www.youtube.com/watch?v=Lc5fmeFqGl4&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy)
* E1: [Node-RED - JavaScript Objekt aus XML Datei erzeugen](https://www.youtube.com/watch?v=Lc5fmeFqGl4&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=1)
* E2: Fraunhofer IESE: [Getting started with Eclipse BaSyx: Easy AAS setup with off-the-shelf components](https://www.youtube.com/watch?v=nGRNg0sj1oY)
  * Die Hinweise in der [BaSyx.md](Installation/BaSyx.md) sind zu beachten.
  * Nicht explizit für diesen Kurs entstanden
* E3: [Node-RED - BaSyx AAS Server per REST API mit Daten befüllen](https://www.youtube.com/watch?v=bhNZlhZ4J8s&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=2)
* E4: [OPC UA - NodeOPCUA Server erstellen und erkunden](https://www.youtube.com/watch?v=5lWk-aKc0uw&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=3)
* E5: [OPC UA - Informationsmodell in UaModeler erstellen und exportieren](https://www.youtube.com/watch?v=CrCrjT1zP1s&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=4)
* E6: [OPC UA - NodeOPCUA Server per REST API mit Daten aus BaSyx AAS Server befüllen](https://www.youtube.com/watch?v=DVMfyJXxlR4&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=5)
* E7: [OPC UA - opcua-logger für Upload in InfluxDB einrichten](https://www.youtube.com/watch?v=97MCgv7MS5I&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=6)
* E8: [Grafana - InfluxDB als data source einrichten und Daten erkunden](https://www.youtube.com/watch?v=kok8IHcI93k&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=7)
* E9: [Grafana - Dashboard erstellen und mit Daten der InfluxDB anreichern](https://www.youtube.com/watch?v=al9quHfWBqI&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=8)
* E10: [Grafana - Dynamische Panels und Dashboards auf Grundlage von Variablen erstellen](https://www.youtube.com/watch?v=biAnjcLIkxc&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=9)

## Weitere Videos
Die folgenden Videos wurden nicht explizit für diesen Kurs ausgelegt. Die Informationen sind jedoch durchgehend interessant und vertiefen das Verständnis der Materie. Es wird wärmstens Empfohlen alle verlinkten Videos eingehend zu studieren.
* Fraunhofer IESE: [Getting started with Eclipse BaSyx: Setting up a running example in 15 minutes from scratch](https://www.youtube.com/watch?v=rRol5EVZHZA)
  * Dieses Video ist nicht notwendig für das Projekt, bietet jedoch wertvolle Hintergrundinformationen zu dem verwendeten BaSyx SDK und sollte von allen Interessierten geschaut werden.
* ACC Automation: [Node-RED Modbus RTU / TCP Communication](https://www.youtube.com/watch?v=yX1w5vcV6cc)
  * Die ersten neun Minuten des Videos erklären die Installation und Verwendung von Modbus Nodes.
  * Ab Minute neun ist das Video nichtmehr relevant für unser Projekt. Interessierte können dem interessanten Video natürlich bis zum Ende folgen.
  * Wichtige Sprungmarken:
    * [Installing node-red-contrib-modbus Palette](https://www.youtube.com/watch?v=yX1w5vcV6cc&t=126s)
    * [Node-RED Modbus Flow Program](https://www.youtube.com/watch?v=yX1w5vcV6cc&t=245s)
