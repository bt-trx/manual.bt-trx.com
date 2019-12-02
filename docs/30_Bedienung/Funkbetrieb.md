# Funkbetrieb

## Herstellen der Bluetooth-Verbindung zum Autoradio oder Headset

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

Die beiden Status-LEDs (grün und blau) liefern folgende Informationen:

| Aktivität-LED (grün) | Bluetooth-LED (blau) | Status                       |
|:--------------------:|:--------------------:|------------------------------|
| aus                  | blinkt               | BT-Verbindungssuche          |
| aus                  | an                   | BT-Verbindung hergestellt    |
| blinkt               | an                   | Audio-Verbindung hergestellt |

## Herstellen der Audio-Verbindung

Um die Audio-Verbindung herstellen zu können, **muss** die Bluetooth-Verbindung
(blaue LED leuchtet) hergestellt sein.
Die Audioverbindung wird mittels eines simulierten Telefongesprächs hergestellt,
denn bt-trx verhält sich gegenüber dem Autoradio wie ein Mobiltelefon.

Der Telefonanruf kann über drei Wege hergestellt werden:

- Tätigen eines Anrufs an eine beliebige Rufnummer (eine Ziffer genügt) aus dem
  Telefonmenü des Autoradios heraus.  
  bt-trx nimmt den ausgehenden Anruf automatisch an.  
  **Wichtig:** Falls das Autoradio mehrere gleichzeitige Bluetooth-Verbindungen
  unterstützt, muss sichergestellt werden, dass das Telefon "bt-trx" verwendet
  wird!  
oder
- Drücken der PTT Taste oder SW1 an bt-trx.  
  Damit wird ein eingehender Anruf simuliert, der noch am Autoradio angenommen
  werden muss.

Nach dem Herstellen des Telefongesprächs ist die Audioverbindung
Autoradio <-> Funkgerät hergestellt und die **grüne LED blinkt**.

Nun kann durch Drücken des PTT-Tasters auf der im Funkgerät eingestellten
Frequenz gesprochen werden!  
Falls das Adapterkabel auch die empfangene Audio vom Funkgerät überträgt, sollte
diese aus den Fahrzeuglautsprechern hörbar sein.

Bei der erstmaligen Verwendung mit einem Funkgerät kann es notwendig sein, die
Ein- und Ausgangsaudiopegel mit Hilfe der Lautstärkeeinstellung des Funkgeräts
und/oder auf der bt-trx Platine vorhandenen Potentiometer zu justieren.

Die Audioverbindung ist aktiv, solange das Telefongespräch läuft. Durch Auflegen
oder Drücken des Tasters an bt-trx wird das Gespräch, und somit auch die
Audio-Verbindung zum Funkgerät beendet.
