# Lötanleitung

!!! note "Hinweis"
    Die folgende Lötanleitung bezieht sich auf das bt-trx Kit (v5.0) mit vorbestückten SMD Bauteilen.

## Inhalt des Kits

![Kit v5.0](bt-trx_kit_1024.jpg)

![Generic Jumper Moudule](bt-trx_jumper-module_1024.jpg)

| Menge | Beschreibung          | Bauteilnummer | Hinweis       |
|:-----:|-----------------------|---------------|---------------|
| 1     | Vorbestückte Platine  | -             |               |
| 1     | ESP32 DevKitC         | U3            | zum Produktionszeitpunkt aktuelle Firmware ist bereits aufgespielt |
| 2     | Buchsenleiste 1x19    | -             | für ESP32     |
| 2     | Buchsenleiste 1x8     | J9, J10       |               |
| 1     | Stiftleiste 1x3       | J5            |               |
| 1     | Klinkenbuchse 3.5mm   | J3            |               |
| 1     | RJ45 Buchse           | J1            |               |
| 1     | Taster                | SW1           |               |
| 1     | Gehäuse               | -             |               |
| 1     | Jumper                | -             | für J5        |
| 2     | Befestigungsschrauben | -             |               |
| 1     | Generic Jumper Module | -             |               |
| 2     | Stiftleiste 1x8       | -             | für Generic Jumper Module |

Bitte prüfen Sie ob alle o.g. Bauteile im Kit vorhanden sind.

## Löten der Hauptplatine

![Vorbestückte Platine](bt-trx_board_1024.jpg)

Idealerweise wird mit der Stiftleiste **J5** begonnen, da diese die geringste Bauhöhe aufweist.

!!! note "Hinweis zum PTT-select Jumper J5"
    Der **Jumper J5** muss für den Funkbetrieb **in jedem Fall** gesteckt sein.  
    Er entscheidet,

    * ob der PTT Taster direkt zum Transceiver
    durchgeschleift wird (Stellung "BTN", Pins 1-2 verbunden), oder
    * ob der ESP32
    das PTT Signal erzeugt (Stellung "uC", Pins 2-3 verbunden), wird benötigt
    für "Soft-PTT" Funktionen.

    Weitere Informationen dazu im Kapitel [PTT-Taste](../PTT-Taste/#soft-ptt).

Als nächstes sollte der Taster **SW1** aufgelötet werden. Gefolgt von der RJ45 Buchse **J1** und der Klinkenbuchse **J3**. Hier sollte auf ein planes Aufliegen der Buchsen geachtet werden.

Nun folgen die beiden Buchsenleisten **J9** und **J10** für das *Jumper Modul*.

Zuguterletzt folgt der ESP32 (**U3**). Die 1x19 Buchsenleisten dienen zum einen zur Erhöhung des ESP32 um den Taster unterhalb unterzubringen, zum anderen kann der ESP zu Entwicklungszwecken aus dem bt-trx leicht entfernt werden.

Um den Lötvorgang so einfach wie möglich zu gestalten, werden die Buchsenleisten vor dem Verlöten auf den ESP32 gesteckt und so eine senkrechte Montage gewährleistet.

!!! note "Hinweis"
    Die USB-Buchse des ESP32 muss bei der Montage zum Platinenrand hin orientiert sein

![Vollbestückte Platine](bt-trx_assembled_1024.jpg)

## Löten des Jumper Moduls

Um die Belegung des RJ45 Steckers **J1** an die jeweiligen Funkgeräte anzupassen, muss ein Jumper Modul zwischen **J9** und **J10** eingesetzt werden.
Dazu kann das mitgelieferte *Generic Jumper Module* verwendet werden. Eine detaillierte Anleitung befindet sich unter [Anschlusskabel](../Anschlusskabel).

## Montage in das Gehäuse

Nun wird das Modul mit den 2 beiligenden Schrauben im mitgelieferten Gehäuse
befestigt. Die [Frontblende](../Frontblende) muss manuell bearbeitet oder mit einem
3D Drucker bzw. Lasercutter gefertigt werden.

## Inbetriebnahme

Zur Erstinbetriebnahme wird das bt-trx Modul mit einem Micro-USB Kabel oder
über **J1** (siehe [Anschlusskabel](../Anschlusskabel)) mit Strom versorgt.

Da der ESP32 vor der Auslieferung bereits mit der aktuellen bt-trx Firmware
bespielt wurde, kann sofort losgelegt werden.
Nach dem kurzen Bootvorgang blinkt die blaue LED und zeigt damit an, dass
Bluetooth-Geräte in der Umgebung gesucht werden.

Nun kann, falls kein Bluetooth PTT Taster verwendet wird, die [PTT-Taste](../PTT-Taste) 
gefertigt werden.

Die weitere Inbetriebnahme kann nun wie [hier](../../30_Bedienung/Anschluss)
beschrieben erfolgen.
