# Proiect Ariton Alexandru -- TSC -- Openbook


### Pasii de implementare
* Am creat schematicul 2D.
* Am creat PCB-ul, am intampinat niste erori:
    * **Via(hole) error** la componenta USB: am modificat footprint-ul componentei.
    * **Wire to wire error**: am rutat firele manual
* Am atribuit fiecarei componente din library cate un model 3D, si am creat placa 3d (*Push to 3D*)
* Am creat modelele pentru Display si Baterie dupa specificatiile din datasheeturi

### Diagrama block
* salvata in folder cu numele BlockSchematic.png
* Pini ESP32-C6
    * Interfetele SPI -- folosite pentru conectarea la Display
    * Este conectat la senzorul BME688 prin I2C.
    * E conectat la portul USB-C prin interfata USB
    * E conectat la butoane prin porturile GPIO

## Configurație pini ESP32-C6

| Componentă      | Pin ESP32-C6        |
|----------------|---------------------|
| Display SPI    | MOSI, CLK, CS, DC   |
| BME688         | SDA, SCL (I2C)      |
| Butoane        | GPIO1, GPIO2, GPIO3 |
| USB-C          | D+, D−, VBUS        |

![Diagrama Bloc](./BlockSchematic.png)



### Componente Folosite

MCU: ESP32-C6-WROOM-1 (sau echivalent), datorita integrarii Wi-Fi 6, BLE 5 si a puterii de procesare ridicate.
Afisaj: Waveshare WSH-13187, e-Paper de 7.5 inch (sau echivalent), cu rezolutie 800x480.
Senzori: Bosch BME688 – pentru temperatura, umiditate, presiune si calitatea aerului.
Baterie: Baterie Li-Polimer de 2500mAh, cu circuit de protectie integrat.
Indicator nivel baterie (Fuel Gauge): Maxim MAX17048 sau echivalent.
Circuit de incarcare: Microchip MCP73831 sau echivalent.
Butoane: Comutatoare tactile Panasonic EVQ-Q2A03W (sau echivalent).
Conector USB-C: Amphenol 12401641E4R (sau echivalent).
Conector pentru card microSD: Attend Tech 112A-TAAR-R03 (sau echivalent).
Ceas in timp real (RTC): DS3231 (sau echivalent), cu supercapacitor pentru backup.
Conector Qwiic/Stemma: pentru conectarea rapida a senzorilor compatibili.


| Componenta                                      | Link                                                                 |
|------------------------------------------------|----------------------------------------------------------------------|
| adafruit_led                                   | [Link](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?company=Politehnica+University+of+Buch&welcome=home&ref=search&t=LED+0603) |
| Button_customv1                                | [Link](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k) |
| Eagle_ltspice_c                                | [Link](https://componentsearchengine.com/part-view/0402WGF3001TCE/UNI-ROYAL(Uniroyal%20Elec)) |
| ESP32_WROVER_AVX—SD0805S020S1R0                | [Link](https://ro.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D) |
| ESP32_WROVER_BME680_BME680                     | [Link](https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home) |
| ESP32_WROVER_EAGLE-LTSPICE_R                   | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) |
| RCL_CPOL-EU                                    | [Link](https://www.snapeda.com/parts/TAJB475K025RNJ/AVX/view-part/?t=capacitor%203528&con_ref=None) |
| SJ                                             | [Link](https://grabcad.com/library/solder-jumpers-1) |
| R-URI                                          | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) |
| ESP32_WROVER_SPARKFUN-DISCRETESEMI_MOSFET_PCH | [Link](https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated) |
| ESP32_WROVER_SPARKFUN-IC-POWER_MCP73831       | [Link](https://eu.mouser.com/ProductDetail/Microchip-Technology/MCP73831T-2ACI-OT?qs=yUQqVecv4qvbBQBGbHx0Mw%3D%3D) |
| TP                                             | Facut Manual |
| FH34SRJ-24S-0.5SH_99_                          | [Link](https://componentsearchengine.com/part-view/FH34SRJ-24S-0.5SH(99)/Hirose) |
| MAX17048G+T10                                  | [Link](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/) |
| SAMACSYS_PARTS_USB4110-GF-A                    | [Link](https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY)) |
| QWIIC_CONNECTOR                                | [Link](https://www.snapeda.com/parts/PRT-14417/SparkFun%20Electronics/view-part/?t=QWIIC_CONNECTORJS-1MM) |
| 112A-TAAR-R03_ATTEND                           | [Link](https://componentsearchengine.com/part-view/112A-TAAR-R03%20ATTEND/ATTEND) |
| 744043680IND_4828-WE-TPC_WRE                   | [Link](https://componentsearchengine.com/part-view/744043680/W%C3%BCrth%20Elektronik) |
| BD5229G-TR                                     | [Link](https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor) |
| CPH3225A                                       | [Link](https://componentsearchengine.com/part-view/CPH3225A/Seiko%20Semiconductors) |
| DS3231SN#                                      | [Link](https://componentsearchengine.com/part-view/DS3231SN%23/Analog%20Devices) |
| ESP32-C6-WROOM-1-N8                            | [Link](https://componentsearchengine.com/part-view/ESP32-C6-WROOM-1-N8/Espressif%20Systems) |
| MBR0530                                        | [Link](https://componentsearchengine.com/part-view/MBR0530/onsemi) |
| SI1308EDL-T1-GE3                               | [Link](https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay) |
| USBLC6-2SC6Y                                   | [Link](https://componentsearchengine.com/part-view/USBLC6-2SC6Y/STMicroelectronics) |
| W25Q512JVEIQ                                   | [Link](https://componentsearchengine.com/part-view/W25Q512JVEIQ/Winbond) |
| XC6220A331MR-G                                 | [Link](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex) |

