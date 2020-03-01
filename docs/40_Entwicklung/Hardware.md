# Hardware

## Entwicklungsumgebung 

Der Schaltplan sowie das PCB wurden mit KiCAD (Version 5.1) enwickelt.

## Schaltplan und PCB

Die PDF zum dev-board v5.0 können hier runtergeladen werden

* [Schaltplan](./schematic_v5_0.pdf)
* [PCB top Layer](./pcb_v5_0_top.pdf)
* [PCB bottom Layer](./pcb_v5_0_bottom.pdf)


## Testpunkte

Die folgenden Testpunkte können z.B. zum Einstellen von Pegeln verwendet werden.

* **TP1** MIC GND
* **TP2** *WT32i* - SPK_LN
* **TP3** *WT32i* - SPK_LP
* **TP4** *WT32i* - MIC_LP
* **TP5** *WT32i* - MIC_LN
* **TP6** *J1* - MIC (Audio OUT)
* **TP7** *J1* - SPK (Audio IN)
* **TP8** TRX GND
* **TPp** PWR GND

## Trimmer

* **RV2** Pegel MIC (Audio OUT) (im Kit nicht bestückt!)
* **RV3** Pegel SPK (Audio  IN)

## Lötbrücke

* **JP1** Brücke wenn RV2 nicht bestückt (im Kit gesetzt)

## Interne Sockel

* **J2** PTT Button
* **J5** Jumper für PTT OUT
    * µC: ESP32 setzt PTT (standard)
    * BTN: BTT Button wird direkt zum Funkgerät druchgeschleift
* **J6** I²C Bus ESP32 (wird aktuell nicht verwendet)
* **J7** Anschluss für SW1, falls dieser nach außen geführt werden muss
* **J8** Zusätzliche Serielle Schnittstelle zum ESP (3.3V Pegel) für z.B. CAT
* **J9** Sockel für Jumper Modul, WT32i seitig
* **J10** Sockel für Jumper Modul, TRX seitig
* **J11** Herausführung des ADC Pins des ESP, für zukünftige Erweiterungen (z.B. Squelch)
* **J12** Abgriff des Audio IN Signals, für zukünftige Erweiterungen (z.B. Squelch)