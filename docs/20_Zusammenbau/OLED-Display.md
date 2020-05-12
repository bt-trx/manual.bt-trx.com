# OLED-Display

## Allgemeines

Ab der Version 1.1.0 der Firmware wird die Ansteuerung eines OLED Displays
unterstützt. Das Diplay muss einen SH1106 Chipsatz mit 128x64 Pixel Größe
haben. Diese Display sind für kleines Geld bei diversen Lieferanten im
Internet erhältlich.

![SH1106 1.3" OLED Display](OLED_Display.jpg)

## Anschluss

Das Display wird an den I²C pins auf dem dev-board v5.0 angeschlossen. Die
entsprechenden Pins sind auf dem dev Board v5.0 direkt neben dem ESP Modul
herausgeführt. Die Belegung zeigt das folgende Bild:

![I2C Pinbelegung](I2C_Pinout.jpg)

Auf dem folgenden Bild ist das Display verbunden und zeigt das bt-trx Logo
während des Bootvorgangs an.

![OLED Display Boot](Display_verbunden.jpg)

## Einbau

Die Gehäusevariante ohne Batterieschacht bietet ausreichend Platz, um das
OLED Display mit ins Gehäuse einzubauen. Für das Display wird ein kleiner
Ausschnitt gefeilt und das Display selbst mit 4 M3 Senkkopfschrauben
befestigt. Wichtig ist hierbei, die Schrauben nicht zu fest anzuziehen, da
sonst die Platine an den Ecken zu stark gebogen wird.
