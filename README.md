# E72-2G4M20S1E
Coordinator firmware ZStack 3.x (znp) for E72-2G4M20S1E module (CC2652P)

This firmware built using SimpleLink SDK 6.40.00.13, TI RTOS-7 and TI ARM compiler 3.00 with [patch](https://github.com/Koenkk/Z-Stack-firmware/blob/master/coordinator/Z-Stack_3.x.0/firmware.patch) made by [Koenkk](https://github.com/Koenkk), check [instruction](https://github.com/Koenkk/Z-Stack-firmware/blob/master/coordinator/Z-Stack_3.x.0/COMPILE.md) for more details how to build the firmware.

## Module pins assignment/function

| E72 Pin | Chip   | Function   | Comment                                                 |
|---------|--------|------------|---------------------------------------------------------|
| 1       | GND    |            |                                                         |
| -       | DIO_5  | RF_HIGH_PA | Control RF switch for high power output                 |
| -       | DIO_6  | RF_24GHZ   | Control RF switch for rx/standard power output          |
| 2       | DIO_7  | GREEN_LED  | Switched On when join permited                          |
| 3       | DIO_8  | RED_LED    | In this firmware is not used                            |
| 7       | DIO_12 | UART_RX    | Serial port RX (input)                                  |
| 8       | DIO_13 | UART_TX    | Serial port TX (output)                                 |
| 9       | DIO_14 | BTN1       | In this firmware is not used                            |
| 10      | DIO_15 | FLASH_BTN  | Press during startup to start BSL for firmware update   |
| 13      | TMS    | JTAG_TMS   |                                                         |
| 14      | TCK    | JTAG_TCK   |                                                         |
| 15      | TDO    | JTAG_TDO   |                                                         |
| 16      | TDI    | JTAG_TDI   |                                                         |
| 17      | DIO_18 | RTS        | Hardware flow control. In this firmware is not used     |
| 18      | DIO_18 | CTS        | Hardware flow control. In this firmware is not used     |
| 19      | GND    |            |                                                         |
| 20      | VCC    | 3V3        |                                                         |
| 24      | RST    | RESET      | CC2652P Chip reset button                               |

## UART settings

- Speed: 115200
- flow control: none.
