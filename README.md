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
| TP                                             | [Link](https://ro.mouser.com/ProductDetail/Adafruit/3825?qs=%252BEew9%252B0nqrAn6n76%252BB5vZg%3D%3D) |
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

adafruit_led: 
[https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?company=Politehnica+University+of+Buch&amp;welcome=home&amp;ref=search&amp;t=LED+0603](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?company=Politehnica+University+of+Buch&amp;welcome=home&amp;ref=search&amp;t=LED+0603)

Button_customv1:
[https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k)

Eagle_ltspice_c: 
[https://componentsearchengine.com/part-view/0402WGF3001TCE/UNI-ROYAL(Uniroyal Elec)](https://componentsearchengine.com/part-view/0402WGF3001TCE/UNI-ROYAL\(Uniroyal%20Elec\))

ESP32_WROVER_AVX—SD0805S020S1R0_AVX_SD0805S020S1R0_0_0: 
[https://ro.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D&_gl=1*9xzrwp*_ga*MTA0NjQwOTgyNi4xNzQzNDg4MTg0*_ga_15W4STQT4T*MTc0MzQ4ODE4NC4xLjEuMTc0MzQ4ODU1My41Ny4wLjA](https://ro.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D&_gl=1*9xzrwp*_ga*MTA0NjQwOTgyNi4xNzQzNDg4MTg0*_ga_15W4STQT4T*MTc0MzQ4ODE4NC4xLjEuMTc0MzQ4ODU1My41Ny4wLjA).

ESP32_WROVER_BME680_BME680: 
[https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home](https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home)

ESP32_WROVER_EAGLE-LTSPICE_R:
[https://componentsearchengine.com/part-view/R0402 1%25 100 K (RC0402FR-07100KL)/YAGEO](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20\(RC0402FR-07100KL\)/YAGEO)

RCL_CPOL-EU: 
[https://www.snapeda.com/parts/TAJB475K025RNJ/AVX/view-part/?t=capacitor 3528&con_ref=None](https://www.snapeda.com/parts/TAJB475K025RNJ/AVX/view-part/?t=capacitor%203528&con_ref=None)

SJ:
[https://grabcad.com/library/solder-jumpers-1](https://grabcad.com/library/solder-jumpers-1)

R-URI:
[https://componentsearchengine.com/part-view/R0402 1%25 100 K (RC0402FR-07100KL)/YAGEO](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20\(RC0402FR-07100KL\)/YAGEO)

ESP32_WROVER_SPARKFUN-DISCRETESEMI_MOSFET_PCH:
[https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes Incorporated](https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated)

ESP32_WROVER_SPARKFUN-IC-POWER_MCP73831:
[https://eu.mouser.com/ProductDetail/Microchip-Technology/MCP73831T-2ACI-OT?qs=yUQqVecv4qvbBQBGbHx0Mw%3D%3D](https://eu.mouser.com/ProductDetail/Microchip-Technology/MCP73831T-2ACI-OT?qs=yUQqVecv4qvbBQBGbHx0Mw%3D%3D)

TP:
[https://ro.mouser.com/ProductDetail/Adafruit/3825?qs=%252BEew9%252B0nqrAn6n76%252BB5vZg%3D%3D](https://ro.mouser.com/ProductDetail/Adafruit/3825?qs=%252BEew9%252B0nqrAn6n76%252BB5vZg%3D%3D)

FH34SRJ-24S-0.5SH_99_:
[https://componentsearchengine.com/part-view/FH34SRJ-24S-0.5SH(99)/Hirose](https://componentsearchengine.com/part-view/FH34SRJ-24S-0.5SH\(99\)/Hirose)

MAX17048G+T10:
[https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/)

SAMACSYS_PARTS_USB4110-GF-A:
[https://componentsearchengine.com/part-view/USB4110-GF-A/GCT (GLOBAL CONNECTOR TECHNOLOGY)](https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20\(GLOBAL%20CONNECTOR%20TECHNOLOGY\))

QWIIC_CONNECTOR:
[https://www.snapeda.com/parts/PRT-14417/SparkFun Electronics/view-part/?t=QWIIC_CONNECTORJS-1MM](https://www.snapeda.com/parts/PRT-14417/SparkFun%20Electronics/view-part/?t=QWIIC_CONNECTORJS-1MM)

112A-TAAR-R03_ATTEND:
[https://componentsearchengine.com/part-view/112A-TAAR-R03%20ATTEND/ATTEND](https://componentsearchengine.com/part-view/112A-TAAR-R03%20ATTEND/ATTEND)

744043680IND_4828-WE-TPC_WRE:
[https://componentsearchengine.com/part-view/744043680/W%C3%BCrth%20Elektronik](https://componentsearchengine.com/part-view/744043680/W%C3%BCrth%20Elektronik)

BD5229G-TR:
[https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor](https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor)

CPH3225A:
[https://componentsearchengine.com/part-view/CPH3225A/Seiko%20Semiconductors](https://componentsearchengine.com/part-view/CPH3225A/Seiko%20Semiconductors)

DS3231SN#:
[https://componentsearchengine.com/part-view/DS3231SN%23/Analog%20Devices](https://componentsearchengine.com/part-view/DS3231SN%23/Analog%20Devices)

ESP32-C6-WROOM-1-N8:
[https://componentsearchengine.com/part-view/ESP32-C6-WROOM-1-N8/Espressif%20Systems](https://componentsearchengine.com/part-view/ESP32-C6-WROOM-1-N8/Espressif%20Systems)

FH34SRJ-24S-0.5SH_99_:
[https://componentsearchengine.com/part-view/FH34SRJ-24S-0.5SH(99)/Hirose](https://componentsearchengine.com/part-view/FH34SRJ-24S-0.5SH(99)/Hirose)

MAX17048G+T10:
[https://componentsearchengine.com/part-view/MAX17048G%2BT10/Analog%20Devices](https://componentsearchengine.com/part-view/MAX17048G%2BT10/Analog%20Devices)

MBR0530:
[https://componentsearchengine.com/part-view/MBR0530/onsemi](https://componentsearchengine.com/part-view/MBR0530/onsemi)

SI1308EDL-T1-GE3:
[https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay](https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay)

USBLC6-2SC6Y:
[https://componentsearchengine.com/part-view/USBLC6-2SC6Y/STMicroelectronics](https://componentsearchengine.com/part-view/USBLC6-2SC6Y/STMicroelectronics)

W25Q512JVEIQ:
[https://componentsearchengine.com/part-view/W25Q512JVEIQ/Winbond](https://componentsearchengine.com/part-view/W25Q512JVEIQ/Winbond)

XC6220A331MR-G:
[https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex)
