# Stromverbrauch

!!! note "Hinweis"
    Diese Daten beziehen sich auf die Firmware Version 0.2.1.

Aktuell sind noch keine stromsparenden Maßnahmen in der Firmware integriert.
Die Leistungsaufnahme beträgt ca. 500 mW.

Die Messungen für 5 V, 12 V, 13.8 V wurden über die RJ45 Buchse durchgeführt.  
Bei ESP32-USB wurde bt-trx über USB versorgt.

| Modus           | 5 V | 12 V | 13.8 V | ESP32-USB (5.1V) |
|-----------------|:---:|:----:|:------:|:----------------:|
| Booten          |  -- |  101 |  --    |  --              |
| Idle            |  69 |   70 |  73    |  74              |
| Idle + Wifi     |  -- |  147 |  --    |  --              |
| BT Suche        |  94 |   96 |  97    | 100              |
| BT Verbunden    |  78 |   81 |  82    |  86              |
| Telefongespräch | 100 |  101 | 102    | 106              |
| ||||                                     Alle Werte in mA|
