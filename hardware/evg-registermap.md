## EVG Function Register Map

The EVM module can be configured for use as an Event Generator (EVG) or a fanout/concentrator.

This is the register map when EVM is configured as an EVG.


| Address |  Register | Type | Description |
| ------- | --------- | ---- | ----------- |
| 0x000 | Status | UINT32 | [Status Register](#status-register) |
| 0x004 | Control | UINT32 | [Control Register](#control-register) |
| 0x008 | IrqFlag | UINT32 | [Interrupt Flag Register](#interrupt-flag-register) |
| 0x00C | IrqEnable | UINT32 | [Interrupt Enable Register](#interrupt-enable-register) |
| 0x010 | ACControl | UINT32 | [AC divider control](#ac-trigger-control-register)
| 0x014 | ACMap | UINT32 | [AC trigger event mapping](#ac-trigger-mapping-register)
| 0x018 | SWEvent | UINT32 | [Software event Register](#software-event-register) |
| 0x01C | PCIMasterIrqEnable | UINT32 | [PCI Master Interrupt Enable Register](#pci-master-interrupt-enable-register) |
| 0x020 | DataBufControl | UINT32 | [Data Buffer Control Register](#data-buffer-control-register) |
| 0x024 | DBusMap | UINT32 | [Distributed Bus Mapping Register](#distributed-bus-mapping-register) |
| 0x028 | DBusEvents | UINT32 | [Distributed Bus Timestamping Events Register](#distributed-bus-event-enable-register) |
| 0x02C | FWVersion | UINT32 | [Firmware Version Register](#fpga-firmware-version-register) |
| 0x030 | SegBufControl | UINT32 | [Segmented Data Buffer Control Register](#segmented-data-buffer-control-register) |
| 0x034 | TSControl | UINT32 | [Timestamp event generator control Register](#timestamp-generator-control-register) |
| 0x038 | TSValue | UINT32 | Timestamp event generator value Register |
| 0x040 | FPInput | UINT32 | Front Panel Input state Register |
| 0x044 | UnivInput | UINT32 | Universal Input state Register |
| 0x048 | TBInput | UINT32 | Transition Board Input state Register |
| 0x04C | UsecDivider | UINT32 | [Divider to get from Event Clock to 1 MHz](#microsecond-divider-register)
| 0x050 | ClockControl | UINT32 | [Event Clock Control Register](#clock-control-register) |
| 0x060 | EvanControl | UINT32 | [Event Analyser Control Register](#event-analyser-control-register) |
| 0x064 | EvanCode | UINT32 | Event Analyser Distributed Bus and Event Code Register |
| 0x068 | EvanTimeHigh | UINT32 | Event Analyser Time Counter (bits 63 – 32)
| 0x06C | EvanTimeLow | UINT32 | Event Analyser Time Counter (bits 31 – 0)
| 0x070 | SeqRamCtrl0 | UINT32 | [Sequence RAM 0 Control Register](#sequence-ram-control-registers) |
| 0x074 | SeqRamCtrl1 | UINT32 | [Sequence RAM 1 Control Register](#sequence-ram-control-registers) |
| 0x080 | FracDiv | UINT32 | [Micrel SY87739L Fractional Divider Configuration Word](#sy87739l-fractional-divider-configuration-word)
| 0x0A0 | SPIData | UINT32 | [SPI Data Register](#spi-configuration-flash-registers) |
| 0x0A4 | SPIControl | UINT32 | [SPI Control Register](#spi-configuration-flash-registers) |
| 0x100 | EvTrig0 | UINT32 | [Event Trigger 0 Register](#event-trigger-registers) |
| 0x104 | EvTrig1 | UINT32 | Event Trigger 1 Register |
| 0x108 | EvTrig2 | UINT32 | Event Trigger 2 Register |
| 0x10C | EvTrig3 | UINT32 | Event Trigger 3 Register |
| 0x110 | EvTrig4 | UINT32 | Event Trigger 4 Register |
| 0x114 | EvTrig5 | UINT32 | Event Trigger 5 Register |
| 0x118 | EvTrig6 | UINT32 | Event Trigger 6 Register |
| 0x11C | EvTrig7 | UINT32 | Event Trigger 7 Register |
| 0x180 | MXCCtrl0 | UINT32  | [Multiplexed Counter 0 Control Register](#multiplexed-counter-registers) |
| 0x184 | MXCPresc0 | UINT32 | Multiplexed Counter 0 Prescaler Register |
| 0x188 | MXCCtrl1 | UINT32  | Multiplexed Counter 1 Control Register |
| 0x18C | MXCPresc1 | UINT32 | Multiplexed Counter 1 Prescaler Register |
| 0x190 | MXCCtrl2 | UINT32  | Multiplexed Counter 2 Control Register |
| 0x194 | MXCPresc2 | UINT32 | Multiplexed Counter 2 Prescaler Register |
| 0x198 | MXCCtrl3 | UINT32  | Multiplexed Counter 3 Control Register |
| 0x19C | MXCPresc3 | UINT32 | Multiplexed Counter 3 Prescaler Register |
| 0x1A0 | MXCCtrl4 | UINT32  | Multiplexed Counter 4 Control Register |
| 0x1A4 | MXCPresc4 | UINT32 | Multiplexed Counter 4 Prescaler Register |
| 0x1A8 | MXCCtrl5 | UINT32  | Multiplexed Counter 5 Control Register |
| 0x1AC | MXCPresc5 | UINT32 | Multiplexed Counter 5 Prescaler Register |
| 0x1B0 | MXCCtrl6 | UINT32  | Multiplexed Counter 6 Control Register |
| 0x1B4 | MXCPresc6 | UINT32 | Multiplexed Counter 6 Prescaler Register |
| 0x1B8 | MXCCtrl7 | UINT32  | Multiplexed Counter 7 Control Register |
| 0x1BC | MXCPresc7 | UINT32 | Multiplexed Counter 7 Prescaler Register |
| 0x400 | FPOutMap0 | UINT16 | Front Panel Output 0 Mapping Register |
| 0x402 | FPOutMap1 | UINT16 | Front Panel Output 1 Mapping Register |
| 0x404 | FPOutMap2 | UINT16 | Front Panel Output 2 Mapping Register |
| 0x406 | FPOutMap3 | UINT16 | Front Panel Output 3 Mapping Register |
| 0x420 | BPOutMap0 | UINT16 | Backplane Output 0 Mapping Register   |
| 0x422 | BPOutMap1 | UINT16 | Backplane Output 1 Mapping Register   |
| 0x424 | BPOutMap2 | UINT16 | Backplane Output 2 Mapping Register   |
| 0x426 | BPOutMap3 | UINT16 | Backplane Output 3 Mapping Register   |
| 0x428 | BPOutMap4 | UINT16 | Backplane Output 4 Mapping Register   |
| 0x42A | BPOutMap5 | UINT16 | Backplane Output 5 Mapping Register   |
| 0x42C | BPOutMap6 | UINT16 | Backplane Output 6 Mapping Register   |
| 0x42E | BPOutMap7 | UINT16 | Backplane Output 7 Mapping Register   |
| 0x440 | UnivOutMap0 | UINT16 | Universal Output 0 Mapping Register |
| 0x442 | UnivOutMap1 | UINT16 | Universal Output 1 Mapping Register |
| 0x444 | UnivOutMap2 | UINT16 | Universal Output 2 Mapping Register |
| 0x446 | UnivOutMap3 | UINT16 | Universal Output 3 Mapping Register |
| 0x448 | UnivOutMap4 | UINT16 | Universal Output 4 Mapping Register |
| 0x44A | UnivOutMap5 | UINT16 | Universal Output 5 Mapping Register |
| 0x44C | UnivOutMap6 | UINT16 | Universal Output 6 Mapping Register |
| 0x44E | UnivOutMap7 | UINT16 | Universal Output 7 Mapping Register |
| 0x450 | UnivOutMap8 | UINT16 | Universal Output 8 Mapping Register |
| 0x452 | UnivOutMap9 | UINT16 | Universal Output 9 Mapping Register |
| 0x454 | UnivOutMap10 | UINT16 | Universal Output 10 Mapping Register |
| 0x456 | UnivOutMap11 | UINT16 | Universal Output 11 Mapping Register |
| 0x458 | UnivOutMap12 | UINT16 | Universal Output 12 Mapping Register |
| 0x45A | UnivOutMap13 | UINT16 | Universal Output 13 Mapping Register |
| 0x45C | UnivOutMap14 | UINT16 | Universal Output 14 Mapping Register |
| 0x45E | UnivOutMap15 | UINT16 | Universal Output 15 Mapping Register |
| 0x480 | TBOutMap0 | UINT16 | [Transition Board Output 0 Mapping Register](#transition-board-output-mapping-registers) |
| 0x482 | TBOutMap1 | UINT16 | Transition Board Output 1 Mapping Register |
| 0x484 | TBOutMap2 | UINT16 | Transition Board Output 2 Mapping Register |
| 0x486 | TBOutMap3 | UINT16 | Transition Board Output 3 Mapping Register |
| 0x488 | TBOutMap4 | UINT16 | Transition Board Output 4 Mapping Register |
| 0x48A | TBOutMap5 | UINT16 | Transition Board Output 5 Mapping Register |
| 0x48C | TBOutMap6 | UINT16 | Transition Board Output 6 Mapping Register |
| 0x48E | TBOutMap7 | UINT16 | Transition Board Output 7 Mapping Register |
| 0x490 | TBOutMap8 | UINT16 | Transition Board Output 8 Mapping Register |
| 0x492 | TBOutMap9 | UINT16 | Transition Board Output 9 Mapping Register |
| 0x494 | TBOutMap10 | UINT16 | Transition Board Output 10 Mapping Register |
| 0x496 | TBOutMap11 | UINT16 | Transition Board Output 11 Mapping Register |
| 0x498 | TBOutMap12 | UINT16 | Transition Board Output 12 Mapping Register |
| 0x49A | TBOutMap13 | UINT16 | Transition Board Output 13 Mapping Register |
| 0x49C | TBOutMap14 | UINT16 | Transition Board Output 14 Mapping Register |
| 0x49E | TBOutMap15 | UINT16 | Transition Board Output 15 Mapping Register |
| 0x500 | FPInMap0 | UINT32 | [Front Panel Input 0 Mapping Register](#front-panel-input-mapping-registers) |
| 0x504 | FPInMap1 | UINT32 | Front Panel Input 1 Mapping Register (VME only) |
| 0x508 | FPInMap2 | UINT32 | Front Panel Input 2 Mapping Register (VME only) |
| 0x520 | FPPhMon0 | UINT32 | [Front Panel Input 0 Phase Monitoring Register](#front-panel-input-phase-monitoring-registers) |
| 0x524 | FPPhMon1 | UINT32 | Front Panel Input 1 Phase Monitoring Register (VME only)|
| 0x528 | FPPhMon2 | UINT32 | Front Panel Input 2 Phase Monitoring Register (VME only)|
| 0x540 | UnivInMap0 | UINT32 | [Universal Input 0 Map Register](#universal-input-mapping-registers) |
| 0x544 | UnivInMap1 | UINT32 | Universal Input 1 Map Register |
| 0x548 | UnivInMap2 | UINT32 | Universal Input 2 Map Register |
| 0x54C | UnivInMap3 | UINT32 | Universal Input 3 Map Register |
| 0x550 | UnivInMap4 | UINT32 | Universal Input 4 Map Register |
| 0x554 | UnivInMap5 | UINT32 | Universal Input 5 Map Register |
| 0x558 | UnivInMap6 | UINT32 | Universal Input 6 Map Register |
| 0x55C | UnivInMap7 | UINT32 | Universal Input 7 Map Register |
| 0x560 | UnivInMap8 | UINT32 | Universal Input 8 Map Register |
| 0x564 | UnivInMap9 | UINT32 | Universal Input 9 Map Register |
| 0x568 | UnivInMap10 | UINT32 | Universal Input 10 Map Register |
| 0x56C | UnivInMap11 | UINT32 | Universal Input 11 Map Register |
| 0x570 | UnivInMap12 | UINT32 | Universal Input 12 Map Register |
| 0x574 | UnivInMap13 | UINT32 | Universal Input 13 Map Register |
| 0x578 | UnivInMap14 | UINT32 | Universal Input 14 Map Register |
| 0x57C | UnivInMap15 | UINT32 | Universal Input 15 Map Register |
| 0x580 | BPInMap0 | UINT32 | Backplane Input 0 Map Register |
| 0x584 | BPInMap1 | UINT32 | Backplane Input 1 Map Register |
| 0x588 | BPInMap2 | UINT32 | Backplane Input 2 Map Register |
| 0x58C | BPInMap3 | UINT32 | Backplane Input 3 Map Register |
| 0x590 | BPInMap4 | UINT32 | Backplane Input 4 Map Register |
| 0x594 | BPInMap5 | UINT32 | Backplane Input 5 Map Register |
| 0x598 | BPInMap6 | UINT32 | Backplane Input 6 Map Register |
| 0x59C | BPInMap7 | UINT32 | Backplane Input 7 Map Register |
| 0x600 | TBInMap0 | UINT32 | [Transition Board Input 0 Mapping Register](#transition-board-input-mapping-registers) |
| 0x604 | TBInMap1 | UINT32 | Transition Board Input 1 Mapping Register |
| 0x608 | TBInMap2 | UINT32 | Transition Board Input 2 Mapping Register |
| 0x60C | TBInMap3 | UINT32 | Transition Board Input 3 Mapping Register |
| 0x610 | TBInMap4 | UINT32 | Transition Board Input 4 Mapping Register |
| 0x614 | TBInMap5 | UINT32 | Transition Board Input 5 Mapping Register |
| 0x618 | TBInMap6 | UINT32 | Transition Board Input 6 Mapping Register |
| 0x61C | TBInMap7 | UINT32 | Transition Board Input 7 Mapping Register |
| 0x620 | TBInMap8 | UINT32 | Transition Board Input 8 Mapping Register |
| 0x624 | TBInMap9 | UINT32 | Transition Board Input 9 Mapping Register |
| 0x628 | TBInMap10 | UINT32 | Transition Board Input 10 Mapping Register |
| 0x62C | TBInMap11 | UINT32 | Transition Board Input 11 Mapping Register |
| 0x630 | TBInMap12 | UINT32 | Transition Board Input 12 Mapping Register |
| 0x634 | TBInMap13 | UINT32 | Transition Board Input 13 Mapping Register |
| 0x638 | TBInMap14 | UINT32 | Transition Board Input 14 Mapping Register |
| 0x63C | TBInMap15 | UINT32 | Transition Board Input 15 Mapping Register |
| 0x800 – 0xFFF  | DataBuf | | Data Buffer Transmit Memory |
| 0x1000 – 0x10FF | configROM | |
| 0x1100 – 0x11FF | scratchRAM | |
| 0x1200 – 0x12FF | SFPEEPROM | | Upstream SFP Transceiver EEPROM contents (SFP address 0xA0) |
| 0x1300 – 0x13FF | SFPDIAG | | Upstream SFP Transceiver diagnostics (SFP address 0xA2) |
| 0x2000 – 0x27FF | SegBuf | | Segmented Data Buffer Transmit Memory |
| 0x8000 – 0xBFFF | SeqRam0 | | Sequence RAM 0 |
| 0xC000 – 0xFFFF | SeqRam1 | | Sequence RAM 1 |

### Register descriptions

#### Status Register

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
|0x000    | RDB7 | RDB6 | RDB5 |  RDB4 | RDB3 |  RDB2 | RDB1 | RDB0 |
|         | **bit 23** | **bit 22** | **bit 21** | **bit 20** | **bit 19** | **bit 18** | **bit 17** | **bit 16** |
| 0x001   | TDB7 | TDB6 | TDB5 | TDB4 | TDB3 | TDB2 | TDB1 | TDB0 |

| Bit | Function |
| --- | -------- |
| RDB7 | Status of received distributed bus bit 7 (from upstream EVG) |
| RDB6 | Status of received distributed bus bit 6 (from upstream EVG) |
| RDB5 | Status of received distributed bus bit 5 (from upstream EVG) |
| RDB4 | Status of received distributed bus bit 4 (from upstream EVG) |
| RDB3 | Status of received distributed bus bit 3 (from upstream EVG) |
| RDB2 | Status of received distributed bus bit 2 (from upstream EVG) |
| RDB1 | Status of received distributed bus bit 1 (from upstream EVG) |
| RDB0 | Status of received distributed bus bit 0 (from upstream EVG) |
| TDB7 | Status of transmitted distributed bus bit 7 |
| TDB6 | Status of transmitted distributed bus bit 6 |
| TDB5 | Status of transmitted distributed bus bit 5 |
| TDB4 | Status of transmitted distributed bus bit 4 |
| TDB3 | Status of transmitted distributed bus bit 3 |
| TDB2 | Status of transmitted distributed bus bit 2 |
| TDB1 | Status of transmitted distributed bus bit 1 |
| TDB0 | Status of transmitted distributed bus bit 0 |

#### Control Register

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x004   | EVGEN  | RXDIS  | RXPWD  | FIFORS |        | SRST   | LEMDE  | MXCRES |
|         | **bit 23** | **bit 22** | **bit 21** | **bit 20** | **bit 19** | **bit 18** | **bit 17** | **bit 16** |
| 0x005   | BCGEN  | DCMST  |        |        |        |        |        | SRALT  |

| Bit | Function |
| --- | -------- |
| EVGEN | Event Generator Master enable |
| RXDIS | Disable event reception |
| RXPWD | Receiver Power down |
| FIFORS|  Reset RX Event Fifo |
| SRST  | Soft reset IP |
| LEMDE | Little endian mode (cPCI-EVG-300) |
|       | 0 – PCI core in big endian mode (power up default) |
|       | 1 – PCI core in little endian mode |
|MXCRES | Write 1 to reset multiplexed counters |
|BCGEN  | Delay Compensation Beacon generator enable |
|       | 0 – Beacon generator disabled |
|       | 1 – Beacon generator enabled, sends out 0x7E events and delay compensation |
|       | data. Set only for master EVG in system |
| DCMST | System Master enable |
|       | 0 – System Master disabled |
|       | 1 – System Master enabled – has to be set and only for master EVG in system |
| SRALT | (reserved) | 

#### Interrupt Flag Register

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
|  0x008  |
|         | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
|  0x009  |        |        | IFSOV1 | IFSOV0 |        |        | IFSHF1 | IFSHF0 |
|         | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x00A   |        |        | IFSSTO1 | IFSSTO0 |             || IFSSTA1 | IFSSTA0 |
|         | bit 7  | bit 6  | bit 5  |bit 4   | bit 3  | bit 2  | bit 1  | bit 0 |
| 0x00B   |        | IFEXT  | IFDBUF |        |                || IFFF   | IFVIO |




| Bit | Function |
| --- | -------- |
| IFSOV1  | Sequence RAM 1 sequence roll over interrupt flag |
| IFSOV0  | Sequence RAM 0 sequence roll over interrupt flag |
| IFSHF1  | Sequence RAM 1 sequence halfway through interrupt flag |
| IFSHF0  | Sequence RAM 0 sequence halfway through interrupt flag |
| IFSSTO1 | Sequence RAM 1 sequence stop interrupt flag |
| IFSSTO0 | Sequence RAM 0 sequence stop interrupt flag |
| IFSSTA1 | Sequence RAM 1 sequence start interrupt flag |
| IFSSTA0 | Sequence RAM 0 sequence start interrupt flag |
| IFEXT   | External Interrupt flag |
| IFDBUF  | Data buffer flag |
| IFFF    | RX Event FIFO full flag |
| IFVIO   | Port U Receiver violation flag |

#### Interrupt Enable Register

| address | bit 31 | bit 30 | bit 29  | bit 28 | bit 27 | bit 26 | bit 25  | bit 24  |
| ------- | ------ | ------ | ------  | ------ | ------ | ------ | ------  | ------  |
| 0x00C   | IRQEN  |        |   
|         | bit 23 | bit 22 | bit 21  | bit 20 | bit 19 | bit 18 | bit 17  | bit 16  |
| 0x00D   |        |        | IESOV1  | IESOV0 |        |        | IESHF1  | IESHF0  |
|         | bit 15 | bit 14 | bit 13  | bit 12 | bit 11 | bit 10 | bit 9   | bit 8   |
| 0x00E   |        |        | IESSTO1 | IESSTO0 |       |        | IESSTA1 | IESSTA0 |
|         | bit 7  | bit 6  | bit 5   | bit 4   | bit 3 | bit 2  | bit 1   | bit 0   |
| 0x00F   |        | IEEXT  | IEDBUF  |         |       |        | IEFF    | IEVIO   |

| Bit     | Function |
| ---     | -------- |
| IRQEN   | Master interrupt enable
| PCIIE   | PCI core interrupt enable (cPCI-EVG-300)
|         |This bit is used by the low level driver to disable further interrupts before the
|         | first interrupt has been handled in user space
| IESOV1  | Sequence RAM 1 sequence roll over interrupt enable
| IESOV0  | Sequence RAM 0 sequence roll over interrupt enable
| IESHF1  | Sequence RAM 1 sequence halfway through interrupt enable
| IESHF0  | Sequence RAM 0 sequence halfway through interrupt enable
| IESSTO1 | Sequence RAM 1 sequence stop interrupt enable
| IESSTO0 | Sequence RAM 0 sequence stop interrupt enable
| IESSTA1 | Sequence RAM 1 sequence start interrupt enable
| IESSTA0 | Sequence RAM 0 sequence start interrupt enable
| IEEXT | External interrupt enable
| IEDBUF | Data buffer interrupt enable
| IEFF | Event FIFO full interrupt enable
| IEVIO | Receiver violation interrupt enable

#### AC Trigger Control Register

| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x011   |        |        |        |        | ACSYN2 | ACSYN1 | ACBYP  | ACSYN0 |
|         | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x012   | ACDIV7 | ACDIV6 | ACDIV5 | ACDIV4 | ACDIV3 | ACDIV2 | ACDIV1 | ACDIV0 |
|         | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| 0x013   | ACPS7  | ACPS6  | ACPS5  | ACPS4  | ACPS3  | ACPS2  | ACPS1  | ACPS0  |

| Bit        | Function |
| ---        | -------- |
| ACBYP      | AC divider and phase shifter bypass (0 = divider/phase shifter enabled, 1 =
|            | divider/phase shifter bypassed)
| ACSYN(2:0) | Synchronization select
|            | 000 = Event clock
|            | 001 = Multiplexed counter 7 output
|            | 011 = Front panel TTL input IN1
|            | 101 = Front panel TTL input IN2
| ACDIV(7:0) | AC Trigger divider (8-bit value)
| ACPS(7:0)  | AC Trigger Phase shift (8-bit value)

#### AC Trigger Mapping Register

| address | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x017   | ACM7   | ACM6   | ACM5   | ACM4   | ACM3   | ACM2   | ACM1   | ACM0   |

| Bit | Function |
| --- | -------- |
| ACM7 | If set AC circuit triggers Event Trigger 7 |
| ACM6 | If set AC circuit triggers Event Trigger 6 |
| ACM5 | If set AC circuit triggers Event Trigger 5 |
| ACM4 | If set AC circuit triggers Event Trigger 4 |
| ACM3 | If set AC circuit triggers Event Trigger 3 |
| ACM2 | If set AC circuit triggers Event Trigger 2 |
| ACM1 | If set AC circuit triggers Event Trigger 1 |
| ACM0 | If set AC circuit triggers Event Trigger 0 |

#### Software Event Register

| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x01A   |        |        |        |        |        |        | SWPEND | SWENA |
|         | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0 |
| 0x01B   | CODE7  | CODE6  | CODE5  | CODE4  | CODE3  | CODE2  | CODE1  | CODE0 |

| Bit       | Function |
| ---       | -------- |
| SWPEND    | Event code waiting to be sent out (read-only). A new event code may be written
|           | to the event code register when this bit reads ‘0’.
| SWENA     | Enable software event
|           | When enabled ‘1’ a new event will be sent out when event code is written to
|           | the event code register.
| CODE(7:0) | Event Code (8-bit value)

#### PCI Master Interrupt Enable Register

| address | bit 31 | bit 30 | bit 29  | bit 28 | bit 27 | bit 26 | bit 25  | bit 24  |
| ------- | ------ | ------ | ------  | ------ | ------ | ------ | ------  | ------  |
| 0x01C   |        | PCIIE  |   

| Bit   | Function |
| ---   | -------- |
| PCIIE | PCI core interrupt enable (mTCA-EVM-300) |
|       | This bit is used by the low level driver to disable further interrupts | 
|       | before the first interrupt has been handled in user space. |

#### Data Buffer Control Register

| address | bit 31  | bit 30  | bit 29  | bit 28  | bit 27 | bit 26   | bit 25  | bit 24  |
| ------- | ------  | ------  | ------  | ------  | ------ | ------   | ------  | ------  |
| 0x020   |        
|         | bit 23  | bit 22  | bit 21  | bit 20  | bit 19 | bit 18   | bit 17  | bit 16  |
| 0x021   |         |         |         | TXCPT   | TXRUN  | TRIG     | ENA     | 1       |
|         | bit 15  | bit 14  | bit 13  | bit 12  | bit 11 | bit 10   | bit 9   | bit 8   |
| 0x022   |         |         |         |         |        | DTSZ(10) | DTSZ(9) | DTSZ(8) |
|         | bit 7   | bit 6   | bit 5   | bit 4   | bit 3  | bit 2    | bit 1   | bit 0   |
| 0x023   | DTSZ(7) | DTSZ(6) | DTSZ(5) | DTSZ(4) | DTSZ(3) | DTSZ(2) | 0       | 0       |
  
| Bit   | Function |
| ---   | -------- |
| TXCPT | Data Buffer Transmission Complete
| TXRUN | Data Buffer Transmission Running – set when data transmission has been
|       | triggered and has not been completed yet
| TRIG  | Data Buffer Trigger Transmission
|       | Write ‘1’ to start transmission of data in buffer
| ENA   | Data Buffer Transmission enable
|       | ‘0’ – data transmission engine disabled
|       | ‘1’ – data transmission engine enabled
| DTSZ  | Data Transfer size 4 bytes to 2k in four byte increments


#### Distributed Bus Mapping Register

| address | bit 31    | bit 30    | bit 29    | bit 28    | bit 27    | bit 26    | bit 25    | bit 24    |
| ------- | ------    | ------    | ------    | ------    | ------    | ------    | ------    | ------    |
| 0x024   | DBMAP7(3) | DBMAP7(2) | DBMAP7(1) | DBMAP7(0) | DBMAP6(3) | DBMAP6(2) | DBMAP6(1) | DBMAP6(0) |
|         | bit 23    | bit 22    | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x025   | DBMAP5(3) | DBMAP5(2) | DBMAP5(1) | DBMAP5(0) | DBMAP4(3) | DBMAP4(2) | DBMAP4(1) | DBMAP4(0) |
|         | bit 15    | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x026   | DBMAP3(3) | DBMAP3(2) | DBMAP3(1) | DBMAP3(0) | DBMAP2(3) | DBMAP2(2) | DBMAP2(1) | DBMAP2(0) |
|         | bit 7     | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x027   | DBMAP1(3) | DBMAP1(2) | DBMAP1(1) | DBMAP1(0) | DBMAP0(3) | DBMAP0(2) | DBMAP0(1) | DBMAP0(0) |

| Bit         | Function |
| ---         | -------- |
| DBMAP7(3:0) | Distributed Bus Bit 7 Mapping:
|             | 0 – Off, output logic ‘0’
|             | 1 – take bus bit from external input
|             | 2 – Multiplexed counter output mapped to distributed bus bit
|             | 3 – Distributed bus bit forwarded from upstream EVG
| DBMAP6(3:0) | Distributed Bus Bit 7 Mapping (see above for mappings)
| DBMAP5(3:0) | Distributed Bus Bit 7 Mapping (see above for mappings)
| DBMAP4(3:0) | Distributed Bus Bit 7 Mapping (see above for mappings)
| DBMAP3(3:0) | Distributed Bus Bit 7 Mapping (see above for mappings)
| DBMAP2(3:0) | Distributed Bus Bit 7 Mapping (see above for mappings)
| DBMAP1(3:0) | Distributed Bus Bit 7 Mapping (see above for mappings)
| DBMAP0(3:0) | Distributed Bus Bit 7 Mapping (see above for mappings)

#### Distributed Bus Event Enable Register

| address | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x02B   | DBEV7  | DBEV6  | DBEV5 |

| Bit   | Function |
| ---   | -------- |
| DBEV5 | Distributed bus input 5 “Timestamp reset” 0x7D event enable
| DBEV6 | Distributed bus input 6 “Seconds ‘0’” 0x70 event enable
| DBEV7 | Distributed bus input 7 “Seconds ‘1’” 0x71 event enable

#### FPGA Firmware Version Register

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x02C   | 0      |     0  |      1 |      0 |  FF3   |  FF2   |  FF1   |  FF0   |
|         | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x02D   | Subrelease ID |
|         | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x02E   | Firmware ID |
|         | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x02F   | Revision ID |


| Bit                | Function | 
| ---                | -------- |
| Form Factor FF(0:3)| |
|                    | 0 – CompactPCI 3U |
|                    | 1 – PMC |
|                    | 2 – VME64x |
|                    | 3 – CompactRIO |
|                    | 4 – CompactPCI 6U |
|                    | 6 – PXIe |
|                    | 7 – PCIe |
|                    | 8 – mTCA.4 |


| Bit | Function |
| --- | -------- |
| Subrelease ID | For production releases the subrelease ID counts up from 00.
|               | For pre-releases this ID is used “backwards” counting down from ff i.e. when
|               | approacing release 22000207, we have prereleases 22FF0206, 22FE0206,
|               | 22FD0206 etc. in this order.
| Firmware ID   | 00 – Modular Register Map firmware (no delay compensation)
|               | 01 – Reserved
|               | 02 – Delay Compensation firmware
| Revision ID   | See end of manual

#### Segmented Data Buffer Control Register

| address | bit 31   | bit 30   | bit 29   | bit 28   | bit 27   | bit 26   | bit 25   | bit 24   |
| ------- | ------   | ------   | ------   | ------   | ------   | ------   | ------   | ------   |
| 0x030   | SADDR(7) | SADDR(6) | SADDR(5) | SADDR(4) | SADDR(3) | SADDR(2) | SADDR(1) | SADDR(0) |
|         | bit 23   | bit 22   | bit 21   | bit 20   | bit 19   | bit 18   | bit 17   | bit 16   |
| 0x031   |          |          |          | TXCPT    | TXRUN    | TRIG     |  ENA     |     1    |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11   | bit 10   | bit 9    | bit 8    |
| 0x032   |          |          |          |          |          | DTSZ(10) | DTSZ(9)  | DTSZ(8)  |
|         | bit 7    | bit 6    | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x033   | DTSZ(7)  | DTSZ(6)  |DTSZ(5)   | DTSZ(4)  | DTSZ(3)  | DTSZ(2)  | 0        | 0        |

| Bit        | Function |
| ---        | -------- |
| SADDR      | Transfer Start Segment Address (16 byte segments)
| TXCPT      | Data Buffer Transmission Complete
| TXRUN      | Data Buffer Transmission Running – set when data transmission has been
|            | triggered and has not been completed yet
| TRIG       | Data Buffer Trigger Transmission
|            | Write ‘1’ to start transmission of data in buffer
| ENA        | Data Buffer Transmission enable
|            | ‘0’ – data transmission engine disabled
|            | ‘1’ – data transmission engine enabled
| DTSZ       | Data Transfer size 4 bytes to 2k in four byte increments


#### Timestamp Generator Control Register

| address | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1   | bit 0   |
| ------- | ----- | ----- | ----- | ----- | ----- | ----- | -----   | -----   |
| 0x037   |       |       |       |       |       |       | TSGLOAD | TSGENA  |

| Bit     | Function |
| ---     | -------- |
| TSGENA  | Timestamp Generator Enable (‘0’ = disable, ‘1’ = enable)
| TSGLOAD | Timestamp Generator Load new value into Timestamp Counter
|         | Write ‘1’ to load new value

#### Microsecond Divider Register 

| address | bit 15 .. bit 0 | 
| ------- | --------------- |
| 0x04E   | Rounded integer value of 1μs * event clock |

This register shall be written with an integer value of the event clock rate in MHz. For 100 MHz event clock
this register should read 100, for 50 MHz event clock this register should read 50. This value is used to set
the parameters for the clock cleaner PLL and e.g. for the phase shifter in the AC input logic.

#### Clock Control Register

| address | bit 31  | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------  | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x050   | PLLLOCK | BWSEL2 | BWSEL1 | BWSEL0 |        | RFSEL2 | RFSEL1 | RFSEL0 |
|         | bit 23  | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x051   | PHTOGG  |        | RFDIV5 | RFDIV4 | RFDIV3 | RFDIV2 | RFDIV1 | RFDIV0 |
|         | bit 15  | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x052   |         |        |        |        |        |        | CGLOCK |        |

| Bit | Function |
| --- | -------- |
| PLLLOCK | Clock cleaner locked
| BWSEL2:0 | PLL Bandwidth Select (see Silicon Labs Si5317 datasheet)
|          | 000 – Si5317, BW setting HM (lowest loop bandwidth)
|          | 001 – Si5317, BW setting HL
|          | 010 – Si5317, BW setting MH
|          | 011 – Si5317, BW setting MM
|          | 100 – Si5317, BW setting ML (highest loop bandwidth)
| PHTOGG   | Distributed bus phase toggle
| RFDIV5-0 | External RF divider select:
|          | 000000 – RF/1
|          | 000001 – RF/2
|          | 000010 – RF/3
|          | 000011 – RF/4
|          | 000100 – RF/5
|          | 000101 – RF/6
|          | 000110 – RF/7
|          | 000111 – RF/8
|          | 001000 – RF/9
|          | 001001 – RF/10
|          | 001010 – RF/11
|          | 001011 – RF/12
|          | 001100 – OFF
|          | 001101 – RF/14
|          | 001110 – RF/15
|          | 001111 – RF/16
|          | 010000 – RF/17
|          | 010001 – RF/18
|          | 010010 – RF/19
|          | 010011 – RF/20
|          | 010100 – RF/21
|          | 010101 – RF/22
|          | 010110 – RF/23
|          | 010111 – RF/24
|          | 011000 – RF/25
|          | 011001 – RF/26
|          | 011010 – RF/27
|          | 011011 – RF/28
|          | 011100 – RF/29
|          | 011101 – RF/30
|          | 011110 – RF/31
|          | 011111 – RF/32
| RFSEL2-0 | RF reference select:
|          | 000 – Use internal reference (fractional synthesizer)
|          | 001 – Use external RF reference (front panel input through divider)
|          | 010 – PXIe 100 MHz clock
|          | 100 – Use recovered RX clock, Fan-Out mode
|          | 101 – Use external RF reference for downstream ports, internal reference for
|          | upstream port, Fan-Out mode, event rate down conversion
|          | 110 – PXIe 10 MHz clock through clock multiplier
|          | 111 – Recovered clock /2 decimate mode, event rate is halved
| CGLOCK   | Micrel SY87739L reference clock locked (read-only)

```{note}
Please note that after changing the Event clock source the fractional synthesizer control word 
must be reloaded to initialize an internal reset.
```

#### Event Analyser Control Register

| address | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| ------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| 0x063   |       |       |       | EVANE | EVARS | EVAOF | EVAEN | EVACR |

| Bit | Function |
| --- | -------- |
|EVANE | Event Analyser FIFO not empty flag:
|      | 0 – FIFO empty
|      | 1 – FIFO not empty, events in FIFO
|EVARS | Event Analyser Reset
|      | 0 – not in reset
|      | 1 – reset
|EVAOF | Event Analyser FIFO overflow flag:
|      | 0 – no overflow
|      | 1 – FIFO overflow
|EVAEN | Event Analyser enable
|      | 0 – Event Analyser disabled
|      | 1 – Event Analyser enabled
|EVACR | Event Analyser 64 bit counter reset
|      | 0 – Counter running
|      | 1 – Counter reset to zero.

#### Sequence RAM Control Registers

| address | bit 31    | bit 30    | bit 29    | bit 28    | bit 27   | bit 26   | bit 25   | bit 24   |
| ------- | ------    | ------    | ------    | ------    | ------   | ------   | ------   | ------   |
| 0x070   |           |           |           |           |          |          | SQ0RUN   | SQ0ENA   |
|         | bit 23    | bit 22    | bit 21    | bit 20    | bit 19   | bit 18   | bit 17   | bit 16   |
| 0x071   | SQ0XTR    | SQ0XEN    | SQ0SWT    | SQ0SNG    | SQ0REC   | SQ0RES   | SQ0DIS   | SQ0EN    |
|         | bit 15    | bit 14    | bit 13    | bit 12    | bit 11   | bit 10   | bit 9    | bit 8    |
| 0x072   | SQSWMASK3 | SQSWMASK2 | SQSWMASK1 | SQSWMASK0 | SQSWENA3 | SQSWENA2 | SQSWENA1 | SQSWENA0 |
|         | bit 7     | bit 6     | bit 5     | bit 4     | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x073   | SQ0TSEL7 | SQ0TSEL6 | SQ0TSEL5 | SQ0TSEL4 | SQ0TSEL3 | SQ0TSEL2 | SQ0TSEL1 | SQ0TSEL0     |

| address | bit 31    | bit 30    | bit 29    | bit 28    | bit 27   | bit 26   | bit 25   | bit 24   |
| ------- | ------    | ------    | ------    | ------    | ------   | ------   | ------   | ------   |
| 0x074   |           |           |           |           |          |          | SQ1RUN   | SQ1ENA   |
|         | bit 23    | bit 22    | bit 21    | bit 20    | bit 19   | bit 18   | bit 17   | bit 16   |
| 0x075   | SQ1XTR    | SQ1XEN    | SQ1SWT    | SQ1SNG    | SQ1REC   | SQ1RES   | SQ1DIS   | SQ1EN    |
|         | bit 15    | bit 14    | bit 13    | bit 12    | bit 11   | bit 10   | bit 9    | bit 8    |
| 0x076   | SQSWMASK3 | SQSWMASK2 | SQSWMASK1 | SQSWMASK0 | SQSWENA3 | SQSWENA2 | SQSWENA1 | SQSWENA0 |
|         | bit 7     | bit 6     | bit 5     | bit 4     | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x077   | SQ1TSEL7  | SQ1TSEL6  | SQ1TSEL5  | SQ1TSEL4  | SQ1TSEL3 | SQ1TSEL2 | SQ1TSEL1 | SQ1TSEL0 |

| Bit | Function |
| --- | -------- |
| SQxRUN   | Sequence RAM running flag (read-only)
| SQxENA   | Sequence RAM enabled flag (read_only)
| SQxSWT   | Sequence RAM software trigger, write ‘1’ to trigger
| SQxSNG   | Sequence RAM single mode
| SQxREC   | Sequence RAM recycle mode
| SQxRES   | Sequence RAM reset, write ‘1’ to reset
| SQxDIS   | Sequence RAM disable, write ‘1’ to disable
| SQxEN    | Sequence RAM enable, write ‘1’ to enable/arm
| SQxXEN   | Sequence RAM allow external enable, ‘1’ - allow
| SQxXTR   | Sequence RAM allow external trigger enable, ‘1’ - allow
| SQSWMASK | Sequence RAM SW mask register, the mask bits are common for all RAMS
| SQSWENA  | Sequence RAM SW enable register, the mask bits are common for all RAMS
| SQxTSEL  | Sequence RAM trigger select:
|          | 0 – trigger from MXC0
|          | 1 – trigger from MXC1
|          | 2 – trigger from MXC2
|          | 3 – trigger from MXC3
|          | 4 – trigger from MXC4
|          | 5 – trigger from MXC5
|          | 6 – trigger from MXC6
|          | 7 – trigger from MXC7
|          | 16 – trigger from AC synchronization logic
|          | 17 – trigger from sequence RAM 0 software trigger
|          | 18 – trigger from sequence RAM 1 software trigger
|          | 19 – trigger always immediately when enabled
|          | 24 – trigger from sequence RAM 0 external trigger
|          | 25 – trigger from sequence RAM 1 external trigger
|          | 31 – trigger disabled (default after power up)


#### SY87739L Fractional Divider Configuration Word

|Configuration Word | Frequency with 24 MHz reference oscillator |
| ----------------- | ------------------------------------------ |
| 0x0891C100        | 142.857 MHz
| 0x00DE816D        | 125 MHz
| 0x00FE816D        | 124.95 MHz
| 0x0C928166        | 124.9087 MHz
| 0x018741AD        | 119 MHz
| 0x072F01AD        | 114.24 MHz
| 0x049E81AD        | 106.25 MHz
| 0x008201AD        | 100 MHz
| 0x025B41ED        | 99.956 MHz
| 0x0187422D        | 89.25 MHz
| 0x0082822D        | 81 MHz
| 0x0106822D        | 80 MHz
| 0x019E822D        | 78.900 MHz
| 0x018742AD        | 71.4 MHz
| 0x0C9282A6        | 62.454 MHz
| 0x009743AD        | 50 MHz
| 0x0C25B43AD       |  49.978 MHz
| 0x0176C36D        | 49.965 MHz

#### SPI Configuration Flash Registers

| address | bit 7    | bit 6    | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    |
| ------- | ------   | ------   | ------   | ------   | ------   | ------   | ------   | ------   |
| 0x0A3   | SPIDATA7 | SPIDATA6 | SPIDATA5 | SPIDATA4 | SPIDATA3 | SPIDATA2 | SPIDATA1 | SPIDATA0 |
|         | bit 7    | bit 6    | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x0A7   | E        | RRDY     | TRDY     | TMT      | TOE      | ROE      | OE       | SSO      |
   
| Bit          | Function |
| ---          | -------- |
| SPIDATA(7:0) | Read SPI data byte / Write SPI data byte |
| E            | Overrun Error flag |
| RRDY         | Receiver ready, if ‘1’ data byte waiting in SPI_DATA |
| TRDY         | Transmitter ready, if ‘1’ SPI_DATA is ready to accept new transmit data byte |
| TMT          | Transmitter empty, if ‘1’ data byte has been transmitted |
| TOE          | Transmitter overrun error |
| ROE          | Receiver overrun error |
| OE           | Output enable for SPI pins, ‘1’ enable SPI pins |
| SSO          | Slave select output enable for SPI slave device, ‘1’ device selected |

#### Event Trigger Registers

| address | bit 15   | bit 14   | bit 13   | bit 12   | bit 11   | bit 10   | bit 9    | bit 8    |
| ------- | ------   | ------   | ------   | ------   | ------   | ------   | ------   | ------   |
| 0x102   |          |          |          |          |          |          |          | EVEN0    |
|         | bit 7    | bit 6    | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x103   | EVCD0(7) | EVCD0(6) | EVCD0(5) | EVCD0(4) | EVCD0(3) | EVCD0(2) | EVCD0(1) | EVCD0(0) |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11   | bit 10   | bit 9    | bit 8    |
| 0x106   |          |          |          |          |          |          |          | EVEN1    |
|         | bit 7    | bit 6    | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x107   | EVCD1(7) | EVCD1(6) | EVCD1(5) | EVCD1(4) | EVCD1(3) | EVCD1(2) | EVCD1(1) | EVCD1(0) |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11   | bit 10   | bit 9    | bit 8    |
| 0x10A   |          |          |          |          |          |          |          | EVEN2    |
|         | bit 7    |  bit 6   | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x10B   | EVCD2(7) | EVCD2(6) | EVCD2(5) | EVCD2(4) | EVCD2(3) | EVCD2(2) | EVCD2(1) | EVCD2(0) |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11   | bit 10   | bit 9    | bit 8    |
| 0x10E   |          |          |          |          |          |          |          | EVEN3    | 
|         | bit 7    |  bit 6   | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    | 
| 0x10F   | EVCD3(7) | EVCD3(6) | EVCD3(5) | EVCD3(4) | EVCD3(3) | EVCD3(2) | EVCD3(1) | EVCD3(0) |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11   | bit 10   | bit 9    | bit 8    |
| 0x112   |          |          |          |          |          |          |          | EVEN4    |
|         | bit 7    |  bit 6   | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x113   | EVCD4(7) | EVCD4(6) | EVCD4(5) | EVCD4(4) | EVCD4(3) | EVCD4(2) | EVCD4(1) | EVCD4(0) |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11   | bit 10   | bit 9    | bit 8    |
| 0x116   |          |          |          |          |          |          |          | EVEN5    |
|         | bit 7    |  bit 6   | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x117   | EVCD5(7) | EVCD5(6) | EVCD5(5) | EVCD5(4) | EVCD5(3) | EVCD5(2) | EVCD5(1) | EVCD5(0) |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11   | bit 10   | bit 9    | bit 8    |
| 0x11A   |          |          |          |          |          |          |          | EVEN6    |
|         | bit 7    | bit 6    | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x11B   | EVCD6(7) | EVCD6(6) | EVCD6(5) | EVCD6(4) | EVCD6(3) | EVCD6(2) | EVCD6(1) | EVCD6(0) |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11   | bit 10   | bit 9    | bit 8    |
| 0x11E   |          |          |          |          |          |          |          | EVEN7    |
|         | bit 7    |  bit 6   | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0    |
| 0x11F   | EVCD7(7) | EVCD7(6) | EVCD7(5) | EVCD7(4) | EVCD7(3) | EVCD7(2) | EVCD7(1) | EVCD7(0) |


| Bit   | Function |
| ---   | -------- |
| EVENx | Enable Event Trigger x |
| EVCDx | Event Trigger Code for Event trigger x | 

#### Multiplexed Counter Registers

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x180   | MXC0   | MXCP0  | 
|         | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| 0x183   | MX0EV7 | MX0EV6 | MX0EV5 | MX0EV4 | MX0EV3 | MX0EV2 | MX0EV1 | MX0EV0 |
|         | bit 31 | bit 0 |
| 0x184   | Multiplexed Counter 0  Prescaler |
|         | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| 0x188   | MXC1   | MXCP1 |
|         | bit 7  | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x18B   | MX1EV7 | MX1EV6 | MX1EV5 | MX1EV4 | MX1EV3 | MX1EV2 | MX1EV1 | MX1EV0 |
|         | bit 31 | bit 0 |
| 0x18C   | Multiplexed Counter 1 Prescaler |
|         | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| 0x190   | MXC2 | MXCP2 |
|         | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x193   | MX2EV7 | MX2EV6 | MX2EV5 | MX2EV4 | MX2EV3 | MX2EV2 | MX2EV1 | MX2EV0 |
|         | bit 31 | bit 0 |
| 0x194   | Multiplexed Counter 2 Prescaler |
|         | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| 0x198   | MXC3 | MXCP3 |
|         | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x19B   | MX3EV7 | MX3EV6 | MX3EV5 | MX3EV4 | MX3EV3 | MX3EV2 | MX3EV1 | MX3EV0 |
|         | bit 31 | bit 0 |
| 0x19C   | Multiplexed Counter 3 Prescaler |
|         | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| 0x1A0   | MXC4 | MXCP4 |
|         | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x1A3   | MX4EV7 | MX4EV6 | MX4EV5 | MX4EV4 | MX4EV3 | MX4EV2 | MX4EV1 | MX4EV0 |
|         | bit 31 | bit 0 |
| 0x1A4   | Multiplexed Counter 4 Prescaler |
|         | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| 0x1A8   | MXC5 | MXCP5 |
|         | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x1AB   | MX5EV7 | MX5EV6 | MX5EV5 | MX5EV4 | MX5EV3 | MX5EV2 | MX5EV1 | MX5EV0 |
|         | bit 31 | bit 0 |
| 0x1AC   | Multiplexed Counter 5 Prescaler |
|         | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| 0x1B0   | MXC6 | MXCP6 |
|         | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x1B3   | MX6EV7 | MX6EV6 | MX6EV5 | MX6EV4 | MX6EV3 | MX6EV2 | MX6EV1 | MX6EV0 |
|         | bit 31 | bit 0 |
| 0x1B4   | Multiplexed Counter 6 Prescaler |
|         | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| 0x1B8   | MXC7 | MXCP7 |
|         | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x1BB   | MX7EV7 | MX7EV6 | MX7EV5 | MX7EV4 | MX7EV3 | MX7EV2 | MX7EV1 | MX7EV0 |
|         | bit 31 | bit 0 |
| 0x1BC   | Multiplexed Counter 7 Prescaler |

| Bit | Function |
| --- | -------- |
|MXCx   | Multiplexed counter output status (read-only)
|MXPx   | Multiplexed counter output polarity
|MXxEV7 | Map rising edge of multiplexed counter x to send out event trigger 7
|MXxEV6 | Map rising edge of multiplexed counter x to send out event trigger 6
|MXxEV5 | Map rising edge of multiplexed counter x to send out event trigger 5
|MXxEV4 | Map rising edge of multiplexed counter x to send out event trigger 4
|MXxEV3 | Map rising edge of multiplexed counter x to send out event trigger 3
|MXxEV2 | Map rising edge of multiplexed counter x to send out event trigger 2
|MXxEV1 | Map rising edge of multiplexed counter x to send out event trigger 1
|MXxEV0 | Map rising edge of multiplexed counter x to send out event trigger 0

#### Transition Board Output Mapping Registers

| address | bit 15 to bit 0 |
| --------| --------------- |
| 0x480   | Transition Board Output 0 Mapping ID (see [the table for mapping IDs](event-generator.md#mapping-id-table))
| 0x482   | Transition Board Output 1 Mapping ID
| ...     |
| 0x41E   | Transition Board Output 15 Mapping ID

#### Front Panel Input Mapping Registers

| address | bit 31   | bit 30   | bit 29   | bit 28   | bit 27    | bit 26    | bit 25    | bit 24           |
| ------- | ------   | ------   | ------   | ------   | ------    | ------    | ------    | ------           |
| 0x500   | FP0SQMK3 | FP0SQMK2 | FP0SQMK1 | FP0SQMK0 | FP0SQEEN3 | FP0SQEEN2 | FP0SQEEN1 | FP0SQEEN0/FP0IRQ |
|         | bit 23   | bit 22   | bit 21   | bit 20   | bit 19    | bit 18    | bit 17    | bit 16           |
| 0x501   | FP0DB7   | FP0DB6   | FP0DB5   | FP0DB4   | FP0DB3    | FP0DB2    | FP0DB1    | FP0DB0           |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11    | bit 10    | bit 9     | bit 8            |
| 0x502   |          |          | FP0SEN1  | FP0SEN0  |           |           | FP0SEQ1   | FP0SEQ0          |
|         | bit 7    | bit 6    | bit 5    | bit 4    | bit 3     | bit 2     | bit 1     | bit 0            |
| 0x503   | FP0EV7   | FP0EV6   | FP0EV5   | FP0EV4   | FP0EV3    | FP0EV2    | FP0EV1    | FP0EV0           |
|         | bit 31   | bit 30   | bit 29   | bit 28   | bit 27    | bit 26    | bit 25    | bit 24           |
| 0x504   | FP1SQMK3 | FP1SQMK2 | FP1SQMK1 | FP1SQMK0 | FP1SQEEN3 | FP1SQEEN2 | FP1SQEEN1 | FP1SQEEN0/FP1IRQ |
|         | bit 23   | bit 22   | bit 21   | bit 20   | bit 19    | bit 18    | bit 17    | bit 16           |
| 0x505   | FP1DB7   | FP1DB6   | FP1DB5   | FP1DB4   | FP1DB3    | FP1DB2    | FP1DB1    | FP1DB0           |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11    | bit 10    | bit 9     | bit 8            |
| 0x506   |          |          | FP1SEN1  | FP1SEN0  |           |           |  FP1SEQ1  | FP1SEQ0          |
|         | bit 7    | bit 6    | bit 5    | bit 4    | bit 3     | bit 2     | bit 1     | bit 0            |
| 0x507   | FP1EV7   | FP1EV6   | FP1EV5   | FP1EV4   | FP1EV3    | FP1EV2    | FP1EV1    | FP1EV0           |
|         | bit 31   | bit 30   | bit 29   | bit 28   | bit 27    | bit 26    | bit 25    | bit 24           |
| 0x508   | FP2SQMK3 | FP2SQMK2 | FP2SQMK1 | FP2SQMK0 | FP2SQEEN3 | FP2SQEEN2 | FP2SQEEN1 | FP2SQEEN0/FP2IRQ |
|         | bit 23   | bit 22   | bit 21   | bit 20   | bit 19    | bit 18    | bit 17    | bit 16           |
| 0x509   | FP2DB7   | FP2DB6   | FP2DB5   | FP2DB4   | FP2DB3    | FP2DB2    | FP2DB1    | FP2DB0           |
|         | bit 15   | bit 14   | bit 13   | bit 12   | bit 11    | bit 10    | bit 9     | bit 8            |
| 0x50A   |          |          | FP2SEN1  | FP2SEN0  |           |           | FP2SEQ1   | FP2SEQ0          |
|         | bit 7    | bit 6    | bit 5    | bit 4    | bit 3     | bit 2     | bit 1     | bit 0            |
| 0x50B   | FP2EV7   | FP2EV6   | FP2EV5   | FP2EV4   | FP2EV3    | FP2EV2    | FP2EV1    | FP2EV0           |

| Bit       | Function |
| --------- | -------- |
| FPxSQMKy  | Map Front panel Input x to Sequence Event Mask bit y
| FPxSQEENy | Map Front panel Input x to Sequence Event Enable bit y
| FPxIRQ    | Map Front panel Input x to External Interrupt
| FPxDB7    | Map Front panel Input x to Distributed Bus bit 7
| FPxDB6    | Map Front panel Input x to Distributed Bus bit 6
| FPxDB5    | Map Front panel Input x to Distributed Bus bit 5
| FPxDB4    | Map Front panel Input x to Distributed Bus bit 4
| FPxDB3    | Map Front panel Input x to Distributed Bus bit 3
| FPxDB2    | Map Front panel Input x to Distributed Bus bit 2
| FPxDB1    | Map Front panel Input x to Distributed Bus bit 1
| FPxDB0    | Map Front panel Input x to Distributed Bus bit 0
| FPxSEN1   | Map Front panel Input x to Sequence External Enable 1
| FPxSEN0   | Map Front panel Input x to Sequence External Enable 0
| FPxSEQ1   | Map Front panel Input x to Sequence Trigger 1
| FPxSEQ0   | Map Front panel Input x to Sequence Trigger 0
| FPxEV7    | Map Front panel Input x to Event Trigger 7
| FPxEV6    | Map Front panel Input x to Event Trigger 6
| FPxEV5    | Map Front panel Input x to Event Trigger 5
| FPxEV4    | Map Front panel Input x to Event Trigger 4
| FPxEV3    | Map Front panel Input x to Event Trigger 3
| FPxEV2    | Map Front panel Input x to Event Trigger 2
| FPxEV1    | Map Front panel Input x to Event Trigger 1
| FPxEV0    | Map Front panel Input x to Event Trigger 0

### Front Panel Input Phase Monitoring Registers

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27   | bit 26   | bit 25    | bit 24   |
| ------- | ------ | ------ | ------ | ------ | ------   | ------   | ------    | ------   |
| 0x520   | PHCLR0 | DBPH0  |        |        |          |          | PHSEL0(1) | PHSEL0(0)|
|         | bit 15 | bit 14 | bit 13 | bit 12 | bit 11   | bit 10   | bit 9     | bit 8    |
| 0x522   |        |        |        |        | PHFE0(3) | PHFE0(2) | PHFE0(1)  | PHFE0(0) |
|         | bit 7  | bit 6  | bit 5  | bit 4  | bit 3    | bit 2    | bit 1     | bit 0    |
| 0x523   |        |        |        |        | PHRE0(3) | PHRE0(2) | PHRE0(1)  | PHRE0(0) |

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27   | bit 26   | bit 25    | bit 24   |
| ------- | ------ | ------ | ------ | ------ | ------   | ------   | ------    | ------   |
| 0x524   | PHCLR1 | DBPH1  |        |        |          |          | PHSEL1(1) | PHSEL1(0)|
|         | bit 15 | bit 14 | bit 13 | bit 12 | bit 11   | bit 10   | bit 9     | bit 8    |
| 0x526   |        |        |        |        | PHFE1(3) | PHFE1(2) | PHFE1(1)  | PHFE1(0) |
|         | bit 7  | bit 6  | bit 5  | bit 4  | bit 3    | bit 2    | bit 1     | bit 0    |
| 0x527   |        |        |        |        | PHRE1(3) | PHRE1(2) | PHRE1(1)  | PHRE1(0) |

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27   | bit 26   | bit 25    | bit 24   |
| ------- | ------ | ------ | ------ | ------ | ------   | ------   | ------    | ------   |
| 0x528   | PHCLR2 | DBPH2  |        |        |          |          | PHSEL2(1) | PHSEL2(0)|
|         | bit 15 | bit 14 | bit 13 | bit 12 | bit 11   | bit 10   | bit 9     | bit 8    |
| 0x52A   |        |        |        |        | PHFE2(3) | PHFE2(2) | PHFE2(1)  | PHFE2(0) |
|         | bit 7  | bit 6  | bit 5  | bit 4  | bit 3    | bit 2    | bit 1     | bit 0    |
| 0x52B   |        |        |        |        | PHRE2(3) | PHRE2(2) | PHRE2(1)  | PHRE2(0) |

| Bit | Function |
| --- | -------- |
| PHCLRx | Reset phase monitoring registers by writing ‘1’
| DBPHx | Distributed bus phase sampled on rising edge of input signal
| PHSELx(1:0) | Input phase select
| | 00 - Sample input with 0° event clock
| | 01 - Sample input with 90° event clock
| | 10 - Sample input with 180° event clock
| | 11 - Sample input with 270° event clock
| PHFEx(3:0) | Falling edge phase monitoring register
| PHREx(3:0) | Rising edge phase monitoring register

#### Universal Input Mapping Registers

| address | bit 31    | bit 30    | bit 29    | bit 28    | bit 27      | bit 26      | bit 25      | bit 24 |
| ------- | ------    | ------    | ------    | ------    | ------      | ------      | ------      | ------ |
| 0x540   | UI0SQMK(3)| UI0SQMK(2)| UI0SQMK(1)| UI0SQMK(0)| UI0SQEEN(3) | UI0SQEEN(2) | UI0SQEEN(1) | UI0SQEEN(0) / UI0IRQ |
|         | bit 23    | bit 22    | bit 21    | bit 20    | bit 19      | bit 18      | bit 17      | bit 16 |
| 0x541   | UI0DB7    | UI0DB6    | UI0DB5    | UI0DB4    | UI0DB3      | UI0DB2      | UI0DB1      | UI0DB0 |
|         | bit 15    | bit 14    | bit 13    | bit 12    | bit 11      | bit 10      | bit 9       | bit 8  |
| 0x542   |           |           | UI0SEN1   | UI0SEN0   |             |             | UI0SEQ1     | UI0SEQ0 |
|         | bit 7     | bit 6     | bit 5     | bit 4     | bit 3       | bit 2       | bit 1       | bit 0 |
| 0x543   | UI0EV7    | UI0EV6    | UI0EV5    | UI0EV4    | UI0EV3      | UI0EV2      | UI0EV1      | UI0EV0 |
|         | bit 31    | bit 30    | bit 29    | bit 28    | bit 27      | bit 26      | bit 25      | bit 24 |
| 0x544   | UI1SQMK(3)| UI1SQMK(2)| UI1SQMK(1)| UI1SQMK(0)| UI1SQEEN(3) | UI1SQEEN(2) | UI1SQEEN(1) | UI1SQEEN(0) / UI1IRQ |
|         | bit 23    | bit 22    | bit 21    | bit 20    | bit 19      | bit 18      | bit 17      | bit 16 |
| 0x545   | UI1DB7    | UI1DB6    | UI1DB5    | UI1DB4    | UI1DB3      | UI1DB2      | UI1DB1      | UI1DB0 |
|         | bit 15    | bit 14    | bit 13    | bit 12    | bit 11      | bit 10      | bit 9       | bit 8  |
| 0x546   |           |           | UI1SEN1   | UI1SEN0   |             |             | TI1SEQ1     | TI1SEQ0 |
|         | bit 7     | bit 6     | bit 5     | bit 4     | bit 3       | bit 2       | bit 1       | bit 0 |
| 0x547   | UI1EV7    | UI1EV6    | UI1EV5    | UI1EV4    | UI1EV3      | UI1EV2      | UI1EV1      | UI1EV0 |
| ... |
|         | bit 31    | bit 30    | bit 29    | bit 28    | bit 27      | bit 26      | bit 25      | bit 24 |
| 0x55C   | UI5SQMK(3)| UI5SQMK(2)| UI5SQMK(1)| UI5SQMK(0)| UI5SQEEN(3) | UI5SQEEN(2) | UI5SQEEN(1) | UI5SQEEN(0) / UI5IRQ |
|         | bit 23    | bit 22    | bit 21    | bit 20    | bit 19      | bit 18      | bit 17      | bit 16 |
| 0x55D   | UI15DB7   | UI15DB6   | UI15DB5   | UI15DB4   | UI15DB3     | UI15DB2     | UI15DB1     | UI15DB0 |
|         | bit 15    | bit 14    | bit 13    | bit 12    | bit 11      | bit 10      | bit 9       | bit 8   |
| 0x55E   |           |           | UI15SEN1  | UI15SEN0  |             |             | UI15SEQ1    | UI15SEQ0 |
|         | bit 7     | bit 6     | bit 5     | bit 4     | bit 3       | bit 2       | bit1        | bit 0 |
| 0x55F   | UI15EV7   | UI15EV6   | UI15EV5   | UI15EV4   | UI15EV3     | UI15EV2     | UI15EV1     | UI15EV0 |

| Bit         | Function |
| ---         | -------- |
| UIxSQMKy    | Map Universal Input x to Sequence Event Mask bit y |
| UIxSQEENy   | Map Universal Input x to Sequence Event Enable bit y |
| UIxIRQ      | Map Universal Input x to External Interrupt |
| UIxDB7      | Map Universal Input x to Distributed Bus bit 7 |
| UIxDB6      | Map Universal Input x to Distributed Bus bit 6 |
| UIxDB5      | Map Universal Input x to Distributed Bus bit 5 |
| UIxDB4      | Map Universal Input x to Distributed Bus bit 4 |
| UIxDB3      | Map Universal Input x to Distributed Bus bit 3 |
| UIxDB2      | Map Universal Input x to Distributed Bus bit 2 |
| UIxDB1      | Map Universal Input x to Distributed Bus bit 1 |
| UIxDB0      | Map Universal Input x to Distributed Bus bit 0 |
| UIxSEN1     | Map Universal Input x to Sequence External Enable 1 |
| UIxSEN0     | Map Universal Input x to Sequence External Enable 0 |
| UIxSEQ1     | Map Universal Input x to Sequence Trigger 1 |
| UIxSEQ0     | Map Universal Input x to Sequence Trigger 0 |
| UIxEV7      | Map Universal Input x to Event Trigger 7 |
| UIxEV6      | Map Universal Input x to Event Trigger 6 |
| UIxEV5      | Map Universal Input x to Event Trigger 5 |
| UIxEV4      | Map Universal Input x to Event Trigger 4 |
| UIxEV3      | Map Universal Input x to Event Trigger 3 |
| UIxEV2      | Map Universal Input x to Event Trigger 2 |
| UIxEV1      | Map Universal Input x to Event Trigger 1 |
| UIxEV0      | Map Universal Input x to Event Trigger 0 |



#### Transition Board Input Mapping Registers

| address | bit 31    | bit 30    | bit 29    | bit 28    | bit 27      | bit 26      | bit 25      | bit 24 |
| ------- | ------    | ------    | ------    | ------    | ------      | ------      | ------      | ------ |
| 0x600   | TI0SQMK(3)| TI0SQMK(2)| TI0SQMK(1)| TI0SQMK(0)| TI0SQEEN(3) | TI0SQEEN(2) | TI0SQEEN(1) | TI0SQEEN(0) / TI0IRQ |
|         | bit 23    | bit 22    | bit 21    | bit 20    | bit 19      | bit 18      | bit 17      | bit 16 |
| 0x601   | TI0DB7    | TI0DB6    | TI0DB5    | TI0DB4    | TI0DB3      | TI0DB2      | TI0DB1      | TI0DB0 |
|         | bit 15    | bit 14    | bit 13    | bit 12    | bit 11      | bit 10      | bit 9       | bit 8  |
| 0x602   |           |           | TI0SEN1   | TI0SEN0   |             |             | TI0SEQ1     | TI0SEQ0 |
|         | bit 7     | bit 6     | bit 5     | bit 4     | bit 3       | bit 2       | bit 1       | bit 0 |
| 0x603   | TI0EV7    | TI0EV6    | TI0EV5    | TI0EV4    | TI0EV3      | TI0EV2      | TI0EV1      | TI0EV0 |
|         | bit 31    | bit 30    | bit 29    | bit 28    | bit 27      | bit 26      | bit 25      | bit 24 |
| 0x604   | TI1SQMK(3)| TI1SQMK(2)| TI1SQMK(1)| TI1SQMK(0)| TI1SQEEN(3) | TI1SQEEN(2) | TI1SQEEN(1) | TI1SQEEN(0) / TI1IRQ |
|         | bit 23    | bit 22    | bit 21    | bit 20    | bit 19      | bit 18      | bit 17      | bit 16 |
| 0x605   | TI1DB7    | TI1DB6    | TI1DB5    | TI1DB4    | TI1DB3      | TI1DB2      | TI1DB1      | TI1DB0 |
|         | bit 15    | bit 14    | bit 13    | bit 12    | bit 11      | bit 10      | bit 9       | bit 8  |
| 0x606   |           |           | TI1SEN1   | TI1SEN0   |             |             | TI1SEQ1     | TI1SEQ0 |
|         | bit 7     | bit 6     | bit 5     | bit 4     | bit 3       | bit 2       | bit 1       | bit 0 |
| 0x607   | TI1EV7    | TI1EV6    | TI1EV5    | TI1EV4    | TI1EV3      | TI1EV2      | TI1EV1      | TI1EV0 |
| ... |
|         | bit 31    | bit 30    | bit 29    | bit 28    | bit 27      | bit 26      | bit 25      | bit 24 |
| 0x61C   | TI5SQMK(3)| TI5SQMK(2)| TI5SQMK(1)| TI5SQMK(0)| TI5SQEEN(3) | TI5SQEEN(2) | TI5SQEEN(1) | TI5SQEEN(0) / TI5IRQ |
|         | bit 23    | bit 22    | bit 21    | bit 20    | bit 19      | bit 18      | bit 17      | bit 16 |
| 0x61D   | TI15DB7   | TI15DB6   | TI15DB5   | TI15DB4   | TI15DB3     | TI15DB2     | TI15DB1     | TI15DB0 |
|         | bit 15    | bit 14    | bit 13    | bit 12    | bit 11      | bit 10      | bit 9       | bit 8   |
| 0x61E   |           |           | TI15SEN1  | TI15SEN0  |             |             | TI15SEQ1    | TI15SEQ0 |
|         | bit 7     | bit 6     | bit 5     | bit 4     | bit 3       | bit 2       | bit1        | bit 0 |
| 0x61F   | TI15EV7   | TI15EV6   | TI15EV5   | TI15EV4   | TI15EV3     | TI15EV2     | TI15EV1     | TI15EV0 |

| Bit         | Function |
| ---         | -------- |
| TIxSQMKy    | Map Transition Board Input x to Sequence Event Mask bit y |
| TIxSQEENy   | Map Transition Board Input x to Sequence Event Enable bit y |
| TIxIRQ      | Map Transition Board Input x to External Interrupt |
| TIxDB7      | Map Transition Board Input x to Distributed Bus bit 7 |
| TIxDB6      | Map Transition Board Input x to Distributed Bus bit 6 |
| TIxDB5      | Map Transition Board Input x to Distributed Bus bit 5 |
| TIxDB4      | Map Transition Board Input x to Distributed Bus bit 4 |
| TIxDB3      | Map Transition Board Input x to Distributed Bus bit 3 |
| TIxDB2      | Map Transition Board Input x to Distributed Bus bit 2 |
| TIxDB1      | Map Transition Board Input x to Distributed Bus bit 1 |
| TIxDB0      | Map Transition Board Input x to Distributed Bus bit 0 |
| TIxSEN1     | Map Transition Board Input x to Sequence External Enable 1 |
| TIxSEN0     | Map Transition Board Input x to Sequence External Enable 0 |
| TIxSEQ1     | Map Transition Board Input x to Sequence Trigger 1 |
| TIxSEQ0     | Map Transition Board Input x to Sequence Trigger 0 |
| TIxEV7      | Map Transition Board Input x to Event Trigger 7 |
| TIxEV6      | Map Transition Board Input x to Event Trigger 6 |
| TIxEV5      | Map Transition Board Input x to Event Trigger 5 |
| TIxEV4      | Map Transition Board Input x to Event Trigger 4 |
| TIxEV3      | Map Transition Board Input x to Event Trigger 3 |
| TIxEV2      | Map Transition Board Input x to Event Trigger 2 |
| TIxEV1      | Map Transition Board Input x to Event Trigger 1 |
| TIxEV0      | Map Transition Board Input x to Event Trigger 0 |


```{note}
All enabled input signals are OR’ed together. So if e.g. distributed bus bit 0 has two sources from
universal input 0 and 1, if either of the inputs is active high also the distributed bus is active high.
```

### Embedded Event Receivers

The EVM-300 firmware includes two embedded event receivers. The downstream event receiver (EVRD) receives
the event stream from port U whereas the upstream event receiver (EVRU) receives the concentrated event
stream from ports 1 through 8.

The downstream event receiver (EVRD) is located in the EVG register map at offset 0x20000 through
0x2ffff and the upstream event receiver (EVRU) is located in the EVG register map at offset 0x30000
through 0x3ffff. The event receiver register map follows the description further in this document.

The event master has a number of internal signals which are connected following:

| Signal destination | Signal source |
| ------------------ | ------------- |
| EVG UNIVIN(0)      | EVRD FPOUT(0) |
| EVG UNIVIN(1)      | EVRD FPOUT(1) |
| EVG UNIVIN(2)      | EVRD FPOUT(2) |
| EVG UNIVIN(3)      | EVRD FPOUT(3) |
| EVG UNIVIN(4)      | EVRD FPOUT(4) |
| EVG UNIVIN(5)      | EVRD FPOUT(5) |
| EVG UNIVIN(6)      | EVRD FPOUT(6) |
| EVG UNIVIN(7)      | EVRD FPOUT(7) |
| EVG UNIVIN(8)      | EVRU FPOUT(0) |
| EVG UNIVIN(9)      | EVRU FPOUT(1) |
| EVG UNIVIN(10)     | EVRU FPOUT(2) |
| EVG UNIVIN(11)     | EVRU FPOUT(3) |
| EVG UNIVIN(12)     | EVRU FPOUT(4) |
| EVG UNIVIN(13)     | EVRU FPOUT(5) |
| EVG UNIVIN(14)     | EVRU FPOUT(6) |
| EVG UNIVIN(15)     | EVRU FPOUT(7) |
| EVRD FPIN(0)       | EVRU FPOUT(0) |
| EVRD FPIN(1)       | EVRU FPOUT(1) |
| EVRD FPIN(2)       | EVRU FPOUT(2) |
| EVRD FPIN(3)       | EVRU FPOUT(3) |
| EVRD FPIN(4)       | EVRU FPOUT(4) |
| EVRD FPIN(5)       | EVRU FPOUT(5) |
| EVRD FPIN(6)       | EVRU FPOUT(6) |
| EVRD FPIN(7)       | EVRU FPOUT(7) |
| EVRU FPIN(0)       | EVRD FPOUT(0) |
| EVRU FPIN(1)       | EVRD FPOUT(1) |
| EVRU FPIN(2)       | EVRD FPOUT(2) |
| EVRU FPIN(3)       | EVRD FPOUT(3) |
| EVRU FPIN(4)       | EVRD FPOUT(4) |
| EVRU FPIN(5)       | EVRD FPOUT(5) |
| EVRU FPIN(6)       | EVRD FPOUT(6) |
| EVRU FPIN(7)       | EVRD FPOUT(7) |

### FCT Function Register Map

| Address         | Register    | Type   | Description |
| -------         | --------    | ----   | ----------- |
| 0x000           | Status      | UINT32 | Status Register
| 0x004           | Control     | UINT32 | Control Register
| 0x010           | UpDCValue   | UINT32 | Upstream Data Compensation Delay Value
| 0x014           | FIFODCValue | UINT32 | Receive FIFO Data Compensation Delay Value
| 0x018           | IntDCValue  | UINT32 | FCT Internal Datapath Data Compensation Delay Value
| 0x02C           | TopologyID  | UINT32 | Timing Node Topology ID
| 0x040           | Port1DCValue| UINT32 | Port 1 loop delay value
| 0x044           | Port2DCValue| UINT32 | Port 2 loop delay value
| 0x048           | Port3DCValue| UINT32 | Port 3 loop delay value
| 0x04C           | Port4DCValue| UINT32 | Port 4 loop delay value
| 0x050           | Port5DCValue| UINT32 | Port 5 loop delay value
| 0x054           | Port6DCValue| UINT32 | Port 6 loop delay value
| 0x058           | Port7DCValue| UINT32 | Port 7 loop delay value
| 0x05C           | Port8DCValue| UINT32 | Port 8 loop delay value
| 0x1000 – 0x10FF | SFP1EEPROM  |        | Port 1 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1100 – 0x11FF | SFP1DIAG    |        | Port 1 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1200 – 0x12FF | SFP2EEPROM  |        | Port 2 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1300 – 0x13FF | SFP2DIAG    |        | Port 2 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1400 – 0x14FF | SFP3EEPROM  |        | Port 3 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1500 – 0x15FF | SFP3DIAG    |        | Port 3 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1600 – 0x16FF | SFP4EEPROM  |        | Port 4 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1700 – 0x17FF | SFP4DIAG    |        | Port 4 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1800 – 0x18FF | SFP5EEPROM  |        | Port 5 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1900 – 0x19FF | SFP5DIAG    |        | Port 5 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1A00 – 0x1AFF | SFP6EEPROM  |        | Port 6 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1B00 – 0x1BFF | SFP6DIAG    |        | Port 6 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1C00 – 0x1CFF | SFP7EEPROM  |        | Port 7 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1D00 – 0x1DFF | SFP7DIAG    |        | Port 7 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1E00 – 0x1EFF | SFP8EEPROM  |        | Port 8 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1F00 – 0x1FFF | SFP8DIAG    |        | Port 8 SFP Transceiver diagnostics (SFP address 0xA2)

#### FCT Link Status Register

| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x001   | LINK8  | LINK7  | LINK6  | LINK5  | LINK4  | LINK3  | LINK2  | LINK1  |
|         | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| 0x003   | VIO8   | VIO7   | VIO6   | VIO5   | VIO4   | VIO3   | VIO2   | VIO1   |

| Bit | Function |
| --- | -------- |
| LINK8 | Port 8 RX Status, 1 – link up, 0 – link down |
| LINK7 | Port 7 RX Status, 1 – link up, 0 – link down |
| LINK6 | Port 6 RX Status, 1 – link up, 0 – link down |
| LINK5 | Port 5 RX Status, 1 – link up, 0 – link down |
| LINK4 | Port 4 RX Status, 1 – link up, 0 – link down |
| LINK3 | Port 3 RX Status, 1 – link up, 0 – link down |
| LINK2 | Port 2 RX Status, 1 – link up, 0 – link down |
| LINK1 | Port 1 RX Status, 1 – link up, 0 – link down |
| VIO8  | Port 8 RX Violation |
| VIO7  | Port 7 RX Violation |
| VIO6  | Port 6 RX Violation |
| VIO5  | Port 5 RX Violation |
| VIO4  | Port 4 RX Violation |
| VIO3  | Port 3 RX Violation |
| VIO2  | Port 2 RX Violation |
| VIO1  | Port 1 RX Violation |

#### FCT Link Control Register

| address | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x007   | CLRV8  | CLRV7  | CLRV6  | CLRV5  | CLRV4  | CLRV3  | CLRV2  | CLRV1  |

| Bit   | Function |
| ---   | -------- |
| CLRV8 | Clear RX Violation Port 8 |
| CLRV7 | Clear RX Violation Port 7 |
| CLRV6 | Clear RX Violation Port 6 |
| CLRV5 | Clear RX Violation Port 5 |
| CLRV4 | Clear RX Violation Port 4 |
| CLRV3 | Clear RX Violation Port 3 |
| CLRV2 | Clear RX Violation Port 2 |
| CLRV1 | Clear RX Violation Port 1 |
