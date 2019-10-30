# Debugschnittstelle

## Allgemeines

Der ESP32 stellt bei Anschluss per USB an einen Computer mit eine serielle
Schnittstelle zur Verfügung.

Über die serielle Schnittstelle werden Logausgaben während des laufenden
Betriebs ausgegeben. Eine Steuerung von bt-trx ist darüber nicht möglich.

Allerdings sind diese Daten sehr wichtig zur Identifikation und Behebung von
(Verbindungs-)problemen. Nach Möglichkeit sollte bei jeder Support-Anfrage
das Log der seriellen Debugschnittstelle mitgeschickt werden.

## Parameter für die serielle Verbindung

!!! tip
    Unter Windows und macOS sind dafür eventuell Treiber notwendig. Weitere
    Hinweise zum Herstellen der Verbindung findet man auf der
    [Herstellerseite des ESP32](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/establish-serial-connection.html).

* Baud rate: 115200
* Data bits = 8
* Stop bits = 1
* Parity = N

## Beispiel für Ausgaben auf der Debugschnittstelle

``` none
bt-trx Hardware: dev-board v4.1
bt-trx Firmware: v0.2.0
> AT
< WRAP THOR AI (6.1.0 build 1022)
< Copyright (c) 2003-2015 Bluegiga Technologies Inc.
< READY.
ERROR: can't reach WT32i module
> AT
< OK
STATE: CONFIGURE
> SET BT BDADDR
< SET BT BDADDR 88:6b:0f:ee:6d:fb
> SET BT NAME bt-trx-ee6dfb
> SET PROFILE HFP-AG ON
> SET BT CLASS 400204
> SET BT SSP 1 0
> SET BT FILTER 200400 200400
> SET BT AUTH * 0000
> SET CONTROL CONFIG 0001 0000 00A0 1100
> SET CONTROL ECHO 5
> SET CONTROL GAIN 8 10
STATE: INQUIRY
> INQUIRY 5 NAME
...
...
```
