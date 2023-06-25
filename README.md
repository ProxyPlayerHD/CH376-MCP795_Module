# RTC-USB_Module
This Module combines the CH376S USB/SD Flash Storage Controller with built-in support for the FAT32 file system, and the MCP795XXX Real Time Clock, in a compact and convienent form factor.

This allows for both File IO and Time keeping using a single module and SPI interface.
#

this project includes all the necessary KiCad files, and even pre-exported Gerbers so anyone can order their own boards from a PCB manufacturer like JLCPCB or PCBWay for example.

A Schematic of the board is included in PDF form, but the connector pinouts are listed below for convenience.

## Main Connector (J2) Pinout:

| Pin | Direction |  Name  | Description |
|-----|-----------|--------|-------------|
|  1  | In        | 5V     | 5V Power |
|  2  | In        | GND    | Ground |
|  3  | In        | SCK    | Clock (SPI) |
|  4  | Out       | ~ACT   | CH376S "Active" signal |
|  5  | In        | MOSI   | Data Input (SPI) |
|  6  | Out       | ~IRQ0  | CH376S Interrupt |
|  7  | Out       | MISO   | Data Output (SPI) |
|  8  | Out       | ~IRQ1  | MCP795 Interrupt |
|  9  | In        | ~SS0   | CH376S Select (SPI) |
|  10 | Out       | ~IRQ2  | MCP795 Watch Dog Interrupt |
|  11 | In        | ~SS1   | MCP795 Select (SPI) |
|  12 | Out       | CLKOUT | MCP795 Programmable Clock Output |

## SD Card Connector (J0) Pinout:

| Pin | Direction |  Name  | Description |
|-----|-----------|--------|-------------|
|  1  | Out       | ~SS    | SD Card Select (SPI) |
|  2  | Out       | SCK    | Clock (SPI) |
|  3  | Out       | MOSI   | Data Output (SPI) |
|  4  | In        | MISO   | Data Input (SPI) |
|  5  | Out       | 5V     | 5V Power |
|  6  | Out       | GND    | Ground |

Note that the J0 pinout is the same as for the common Arduino SD Card Modules. as the intend was to allow people to simply plug one of those in instead of having to make their own SD board/adpater.

