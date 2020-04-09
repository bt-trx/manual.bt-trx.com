# Software

## Entwicklungsumgebung

Die ESP32 Firmware ist in C++ mit dem Arduino-Framework geschrieben.
Als Build-Umgebung wird PlatformIO verwendet
(z.B. Visual Studio Code mit PlatformIO Plugin).

### Erstellen eines Firmware Binaries

Downloaden des Quellcodes von [Github](https://github.com/bt-trx/firmware/releases)
oder clonen des Repositories mit

```bash
git clone https://github.com/bt-trx/firmware.git
```

Danach wechseln in das Verzeichnis des Quellcodes und compilieren der Firmware

```bash
cd firmware
platformio run
```

Das erstelle Firmware-Binary ist dann unter `.pio/build/esp/firmware.bin`
zu finden.
Alternativ kann die Firmware direkt auf einen angesteckten ESP32 geladen werden:

```bash
platformio run --target upload
```

Falls der voreingestellte Port für den CP2102 nicht stimmt, kann ein anderer 
Port mittels Paramter übergeben werden. Zum Beispiel:

```bash
platformio run --target upload --upload-port /dev/ttyUSB4
```

## Styleguide

Es sollte sich an den Google-Styleguide für C++ gehalten werden.
Die Code-Formatierung wird mittels clang-format automatisch gewartet:
`./tools/code-style.sh src/*.cpp src/*.h`

## Unit-Tests

Die Unit-Tests für die Software sind mittels gtest umgesetzt. Zur Abstrahierung
der Hardware-Aufrufe werden gmock Mockups verwendet.

Die Tests werden mit `./test/build.sh` durchgeführt.
