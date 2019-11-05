# Hardware

## Entwicklungsumgebung 

Der Schaltplan sowie das PCB wurden mit KiCAD (Version 5.1) enwickelt.

## Schaltplan und PCB

Die PDF zum dev-board v4.1 können hier runtergeladen werden

* [Schaltplan](./schematic_v4_1.pdf)
* [PCB](./pcb_v4_1.pdf)

## Testpunkte

Die folgenden Testpunkte können z.B. zum Einstellen von Pegeln verwendet werden.

* **TP1** *J1* - Audio B IN
* **TP2** *WT32i* - SPK_LN
* **TP3** *WT32i* - SPK_LP
* **TP4** *WT32i* - MIC_LP
* **TP5** *WT32i* - MIC_LN
* **TP6** *J1* - Audio OUT
* **TP7** *J1* - Audio A IN
* **TP8** GND

## Trimmer

* **RV1** Pegel Audio B IN
* **RV2** Pegel Audio OUT (im Kit nicht bestückt!)
* **RV3** Pegel Audio A IN

## Lötbrücken

* **JP1** Enable Audio B (im Kit nicht gesetzt)
* **JP2** Brücke wenn RV2 nicht bestückt (im Kit gesetzt)
* **JP3** Brücke von Audio A/B zum AD Eingang ESP32 (im Kit nicht gesetzt)
* **JP4** Enable PTT Pullup (im Kit gesetzt)

## Interne Sockel

* **J2** PTT Button
* **J5** Jumper für PTT OUT
    * µC: ESP32 setzt PTT (standard)
    * BTN: BTT Button wird direkt zum Funkgerät druchgeschleift
* **J6** I²C Bus ESP32 (wird aktuell nicht verwendet)
* **J7** Anschluss für SW1, falls dieser nach außen geführt werden muss.