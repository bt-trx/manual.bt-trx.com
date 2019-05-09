# Bedienung

## 1. Anschluss von Funkgerät, Spannungsversorgung und PTT-Taste

Der Anschluss ans Funkgerät erfolgt in der Regel über ein
[Adapterkabel](../Zusammenbau/Adapterkabel).

bt-trx bietet zwei Möglichkeiten um mit Spannung versorgt zu werden:

- Adapterkabel: V_IN (Pin 7)/GND (Pin 8), 6...20 V DC, ca. 40 mA bei 12 V, oder
- Mikro-USB Buchse

Nach dem Herstellen der Spannungsversorgung leuchtet die **rote LED** (zeigt 
3.3 V Betriebsspannung des Controllers und des BT-Moduls an), bt-trx startet automatisch.

## 2. Herstellen der Bluetooth-Verbindung

bt-trx beginnt selbstständig, nach geeigneten Geräten für die
Bluetoothverbindung zu suchen und eine Verbindung herzustellen.  
Es wird nur eine Verbindung mit Geräten hergestellt, die das
"HFP"-Profil unterstützen (Autoradios, bestimmte Headsets). Eine (ungewollte) 
Verbindung mit einem Smartphone kann daher nicht passieren.

Die Verbindung zu einfachen Bluetooth-Headsets über das "HSP"-Profil wird aktuell
noch nicht unterstützt, ist aber möglich und wird in einer der kommenden Firmware-Versionen
eingebaut werden.

Es kann notwendig sein, das Autoradio zum Verbindungsaufbau in den Bluetooth-Pairingmodus zu versetzen, um es
für bt-trx sichtbar zu machen.  
In der Regel geschieht dies über einen Menüpunkt "Neues Bluetooth-Gerät hinzufügen" o.ä..

Sobald die Verbindung einmal erfolgeich hergestellt wurde, sollten sich die beiden Geräte beim nächsten Start des bt-trx, bzw. des Fahrzeugs automatisch miteinander verbinden.

Die beiden Status-LEDs (blau und grün) liefern folgende Informationen:

| LED blau | LED grün | Status                       |
|:--------:|:--------:|------------------------------|
| aus      | an       | BT-Verbindungssuche          |
| an       | aus      | BT-Verbindung hergestellt    |
| an       | blinkt   | Audio-Verbindung hergestellt |

## 3. Herstellen der Audio-Verbindung

Um die Audio-Verbindung herzustellen, **muss** die Bluetooth-Verbindung (blaue LED leuchtet) hergestellt sein.

Die Audioverbindung kann über zwei Wege hergestellt werden:

- Tätigen eines Anrufs an eine beliebige Rufnummer (eine Ziffer genügt) aus dem Telefonmenü des Autoradios heraus.  
bt-trx nimmt den ausgehenden Anruf automatisch an.  
**Wichtig:** Falls das Autoradio mehrere gleichzeitige Bluetooth-Verbindungen unterstützt, muss sichergestellt werden, dass das Telefon "bt-trx" verwendet wird!  
oder
- Drücken des Tasters am bt-trx.  
Damit wird ein eingehender Anruf simuliert, der am Autoradio angenommen werden muss.

Nach dem Herstellen des Telefongesprächs ist die Audioverbindung Autoradio <-> Funkgerät hergestellt und die **grüne LED blinkt**.

Nun kann durch Drücken des PTT-Tasters auf der im Funkgerät eingestellten Frequenz gesprochen werden!  
Falls das Adapterkabel auch die empfangene Audio vom Funkgerät überträgt, sollte diese aus den Fahrzeuglautsprechern 
hörbar sein.

Bei der erstmaligen Verwendung mit einem Funkgerät kann es notwendig sein, die Ein- und Ausgangsaudiopegel mit Hilfe der Lautstärkeeinstellung des Funkgeräts und/oder auf der bt-trx Platine vorhandenen Potentiometer zu justieren.


Die Audioverbindung ist aktiv, solange das Telefongespräch läuft. Durch auflegen oder drücken des Tasters am bt-trx wird das Gespräch, und somit auch die Audio-Verbindung zum Funkgerät beendet.
