# Inbetriebnahme

## 1. Anschluss des Funkgeräts

Der Anschluss ans Funkgerät erfolgt in der Regel über ein
[Adapterkabel](../Zusammenbau/Anschlusskabel).

## 2. Anschluss einer PTT-Taste

Der Anschluss einer PTT-Taste kann drahtgebunden oder kabellos (über Bluetooth
Low Energy erfolgen). Es ist auch möglich, beide Varianten gleichzeitig zu
nutzen.

!!! note "Hinweis zum PTT-select Jumper J5"
    Der **Jumper J5** muss für den Funkbetrieb **in jedem Fall** gesteckt sein.  
    Er entscheidet,

    * ob der PTT Taster direkt zum Transceiver
    durchgeschleift wird (Stellung "BTN", Pins 1-2 verbunden), oder
    * ob der ESP32
    das PTT Signal erzeugt (Stellung "uC", Pins 2-3 verbunden).
    Dies wird benötigt für "Soft-PTT" Funktionen und für die Nutzung eines
    BLE PTT Buttons.

### Drahtgebunden

Eine [PTT-Taste](../Zusammenbau/PTT-Taste) kann direkt in das bt-trx Gehäuse
integriert (Kontakte J2), oder an die Klinkenbuchse (J3) angeschlossen werden.

### BLE (Bluetooth Low Energy) PTT Button

Nachdem bt-trx gestartet ist, kann durch einen einmaliges Drücken auf den
PTT Button die Verbindung mit bt-trx hergestellt werden.  
Der BLE PTT Button verhält sich wie ein normaler PTT Taster.

!!! warning "Jumper J5"
    Um den BLE PTT Button nutzen zu können, muss Jumper J5 auf Stellung "uC" sein.

## 3. Anschluss an die Spannungsversorgung

Nach dem Herstellen der Spannungsversorgung leuchtet die **bernsteinfarbene LED**
(zeigt 3.3 V Betriebsspannung des ESP32 und des BT-Moduls an),
bt-trx startet automatisch.
