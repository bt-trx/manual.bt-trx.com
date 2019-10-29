# Lötanleitung

!!! note "Hinweis"
    Die folgende Lötanleitung bezieht sich auf das bt-trx Kit (v4.1) mit vorbestückten SMD Bauteilen.

## Inhalt des Kits

![Kit v4.1](bt-trx_kit_1024.jpg)

| Menge | Beschreibung          | Bauteilnummer | Hinweis       |
|:-----:|:---------------------:|---------------|---------------|
| 1     | Vorbestückte Platine  | -             |               |
| 1     | ESP32 DevKitC         | U3            | vorgeflashed  |
| 2     | Buchsenleiste 1x19    | -             | für ESP32     |
| 2     | Stiftleiste 1x3       | J2, J5        |               |
| 1     | Stiftleiste 1x2       | J7            |               |
| 1     | Stiftleiste 1x4       | J6            |               |
| 1     | Klinkenbuchse 3.5mm   | J3            |               |
| 1     | RJ45 Buchse           | J1            |               |
| 1     | Taster                | SW1           |               |
| 1     | Gehäuse               | -             |               |
| 1     | Jumper                | -             |               |
| 2-4   | Befestigungsschrauben | -             |               |

Bitte prüfen Sie ob alle o.g. Bauteile im Kit vorhanden sind.

## Lötvorgang

![Vorbestückte Platine](bt-trx_board_1024.jpg)

Idealerweise wird mit den Stiftleisten **J2**, **J5**, **J6** und **J7** begonnen, da diese die geringste Bauhöhe aufweisen

!!! note "Hinweise zu den Stiftleisten"
    * Die Stiftleiste **J2** wird nur benötigt, falls ein PTT Taster nicht via Klinkenstecker verbunden werden soll, sondern direkt im Gehäuse verbaut wird.
    * Die Stiftleiste **J7** wird nur benötigt, falls der Taster SW1 aus dem Gehäuse herrausgeführt werden soll. z.B. falls das bt-trx schwer erreichbar verbaut werden soll.
    * Die Stiftleiste **J6** ist eine optionale Herausführung des I2C-Bus des ESP32. Diese wird aktuell nicht verwendet und könnte in Zukunft z.B. für ein Display verwendet werden.

Als nächstes sollte der Taster SW1 aufgelötet werden. Gefolgt von der RJ45 Buchse **J1** und der Klinkenbuchse **J3**. Hier sollte auf ein planes Aufliegen der Buchsen geachtet werden.

Zuguterletzt folgt der ESP32 (**U3**). Die 1x19 Buchsenleisten dienen zum einen zur Erhöhung des ESP32 um den Taster unterhalb unterzubringen, zum anderen kann der ESP zu Entwicklungszwecken aus dem bt-trx leicht entfert werden. 

Um den Lötvorgang so Einfach wie möglich zu gestalten, werden die Buchsenleisten vor dem Verlöten auf den ESP32 gesteckt und so eine senkrechte Montage gewährleistet.

!!! note "Hinweis"
    Die USB-Buchse des ESP32 muss bei der Montage zum Platinenrand hin orientiert sein

![Vollbestückte Platine](bt-trx_assembled_1024.jpg)

## Inbetriebnahme

Zur Erstinbetriebnahme wird das bt-trx Modul mit einem Micro-USB Kabel mit Strom versorgt. 

Nun sollten die bersteinfarbende sowie die blaue LED dauerleuchten.

## Montage des Gehäuses

Nun wird das Modul mit den 2 beiligenden Schrauben im mitgelieferten Gehäuse befestigt. Die Frontplatte muss derzeit noch manuell bearbeitet oder mit einem 3D Drucker [Link einfügen] gefertigt werden.

Nun kann, wenn noch nicht geschehen, das [Anschlusskabel](../Anschlusskabel) und der [PTT-Taster](../PTT-Taster) gefertigt werden.

Die weitere Inbetriebnahme kann nun wie [hier](../../30_Bedienung/Anschluss) beschrieben erfolgen.
