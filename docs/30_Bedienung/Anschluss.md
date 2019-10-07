# Bedienung

(Beschreibung für dev-board v4.1 und Firmware Version 0.1.2)

## 1. Anschluss von Funkgerät, Spannungsversorgung und PTT-Taste

Der Anschluss ans Funkgerät erfolgt in der Regel über ein
[Adapterkabel](../Zusammenbau/Anschlusskabel).

bt-trx bietet zwei Möglichkeiten um mit Spannung versorgt zu werden:

- Buchse J5: V_IN (Pin 7)/GND (Pin 8), 5...15 V DC, ca. 90 mA bei 12 V, oder
- Mikro-USB Buchse

Eine [PTT-Taste](../Zusammenbau/PTT-Taste) kann direkt in das bt-trx Gehäuse
integriert (Kontakte J2), oder an die Klinkenbuchse (J3) angeschlossen werden.

Nach dem Herstellen der Spannungsversorgung leuchtet die **rote LED**
(zeigt 3.3 V Betriebsspannung des Controllers und des BT-Moduls an),
bt-trx startet automatisch.

## 2. Herstellen der Bluetooth-Verbindung

bt-trx beginnt nach dem Start selbstständig, nach geeigneten Geräten für die
Bluetoothverbindung zu suchen und eine Verbindung herzustellen.  
Es wird nur eine Verbindung mit Geräten hergestellt, die das
"HFP"-Profil unterstützen (Autoradios, bestimmte Headsets). Eine (ungewollte)
Verbindung mit einem Smartphone kann daher nicht passieren.

**Info:**
Die Verbindung zu einfachen Bluetooth-Headsets über das "HSP"-Profil wird
aktuell noch nicht unterstützt, ist aber möglich und wird in einer der kommenden
Firmware-Versionen eingebaut werden.

Es kann notwendig sein, das Autoradio zum Verbindungsaufbau in den
Bluetooth-Pairingmodus zu versetzen, um es für bt-trx sichtbar zu machen.  
In der Regel geschieht dies über einen Menüpunkt
"Neues Bluetooth-Gerät hinzufügen" o.ä..

Sobald die Verbindung einmal erfolgeich hergestellt wurde, sollten sich die
beiden Geräte beim nächsten Start des bt-trx, bzw. des Fahrzeugs automatisch
miteinander verbinden.

Die beiden Status-LEDs (blau und grün) liefern folgende Informationen:

| LED blau | LED grün | Status                       |
|:--------:|:--------:|------------------------------|
| aus      | an       | BT-Verbindungssuche          |
| an       | aus      | BT-Verbindung hergestellt    |
| an       | blinkt   | Audio-Verbindung hergestellt |
