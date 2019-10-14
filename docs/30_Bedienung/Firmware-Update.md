# Firmware-Update

Eine neue Firmware-Version kann mittels WLAN auf bt-trx aufgespielt werden.

Dafür muss bt-trx in den Update-Modus versetzt werden. Hierzu hält man SW1
während des Starts von bt-trx für 5 Sekunden lang gedrückt.
Wenn der Update-Modus erfolgreich gestartet wurde, blinken die beiden
Status-LEDs gleichzeitig im Sekundentakt.

Nun kann man sich mit dem Computer oder dem Smartphone mit dem WLAN "bt-trx"
verbinden (Password: "bt-trx73").
Sobald man sich verbunden hat, kann man das bt-trx Modul mit einem Browser
unter [http://bt-trx.local](http://bt-trx.local) oder
[http://192.168.4.1](http://192.168.4.1) erreichen.

![Webinterface Firmware-Update](firmware_update.png)

Auf der Website muss mittels "Choose File" die Firmwaredatei (*.bin) ausgewählt
und mit dem "Update" Button auf das Gerät geschrieben werden.
Nach erfolgreichem Upload und Einspielen des Updates startet sich bt-trx
automatisch neu.

Die aktuellste Firmwareversion kann man sich unter [https://github.com/bt-trx/firmware/releases](https://github.com/bt-trx/firmware/releases) herunterladen.
