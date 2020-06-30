# Konfiguration

!!! note "WLAN-Modus"
    Dafür muss bt-trx in den WLAN-Modus versetzt werden. Hierzu hält man SW1 während des Starts von bt-trx für 5 Sekunden lang gedrückt. Wenn der WLAN-Modus erfolgreich gestartet wurde, blinken die beiden Status-LEDs kurz gleichzeitig.

    Nun kann man sich mit dem Computer oder dem Smartphone mit dem WLAN "bt-trx"
    verbinden (Password: "bt-trx73").
    Sobald man sich verbunden hat, kann man das bt-trx Modul mit einem Browser
    unter [http://bt-trx.local](http://bt-trx.local) oder
    [http://192.168.4.1](http://192.168.4.1) erreichen.

!!! info "Javascript notwendig"
    Um das Webinterface zu nutzen, muss im Browser Javascript aktiviert sein.

!!! warning "BLE im WLAN-Modus nicht verfügbar"
    Während der WLAN-Modus aktiv ist, kann keine Verbindung mit einem BLE PTT
    Button hergestellt werden.  
    BLE ist währenddessen deaktiviert.

![Webinterface Konfiguration](konfiguration.png)

## Einstellmöglichkeiten

### Identification

Mit diesem Eingabefeld kann das eigene Rufzeichen angegeben werden. Dieses wird
dann für die Benamung der WLAN SSID und des Bluetooth Namens des bt-trx
verwendet.

### Audio

#### ADC Gain

Hier kann die Verstärkung des Audio-Signals _vom_ Transceiver eingestellt
werden (-27...+39 dB).

#### DAC Gain

Hier kann die Verstärkung des Audio-Signals _zum_ Transceiver eingestellt
werden (-42...+24 dB).

### PTT

!!! info
    Für alle nachfolgenden PTT Features muss Jumper J5 auf "uC" gesetzt sein
    ("Soft-PTT Modus").

#### PTT Mode

- Direct  
    Wenn diese Option aktiviert ist, wird PTT aktiviert, solange die PTT Taste
    gedrückt ist.

- Toggle  
    Wenn diese Option aktiviert ist, wird PTT beim einmaligen Drücken so lange
    aktiviert, bis es durch nochmaliges Drücken der PTT Taste wieder deaktiviert
    wird.

- Willimode  
    In diesem Modus ist das Verhalten des Hardware-PTT Tasters folgendermaßen:  
    - Länger als 1 sek halten: Nichts passiert  
    - Kürzer als 1 sek halten: PTT wird getoggelt  
    - Bluetooth PTT Taste verhält sich wie im Toggle Mode.

#### PTT Timeout

Legt fest, wie lange PTT am Stück aktiviert werden kann
("maximum time of transmit").  
Erlaubte Werte: 1-9 Minuten (0 deaktiviert den Timeout).

#### PTT Hang Time

Zeit, die PTT nach Loslassen der PTT Taste noch aktiv bleibt, um die
Signalverzögerung der Freisprecheinrichtung auszugleichen.

### Bluetooth

#### Bluetooth PIN Code

In der Regel ist für das Bluetooth Pairing keine Eingabe einer PIN erforderlich.
Der angezeigte PIN Code kann einfach bestätigt werden.  
Manche Geräte verlangen die Eingabe eines vorgegebenen, 4-stelligen PIN
Codes (siehe Kommentare in der [Kompatibilitätsliste](../../10_Allgemein/Kompatibilitätsliste/)).  
Hier kann der vorgegebene Code eingegeben werden.  
Falls bereits ein Versuch mit falscher PIN stattgefunden hat, sollten mit dem
Button "Reset Bluetooth Pairings" (siehe unten) die Pairings im bt-trx
zurückgesetzt werden, um einen sauberen neuen Versuch zu starten.

#### Reset Bluetooth Pairings

Mit dieser Schaltfläche können alle bisherigen Bluetooth Pairings im bt-trx
gelöscht werden. Ein Neustart ist notwendig, damit die Änderungen aktiv werden.
