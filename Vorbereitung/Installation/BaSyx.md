# Installation und Konfiguration von BaSyx

Dieses Dokument dient als Anleitung zur Installation und Konfiguration des BaSyx AAS Servers auf Windows 10.

[<img src="https://www.eclipse.org/basyx/img/basyxlogo.png" width="100">](https://www.eclipse.org/basyx/)

:information_source: **Diese Anleitung wurde mit dem offiziellen BaSyx 1.0.0 Docker Container getestet.**

### Vor der Installation
* Docker Desktop muss installiert und gestartet sein
* Die Nutzung eines JSON-Formatters für den verwendeten Browser ist wärmstens empfohlen
  * Bsp. [Chrome](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa), [Edge](https://www.microsoft.com/de-de/p/json-formatter-for-edge/9nz9d2j86w6s?activetab=pivot:overviewtab), Firefox (built-in)
* Lege einen lokalen Ordner als Datenaustausch für den Container fest. Bsp.: `C:\aas-data`
  * im Folgenden `<local-folder>` genannt.
* [__Getting started with Eclipse BaSyx: Easy AAS setup with off-the-shelf components__](https://www.youtube.com/watch?v=nGRNg0sj1oY) des Fraunhofer IESE folgen
  * :information_source: Hinweise in den folgenden Abschnitten beachten

:information_source: Notiert euch alle wichtigen Daten, insbesondere Zugangsdaten und Datenbanknamen.

### Ergänzende Hinweise zu dem Video
* Das GitHub Repository zu dem aas-package-explorer bei [1 Minuten 17 Sekunden](https://www.youtube.com/watch?v=nGRNg0sj1oY&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&t=1m17s) befindet sich [hier](https://github.com/admin-shell-io/aasx-package-explorer)
  * Windows 10 binaries können unter dem Abschnitt [Releases](https://github.com/admin-shell-io/aasx-package-explorer/releases) heruntergeladen werden
  * Innerhalb der `.zip`  Datei befindet sich die `AasxPackageExplorer.exe`
  * Die erstellte AAS sollte anhand der Daten der fiktiven Pumpe in diesem Repository erstellt werden
* Die erste Eingabe bei [3 Minuten 38 Sekunden](https://www.youtube.com/watch?v=nGRNg0sj1oY&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&t=3m38s) kann ausgelassen werden
  * Alternativ kann die Eingabe durch `docker run --name aas-server -p 4001:4001 eclipsebasyx/aas-server:1.0.0` ersetzt werden
  * Hier wird der Server ohne Parameter gestartet, dies ist nicht notwendig
* Die `aas.properties` Datei bei [4 Minuten 10 Sekunden](https://www.youtube.com/watch?v=nGRNg0sj1oY&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&t=4m10s) kann aus [diesem GitHub Repository](../Dateien/BaSyx) heruntergeladen werden
* Zusätzlich zu der aas.properties Datei soll die context.properties Datei ebenfalls heruntergeladen und in den gleichen Ordner geschoben werden
  * Die `context.properties` Datei erlaubt das Setzen bestimmter Host-Daten wie ContextPath, IP oder Port
* Statt der Eingabe bei [5 Minuten 16 Sekunden](https://www.youtube.com/watch?v=nGRNg0sj1oY&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&t=5m16s) muss `docker run --name aas-server -p 4001:4001 -v <local-folder>:/usr/share/config eclipsebasyx/aas-server:1.0.0` ausgeführt werden

### Ohne Docker Desktop
:information_source: Dieser Abschnitt ist ausschließlich für Studierende gedacht, bei denen Docker Desktop aus verschiedenen Gründen nicht verfügbar ist.

:information_source: Java Version 8 Update 291 (JRE 1.8.0_291-b10) oder höher wird benötigt

* Lade das [BaSyx AAS Server Archiv](../Dateien/BaSyx/Java Server) herunter
  * Die drei Dateien gehören zusammen und bilden gemeinsam eine `.zip` Datei. Gängige Komprimierungsprogramme wie 7zip, WinZip oder WinRAR ermöglichen das Entpacken solch aufgeteilter Archive.
* Lege die extrahierte `Server.jar` in einem beliebigen Ordner ab und erstelle in demselben Ordner den Ordner `resources`
  * In `resources` werden die `aas.properties` und `context.properties` Dateien abgelegt
* Der Server wird dann über die Eingabeaufforderung gestartet. Navigiere dazu in den entsprechenden Ordner und gib `java -jar Server.jar` ein, um den Server zu starten.
  
Damit sind Installation und Konfiguration des BaSyx AAS Servers abgeschlossen.
