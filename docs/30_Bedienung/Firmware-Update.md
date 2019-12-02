# Firmware-Update

Die aktuellste Firmwareversion kann man sich unter
[https://github.com/bt-trx/firmware/releases](https://github.com/bt-trx/firmware/releases)
("bt-trx_esp32_firmware_x.y.z.bin") herunterladen.

Eine neue Firmware-Version kann mittels WLAN auf bt-trx aufgespielt werden.

!!! note "WLAN-Modus"
    Dafür muss bt-trx in den WLAN-Modus versetzt werden. Hierzu hält man SW1
    während des Starts von bt-trx für 5 Sekunden lang gedrückt.
    Wenn der WLAN-Modus erfolgreich gestartet wurde, blinken die beiden
    Status-LEDs kurz gleichzeitig.

    Nun kann man sich mit dem Computer oder dem Smartphone mit dem WLAN "bt-trx"
    verbinden (Passwort: "bt-trx73").
    Sobald man sich verbunden hat, kann man das bt-trx Modul mit einem Browser
    unter [http://bt-trx.local](http://bt-trx.local) oder
    [http://192.168.4.1](http://192.168.4.1) erreichen.

!!! warning "bt-trx Update von Firmware <0.3.0 auf 0.3.0 und höher"
    Die bt-trx Firmware ab Version 0.3.0 benötigt aufgrund ihrer Größe eine
    Partitionstabelle, die vom Standard-Layout des ESP32 abweicht.  
    Diese muss für ein Update von einer Version <0.3.0 auf 0.3.0 und höher
    [mittels USB](../../40_Entwicklung/Flashen&#32;der&#32;Firmware&#32;über&#32;USB)  auf den ESP32 aufgespielt werden.

![Webinterface Firmware-Update](firmware_update.png)

Auf der Website muss mittels "Choose File" die Firmwaredatei (*.bin) ausgewählt
und mit dem "Update" Button auf das Gerät geschrieben werden.
**Bitte unbedingt abwarten, bis die Datei komplett hochgeladen wurde!**
Nach erfolgreichem Upload und Einspielen des Updates startet sich bt-trx
automatisch neu.
