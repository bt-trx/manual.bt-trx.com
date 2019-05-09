# Adapterkabel

Zum Anschluss des bt-trx an das Funkgerät empfiehlt es sich, aus einem
Netzwerkkabel mit RJ45 Stecker ein Adapterkabel zu bauen.

Da die Funkgeräte an der Mikrofonbuchse nicht immer eine passende Versorgungsspannung bzw. -leistung liefern,
kann es erforderlich sein, die Spannung extern zuzuführen (z.B. über Zigarettenanzünder).

bt-trx bietet zwei Möglichkeiten um mit Spannung versorgt zu werden:

- Adapterkabel: V_IN (Pin 7)/GND (Pin 8), 6...20 V DC, ca. 40 mA bei 12 V, oder
- Mikro-USB Buchse

**In den folgenden Tabellen werden immer RJ45 Stecker mit T568B Belegung angenommen!**

## Belegung bt-trx

| Pin | Kürzel | Farbe       | Signal bt-trx |
|:---:|:------:|-------------|---------------|
| 1   | o      | orange/weiß | CAT_TX        |
| 2   | O      | orange      | AUDIO_IN_B    |
| 3   | g      | grün/weiß   | CAT_RX        |
| 4   | B      | blau        | AUDIO_IN_A    |
| 5   | b      | blau/weiß   | PTT           |
| 6   | G      | grün        | AUDIO_OUT     |
| 7   | br     | braun/weiß  | V_IN (6...20 V DC) |
| 8   | BR     | braun       | GND           |

## Belegung Funkgeräte

### Handfunkgeräte (2.5mm und 3.5 mm Klinke)

z.B. Anytone, Baofeng, Kenwood, Wouxun

| Kontakt       | Signal   | Farbe | Signal bt-trx |
|---------------|----------|:-----:|---------------|
| 3.5 mm Tip    | +5V      | --    | --            |
| 3.5 mm Ring   | MIC+     | G     | AUDIO_OUT     |
| 3.5 mm Sleeve | MIC-/PTT | b     | PTT           |
| 2.5 mm Tip    | SPK+     | B     | AUDIO_IN_A    |
| 2.5 mm Ring   | Prog     | --    | --            |
| 2.5 mm Sleeve | SPK-/PTT | BR    | GND           |

Die Spannungsversorgung des bt-trx (br (+)/BR (-)) muss extern zugeführt werden oder
über USB erfolgen.

![Beispiel Adapterkabel mit Klinkenstecker](https://picsum.photos/400/300)  
Beispiel für ein Adapterkabel mit Klinkenstecker

### Kenwood (nicht getestet)

| Pin | Farbe | TM-D700             | TM-D710             | Farbe | Signal bt-trx |
|:---:|:-----:|---------------------|---------------------|:-----:|---------------|
| 1   | o     | DWN                 | Keypard Serial      | --    | --            |
| 2   | O     | --                  | --                  | --    | --            |
| 3   | g     | MIC                 | MIC (600 Ohm)       | G     | AUDIO_OUT     |
| 4   | B     | GND (MIC)           | GND (MIC)           | BR    | --            |
| 5   | b     | STBY (PTT)          | PTT                 | b     | PTT           |
| 6   | G     | GND                 | GND                 | BR    | GND           |
| 7   | br    | 8 V, max. 200 mA    | 8 V, max. 100 mA    | br    | V_IN          |
| 8   | BR    | UP                  | --                  | --    | --            |

TODO: Testen ob der Strom bei 8 V reicht, oder extern zugeführt werden muss.

### ICOM (nicht getestet)

| Pin | Farbe | IC-7000          | Farbe | Signal bt-trx |
|:---:|:-----:|------------------|:-----:|---------------|
| 1   | o     | +8 V, 10 mA max. | --    | --            |
| 2   | O     | UP/DWN           | --    | --            |
| 3   | g     | M8V SW           | --    | --            |
| 4   | B     | PTT              | b     | PTT           |
| 5   | b     | GND (MIC)        | BR    | GND           |
| 6   | G     | MIC              | G     | AUDIO_OUT     |
| 7   | br    | GND              | BR    | GND           |
| 8   | BR    | SQL              | --    | --            |
