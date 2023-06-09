# Installation und Konfiguration von Node-RED

Dieses Dokument dient als Anleitung zur Installation und Konfiguration von Node-RED unter Windows 10.

[<img src="https://avatars.githubusercontent.com/u/5375661?s=200&v=4" width="100">](https://nodered.org/)

<!--:information_source: **Diese Anleitung wurde mit dem offiziellen Node-RED 1.3.5 Docker Container getestet.** Sollte es mit einem späteren build zu Problemen kommen, kann bei der Installation statt `latest` auch `1.3.5` eingegeben werden.-->

### Vor der Installation
* Docker Desktop muss installiert und gestartet sein
* Lege einen lokalen Ordner als Datenaustausch für den Container fest. Bsp.: `C:\node-red-data`
  * im Folgenden `<local-folder>` genannt

:information_source: Notiert euch alle wichtigen Daten, insbesondere Zugangsdaten und Datenbanknamen.

:information_source: `<...>` dient als Platzhalter für einen bestimmten Wert. Hier muss entweder ein bereits bekannter Wert eingegeben oder ein neuer Wert festgelegt werden (ohne `<` und `>`)!

### Installation
* Öffne die Eingabeaufforderung (cmd)
* `docker run -it --name node-red -p 1880:1880 -v <local-folder>:/data nodered/node-red:3.0` ausführen

### Konfiguration und Start
* Per Browser mit Node-RED verbinden `http://<ip-address>:1880/`
  * `<ip-address>` ist eure lokale IP Adresse
  
Damit sind Installation und Konfiguration von Node-RED abgeschlossen.
