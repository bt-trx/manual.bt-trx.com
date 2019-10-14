# Software

## Entwicklungsumgebung 

Die ESP32 Firmware ist in C++ mit dem Arduino-Framework geschrieben.
Als Build-Umgebung wird PlatformIO verwendet
(z.B. Visual Studio Code mit PlatformIO Plugin).

## Styleguide

Es sollte sich an den Google-Styleguide für C++ gehalten werden.
Die Code-Formatierung wird mittels clang-format automatisch gewartet:
`./tools/code-style.sh src/*.cpp src/*.h`

## Unit-Tests

Die Unit-Tests für die Software sind mittels gtest umgesetzt. Zur Abstrahierung
der Hardware-Aufrufe werden gmock Mockups verwendet.

Die Tests werden mit `./test/build.sh` durchgeführt.
