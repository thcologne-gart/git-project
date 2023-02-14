# Installation und Konfiguration der InfluxDB

Dieses Dokument dient als Anleitung zur Installation und Konfiguration der InfluxDB unter Windows 10.

[<img src="https://www.influxdata.com/wp-content/uploads/influx-logo-white-01.svg" width="100">](https://www.influxdata.com/)

<!--:information_source: **Diese Anleitung wurde mit dem offiziellen InfluxDB 2.0.5 Docker Container getestet.** Sollte es mit einem späteren build zu Problemen kommen, kann bei der Installation statt `latest` auch `2.0.5` eingegeben werden.-->

### Vor der Installation
* Docker Desktop muss installiert und gestartet sein
* Lege einen lokalen Ordner als Datenaustausch für den Container fest. Bsp.: `C:\influxDB-data`
  * im Folgenden `<local-folder>` genannt

:information_source: Notiert euch alle wichtigen Daten, insbesondere Zugangsdaten und Datenbanknamen.

:information_source: `<...>` dient als Platzhalter für einen bestimmten Wert. Hier muss entweder ein bereits bekannter Wert eingegeben oder ein neuer Wert festgelegt werden (ohne `<` und `>`)!

### Installation
* Öffne die Eingabeaufforderung (cmd)
* `docker run --name influxDB -p 8086:8086 -v <local-folder>:/var/lib/influxdb influxdb:2.0.5` ausführen

:information_source: `\` erzeugt einen Zeilenumbruch, ohne das Kommando abzuschicken

### Konfiguration und Start
* Per Browser mit InfluxDB verbinden `http://<ip-address>:8086/`
  * `<ip-address>` ist eure lokale IP Adresse. Dies gilt auch für die folgenden Schritte der Installation und Konfiguration!
* Username, Password, Initial Organization Name und Initial Bucket Name festlegen
  * im Folgenden respektive `<original-username>`, `<original-password>`, `<org-name>` und `<bucket-name>` genannt
  * Bsp.: user, password2020, org, data
* `Configure later` klicken
* Data --> Tokens --> `<original-username>'s Token` klicken und mit `Copy to Clipboard` Token String kopieren
  * im Folgenden `<token>` genannt
* Data --> Buckets --> ID des Buckets <bucket-name> mit einem Klick auf die ID kopieren
  * im Folgenden `<bucket-id>` genannt
* In Docker Desktop bei dem influxDB Container auf `CLI` klicken
* Folgende Eingaben nacheinander durchführen:

___1. Legt eine dauerhafte Konfiguration an, die den Token speichert und Schreibrechte gewährleistet:___
```
influx config create \
--active \
--config-name <config-name> \
--host-url http://<ip-address>:8086 \
--org <org-name> \
--token <token>
```

___Beispiel___
```
influx config create \
--active \
--config-name example-config \
--host-url http://192.168.0.1:8086 \
--org organization \
--token q_ETpZ8yAjqOt-KupyfShva3otKaF4zhPHwRV2d7x1y1ZobwDTLiFWUJ4a8s65-q6rHQGrKXkhi1SyOJOj3KkQ==
```

___2. Legt einen zusätzlichen InfluxDB-User für opcua logger an:___
```
influx user create \
--name <logger-username> \
--password <logger-password> \
--org <org-name>
```

___Beispiel___
```
influx user create \
--name logger \
--password logger2020 \
--org organization
```

___3. Legt einen zusätzlichen InfluxDB-User für Grafana an:___
``` 
influx user create \
--name <grafana-username> \
--password <grafana-password> \
--org <org-name>
```

___Beispiel___
``` 
influx user create \
--name grafana \
--password grafana2020 \
--org organization
```

___4. Legt eine v1 Datenbank zum v2 Bucket an:___
``` 
influx v1 dbrp create \
--bucket-id <bucket-id> \
--db <database-name> \
--rp <retention-policy-name> \
--default
```

___Beispiel___
``` 
influx v1 dbrp create \
--bucket-id 8f67da14d3fcc6d2 \
--db data \
--rp data-rp \
--default
```

___5. Gibt opcua logger Schreibrechte:___
``` 
influx v1 auth create \
--read-bucket <bucket-id> \
--write-bucket <bucket-id> \
--username <logger-username>
```

___Beispiel___
``` 
influx v1 auth create \
--read-bucket 8f67da14d3fcc6d2 \
--write-bucket 8f67da14d3fcc6d2 \
--username logger
```

___6. Gibt Grafana Leserechte:___
``` 
influx v1 auth create \
--read-bucket <bucket-id> \
--username <grafana-username>
```

___Beispiel___
``` 
influx v1 auth create \
--read-bucket 8f67da14d3fcc6d2 \
--username grafana
```

Damit sind Installation und Konfiguration der InfluxDB abgeschlossen.

### Ohne Docker Desktop
:information_source: Dieser Abschnitt ist ausschließlich für Studierende gedacht, bei denen Docker Desktop aus verschiedenen Gründen nicht verfügbar ist.

* Besuche den Abschnitt [Install InfluxDB](https://docs.influxdata.com/influxdb/v2.0/install/) der InfluxDB Dokumentation und folge den Anweisungen
