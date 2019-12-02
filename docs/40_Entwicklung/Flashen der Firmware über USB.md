
# Flashen der Firmware über USB

Zum erstmaligen Aufspielen der Partitionstabelle und der Firmware auf einen ESP32.

Das erstmalige Aufspielen der Firmware auf den ESP32 Controller **muss** über
USB erfolgen, da die Partitionstabelle nur über USB geschrieben werden kann.
Alle weiteren Updates können über das
[Webinterface](../30_Bedienung/Firmware-Update.md) erfolgen.

Bei den ESP32 in den Bausätzen ist die Partitionstabelle und die aktuellste
verfügbare Firmware bereits aufgespielt. Updates können über
das [Webinterface](../30_Bedienung/Firmware-Update.md) erfolgen und untenstehende
Schritte sind **nicht** notwendig.

## Windows

1. Herunterladen der aktuellen bt-trx Dateien von
   [Github](https://github.com/bt-trx/firmware/releases/).  
   Für das initiale Aufspielen ist die Partitions-Datei und die Firmware-Datei
   notwendig  
   (z.B. _bt-trx_partitions_0.3.0.bin_ und _bt-trx_firmware_0.3.0.bin_).
2. Download des ESP32 Flashtools von der
   [espressif Homepage](https://www.espressif.com/en/products/hardware/esp32/resources)
   (Direktlink: [Version 3.6.7](
   https://www.espressif.com/sites/default/files/tools/flash_download_tools_v3.6.7_1.zip))

3. Anschließen des ESP32 mit Micro-USB-Kabel an den Computer

4. Starten des Tools im "ESP32 Download" Modus

5. Einstellen folgender Parameter im Reiter "SPIDownload":

    ![Einstellungen ESP32 Flashtool 3.6.6](ESP32_FlashTool_Settings.png)

    1. Einstellen der hochzuladenden Dateien und der Zieladressen, sowie
       Ankreuzen der der beiden Zeilen.  
       Die Partitions-Datei muss auf Adresse **0x8000** geschrieben werden.  
       Die Firmware-Datei muss auf Adresse **0x10000** geschrieben werden.  
       Zum Beispiel:  
       _[x] bt-trx_esp32_partitions_0.3.0.bin @ 0x8000_  
       _[x] bt-trx_esp32_firmware_0.3.0.bin @ 0x010000_
    2. SPI Speed: 80 MHz
    3. COM-Port des ESP32 einstellen, Baudrate: 460800
    4. Mit Klick auf "START" beginnt der Flashvorgang.
  
    Der Fortschritt wird mit einem grünen Balken angezeigt.  
    Nach Ende des Flashvorgangs wird "FINISHED" angezeigt.
