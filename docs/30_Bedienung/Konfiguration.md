# Konfiguration

!!! note "WLAN-Modus"
    Dafür muss bt-trx in den WLAN-Modus versetzt werden. Hierzu hält man SW1 während des Starts von bt-trx für 5 Sekunden lang gedrückt. Wenn der WLAN-Modus erfolgreich gestartet wurde, blinken die beiden Status-LEDs kurz gleichzeitig.

    Nun kann man sich mit dem Computer oder dem Smartphone mit dem WLAN "bt-trx"
    verbinden (Password: "bt-trx73").
    Sobald man sich verbunden hat, kann man das bt-trx Modul mit einem Browser
    unter [http://bt-trx.local](http://bt-trx.local) oder
    [http://192.168.4.1](http://192.168.4.1) erreichen.


![Webinterface Konfiguration](konfiguration.png)

Um das Webinterface zu nutzen, muss im Browser Javascript aktiviert sein.

## Einstellmöglichkeiten

### Audio

#### ADC Gain

Hier kann die Verstärkung des Audio-Signals _vom_ Transceiver eingestellt
werden (-27...+39 dB).

#### DAC Gain

Hier kann die Verstärkung des Audio-Signals _zum_ Transceiver eingestellt
werden (-42...+24 dB).

### PTT

#### PTT Hang Time

Zeit, die PTT nach Loslassen der PTT Taste noch aktiv bleibt, um die
Signalverzögerung der Freisprecheinrichtung auszugleichen.

**Wichtig:** Jumper J5 muss auf "uC" gesetzt sein ("Soft-PTT Modus").

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
