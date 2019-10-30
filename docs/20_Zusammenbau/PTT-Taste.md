# PTT-Taste

## Allgemeines

Der PTT-Kontakt des Funkgeräts ist auf mehreren Wegen von bt-trx bedienbar.

![Schaltbild PTT-Taste](ptt_schematic.png)

Soll die PTT-Taste direkt in das bt-trx Gehäuse integriert werden,
bietet sich J2 an.  
Soll die PTT-Taste an einer anderen Stelle als das bt-trx Gehäuse montiert
werden, wird der Anschluss an die Klinkenbuchse J3 empfohlen.  
Mit einem Taster und einem Klinkenstecker kann somit einfach eine für den
jeweiligen Zweck passende PTT-Taste gebaut werden (siehe Bild weiter unten).

Der "Ring"-Kontakt der Klinkenbuchse bzw. der mittlere Kontakt von J2 ist mit
einem GPIO (3.3 V, max. 20 mA) des ESP32 verbunden, der den PTT-Status anzeigt
("UC_PTT_LED").  
An diesen Kontakt kann eine LED (mit Vorwiderstand) angeschlossen werden, um
den aktuellen PTT Status widerzuspiegeln.

!!! note "Hinweis zum PTT-select Jumper J5"
    Der **Jumper J5** muss für den Funkbetrieb **in jedem Fall** gesteckt sein.  
    Er entscheidet,

    * ob der PTT Taster direkt zum Transceiver
    durchgeschleift wird (Stellung "BTN", Pins 1-2 verbunden), oder
    * ob der ESP32
    das PTT Signal erzeugt (Stellung "uC", Pins 2-3 verbunden), wird benötigt
    für "Soft-PTT" Funktionen.

## Soft-PTT

"Soft-PTT" ist kurz für "Software-PTT" und beschreibt Komfort-Funktionen, die
mit einer direkten Verbindung der PTT-Taste an den Transceiver nicht möglich
wären.  
Daher wird für Soft-PTT der ESP32 zwischen Taster und Transceiver geschaltet,
damit das PTT Signal per Software gesteuert werden kann.  
Um die Soft-PTT Funktionen nutzen zu können, muss der Jumper **J5** auf der
Stellung "uC" sein (Pins 2-3 verbunden).
Aktuell sind folgende Funktionen in der Firmware integriert:

- PTT wird nach Loslassen des Tasters noch für 500 ms gehalten

## Beispiel für eine selbstgebaute externe PTT-Taste

![Beispiel PTT-Taste](Taster_PTT_640.jpg)
