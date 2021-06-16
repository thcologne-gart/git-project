# Installation und Konfiguration von Grafana

Dieses Dokument dient als Anleitung zur Installation und Konfiguration von Grafana auf Windows 10.

[<img src="https://grafana.com/static/assets/internal/grafana_logo-web-dark.svg" width="100">](https://grafana.com/)

:information_source: **Diese Anleitung wurde mit dem offiziellen Grafana 8.0.0-beta3 Docker Container getestet.** Sollte es mit einem späteren build zu Problemen kommen, kann bei der Installation statt `latest` auch `8.0.0-beta3` eingegeben werden.

### Vor der Installation
* Docker Desktop muss installiert und gestartet sein
* Lege einen lokalen Ordner als Datenaustausch für den Container fest. Bsp.: `C:\grafana-data`
  * im Folgenden `<local-folder>` genannt

:information_source: Notiert euch alle wichtigen Daten, insbesondere Zugangsdaten und Datenbanknamen.

:information_source: `<...>` dient als Platzhalter für einen bestimmten Wert. Hier muss entweder ein bereits bekannter Wert eingegeben oder ein neuer Wert festgelegt werden (ohne `<` und `>`)!

### Installation
* Öffne die Eingabeaufforderung (cmd)
* `docker run -d --name grafana -p 3000:3000 -v <local-folder>:/var/lib/grafana grafana/grafana:latest` ausführen

### Konfiguration und Start
* Per Browser mit Grafana verbinden `http://<ip-address>:3000/`
  * `<ip-address>` muss mit der IP Adresse der Maschine ersetzt werden, da `localhost` aufgrund des Docker Containers nicht funktioniert
* Username und Password eingeben (Username: admin, Password: admin)
  * Passwort ändern
  
Damit sind Installation und Konfiguration von Grafana abgeschlossen.