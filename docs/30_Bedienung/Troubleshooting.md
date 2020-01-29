# Troubleshooting

## dev-board v4.1

### PTT auf Dauersendung wenn bt-trx stromlos ist

Bei manchen Funkgeräten (z.B. Yaesu FTM-350, Yaesu FT-8800)
wird PTT auf Dauer-An interpretiert, sobald bt-trx stromlos ist.
Dies kann behoben werden, indem bei der PTT Leitung ein 27 kOhm Widerstand in
Reihe geschaltet wird. Dies sollte bei allen Geräten mit MC-48 Abhilfe schaffen.
(Danke, Dirk!)

### Störgeräusch/Brummen auf Tx NF Audio

Bei manchen Funkgeräten bzw. Setups kann es bei der Tx NF Audio zu
Störgeräuschen kommen. Folgende Punkte können einzeln oder in Kombination für
Abhilfe sorgen:

* Versorgung über USB (ggf. aus Akkupack)
* Separate Masseleitung von TP8 (Audio-Out Gnd) zum Transceiver-Gehäuse
* Separate Verkabelung von PTT über Relais/Optokoppler
