## Event Receiver Registermap

Event Receiver register/memory map.

### Register Map

| Address | Register | Type | Description |
| ------- | -------- | ---- | ------------|
| 0x000 | Status         | UINT32 | [Status Register](#status-register)
| 0x004 | Control        | UINT32 | [Control Register](#control-register)
| 0x008 | IrqFlag        | UINT32 | [Interrupt Flag Register](#interrupt-flag-register)
| 0x00C | IrqEnable      | UINT32 | [Interrupt Enable Register](#interrupt-enable-register)
| 0x010 | PulseIrqMap    | UINT32 | [Mapping register for pulse interrupt](#hardware-interrupt-mapping-register)
| 0x018 | SWEvent        | UINT32 | [Software event register](#software-event-register)
| 0x01C | PCIIrqEnable   | UINT32 | [PCI Interrupt Enable Register](#pci-interrupt-enable-register)
| 0x020 | DataBufCtrl    | UINT32 | [Data Buffer Control and Status Register](#receive-data-buffer-control-and-status-register)
| 0x024 | TxDataBufCtrl  | UINT32 | [TX Data Buffer Control and Status Register](#transmit-data-buffer-control-register) 
| 0x028 | TxSegBufCtrl   | UINT32 | [TX Segmented Data Buffer Control and Status Register](#transmit-segemented-data-buffer-control-register)
| 0x02C | FWVersion      | UINT32 | [Firmware Version Register](#fpga-firmware-version-register)
| 0x040 | EvCntPresc     | UINT32 | Event Counter Prescaler
| 0x04C | UsecDivider    | UINT32 | Divider to get from Event Clock to 1 MHz
| 0x050 | ClockControl   | UINT32 | [Event Clock Control Register](#clock-control-register)
| 0x05C | SecSR          | UINT32 | Seconds Shift Register
| 0x060 | SecCounter     | UINT32 | Timestamp Seconds Counter
| 0x064 | EventCounter   | UINT32 | Timestamp Event Counter
| 0x068 | SecLatch       | UINT32 | Timestamp Seconds Counter Latch
| 0x06C | EvCntLatch     | UINT32 | Timestamp Event Counter Latch
| 0x070 | EvFIFOSec      | UINT32 | Event FIFO Seconds Register
| 0x074 | EvFIFOEvCnt    | UINT32 | Event FIFO Event Counter Register
| 0x078 | EvFIFOCode     | UINT16 | Event FIFO Event Code Register
| 0x07C | LogStatus      | UINT32 | Event Log Status Register
| 0x080 | FracDiv        | UINT32 | [Micrel SY87739L Fractional Divider Configuration Word](#sy87739l-fractional-divider-configuration-word)
| 0x090 | GPIODir        | UINT32 | Front Panel UnivIO GPIO signal direction
| 0x094 | GPIOIn         | UINT32 | Front Panel UnivIO GPIO input register
| 0x098 | GPIOOut        | UINT32 | Front Panel UnivIO GPIO output register
| 0x0A0 | SPIData        | UINT32 | [SPI Data Register](#spi-configuration-flash-registers)
| 0x0A4 | SPIControl     | UINT32 | [SPI Control Register](#spi-configuration-flash-registers)
| 0x0B0 | DCTarget       | UINT32 | Delay Compensation Target Value
| 0x0B4 | DCRxValue      | UINT32 | Delay Compensation Transmission Path Delay Value
| 0x0B8 | DCIntValue     | UINT32 | Delay Compensation Internal Delay Value
| 0x0BC | DCStatus       | UINT32 | [Delay Compensation Status Register](#delay-compensation-status-register)
| 0x0C0 | TopologyID     | UINT32 | Timing Node Topology ID
| 0x0E0 | SeqRamCtrl     | UINT32 | [Sequence RAM Control Register](#sequence-ram-control-register)
| 0x100 | Prescaler0     | UINT32 | Prescaler 0 Divider
| 0x104 | Prescaler1     | UINT32 | Prescaler 1 Divider
| 0x108 | Prescaler2     | UINT32 | Prescaler 2 Divider
| 0x10C | Prescaler3     | UINT32 | Prescaler 3 Divider
| 0x110 | Prescaler4     | UINT32 | Prescaler 4 Divider
| 0x114 | Prescaler5     | UINT32 | Prescaler 5 Divider
| 0x118 | Prescaler6     | UINT32 | Prescaler 6 Divider
| 0x11C | Prescaler7     | UINT32 | Prescaler 7 Divider
| 0x120 | PrescPhase0    | UINT32 | Prescaler 0 Phase Offset Register
| 0x124 | PrescPhase1    | UINT32 | Prescaler 1 Phase Offset Register
| 0x128 | PrescPhase2    | UINT32 | Prescaler 2 Phase Offset Register
| 0x12C | PrescPhase3    | UINT32 | Prescaler 3 Phase Offset Register
| 0x130 | PrescPhase4    | UINT32 | Prescaler 4 Phase Offset Register
| 0x134 | PrescPhase5    | UINT32 | Prescaler 5 Phase Offset Register
| 0x138 | PrescPhase6    | UINT32 | Prescaler 6 Phase Offset Register
| 0x13C | PrescPhase7    | UINT32 | Prescaler 7 Phase Offset Register
| 0x140 | PrescTrig0     | UINT32 | [Prescaler 0 Pulse Generator Trigger Register](#prescaler-pulse-trigger-registers)
| 0x144 | PrescTrig1     | UINT32 | Prescaler 1 Pulse Generator Trigger Register
| 0x148 | PrescTrig2     | UINT32 | Prescaler 2 Pulse Generator Trigger Register
| 0x14C | PrescTrig3     | UINT32 | Prescaler 3 Pulse Generator Trigger Register
| 0x150 | PrescTrig4     | UINT32 | Prescaler 4 Pulse Generator Trigger Register
| 0x154 | PrescTrig5     | UINT32 | Prescaler 5 Pulse Generator Trigger Register
| 0x158 | PrescTrig6     | UINT32 | Prescaler 6 Pulse Generator Trigger Register
| 0x15C | PrescTrig7     | UINT32 | Prescaler 7 Pulse Generator Trigger Register
| 0x180 | DBusTrig0      | UINT32 | [DBus Bit 0 Pulse Generator Trigger Register](#distributed-bus-pulse-trigger-registers)
| 0x184 | DBusTrig1      | UINT32 | DBus Bit 1 Pulse Generator Trigger Register
| 0x188 | DBusTrig2      | UINT32 | DBus Bit 2 Pulse Generator Trigger Register
| 0x18C | DBusTrig3      | UINT32 | DBus Bit 3 Pulse Generator Trigger Register
| 0x190 | DBusTrig4      | UINT32 | DBus Bit 4 Pulse Generator Trigger Register
| 0x194 | DBusTrig5      | UINT32 | DBus Bit 5 Pulse Generator Trigger Register
| 0x198 | DBusTrig6      | UINT32 | DBus Bit 6 Pulse Generator Trigger Register
| 0x19C | DBusTrig7      | UINT32 | DBus Bit 7 Pulse Generator Trigger Register
| 0x200 | Pulse0Ctrl     | UINT32 | [Pulse 0 Control Register](#pulse-generator-registers)
| 0x204 | Pulse0Presc    | UINT32 | Pulse 0 Prescaler Register
| 0x208 | Pulse0Delay    | UINT32 | Pulse 0 Delay Register
| 0x20C | Pulse0Width    | UINT32 | Pulse 0 Width Register
| 0x210 | Pulse 1 Registers
| 0x220 | Pulse 2 Registers
| ...| | 
| 0x3F0 | Pulse 31 Registers
| 0x400 | FPOutMap0      | UINT16 | Front Panel Output 0 Map Register
| 0x402 | FPOutMap1      | UINT16 | Front Panel Output 1 Map Register
| 0x404 | FPOutMap2      | UINT16 | Front Panel Output 2 Map Register
| 0x406 | FPOutMap3      | UINT16 | Front Panel Output 3 Map Register
| 0x408 | FPOutMap4      | UINT16 | Front Panel Output 4 Map Register
| 0x40A | FPOutMap5      | UINT16 | Front Panel Output 5 Map Register
| 0x40C | FPOutMap6      | UINT16 | Front Panel Output 6 Map Register
| 0x40E | FPOutMap7      | UINT16 | Front Panel Output 7 Map Register
| 0x440 | UnivOutMap0    | UINT16 | Front Panel Universal Output 0 Map Register
| 0x442 | UnivOutMap1    | UINT16 | Front Panel Universal Output 1 Map Register
| 0x444 | UnivOutMap2    | UINT16 | Front Panel Universal Output 2 Map Register
| 0x446 | UnivOutMap3    | UINT16 | Front Panel Universal Output 3 Map Register
| 0x448 | UnivOutMap4    | UINT16 | Front Panel Universal Output 4 Map Register
| 0x44A | UnivOutMap5    | UINT16 | Front Panel Universal Output 5 Map Register
| 0x44C | UnivOutMap6    | UINT16 | Front Panel Universal Output 6 Map Register
| 0x44E | UnivOutMap7    | UINT16 | Front Panel Universal Output 7 Map Register
| 0x450 | UnivOutMap8    | UINT16 | Front Panel Universal Output 8 Map Register
| 0x452 | UnivOutMap9    | UINT16 | Front Panel Universal Output 9 Map Register
| 0x454 | UnivOutMap10   | UINT16 | Front Panel Universal Output 10 Map Register
| 0x456 | UnivOutMap11   | UINT16 | Front Panel Universal Output 11 Map Register
| 0x458 | UnivOutMap12   | UINT16 | Front Panel Universal Output 12 Map Register
| 0x45A | UnivOutMap13   | UINT16 | Front Panel Universal Output 13 Map Register
| 0x45C | UnivOutMap14   | UINT16 | Front Panel Universal Output 14 Map Register
| 0x45E | UnivOutMap15   | UINT16 | Front Panel Universal Output 15 Map Register
| 0x460 | UnivOutMap16   | UINT16 | Front Panel Universal Output 16 Map Register
| 0x462 | UnivOutMap17   | UINT16 | Front Panel Universal Output 17 Map Register
| 0x480 | TBOutMap0      | UINT16 | Transition Board Output 0 Map Register
| 0x482 | TBOutMap1      | UINT16 | Transition Board Output 1 Map Register
| 0x484 | TBOutMap2      | UINT16 | Transition Board Output 2 Map Register
| 0x486 | TBOutMap3      | UINT16 | Transition Board Output 3 Map Register
| 0x488 | TBOutMap4      | UINT16 | Transition Board Output 4 Map Register
| 0x48A | TBOutMap5      | UINT16 | Transition Board Output 5 Map Register
| 0x48C | TBOutMap6      | UINT16 | Transition Board Output 6 Map Register
| 0x48E | TBOutMap7      | UINT16 | Transition Board Output 7 Map Register
| 0x490 | TBOutMap8      | UINT16 | Transition Board Output 8 Map Register
| 0x492 | TBOutMap9      | UINT16 | Transition Board Output 9 Map Register
| 0x494 | TBOutMap10     | UINT16 | Transition Board Output 10 Map Register
| 0x496 | TBOutMap11     | UINT16 | Transition Board Output 11 Map Register
| 0x498 | TBOutMap12     | UINT16 | Transition Board Output 12 Map Register
| 0x49A | TBOutMap13     | UINT16 | Transition Board Output 13 Map Register
| 0x49C | TBOutMap14     | UINT16 | Transition Board Output 14 Map Register
| 0x49E | TBOutMap15     | UINT16 | Transition Board Output 15 Map Register
| 0x4A0 | TBOutMap16     | UINT16 | Transition Board Output 16 Map Register
| 0x4A2 | TBOutMap17     | UINT16 | Transition Board Output 17 Map Register
| 0x4A4 | TBOutMap18     | UINT16 | Transition Board Output 18 Map Register
| 0x4A6 | TBOutMap19     | UINT16 | Transition Board Output 19 Map Register
| 0x4A8 | TBOutMap20     | UINT16 | Transition Board Output 20 Map Register
| 0x4AA | TBOutMap21     | UINT16 | Transition Board Output 21 Map Register
| 0x4AC | TBOutMap22     | UINT16 | Transition Board Output 22 Map Register
| 0x4AE | TBOutMap23     | UINT16 | Transition Board Output 23 Map Register
| 0x4B0 | TBOutMap24     | UINT16 | Transition Board Output 24 Map Register
| 0x4B2 | TBOutMap25     | UINT16 | Transition Board Output 25 Map Register
| 0x4B4 | TBOutMap26     | UINT16 | Transition Board Output 26 Map Register
| 0x4B6 | TBOutMap27     | UINT16 | Transition Board Output 27 Map Register
| 0x4B8 | TBOutMap28     | UINT16 | Transition Board Output 28 Map Register
| 0x4BA | TBOutMap29     | UINT16 | Transition Board Output 29 Map Register
| 0x4BC | TBOutMap30     | UINT16 | Transition Board Output 30 Map Register
| 0x4BE | TBOutMap31     | UINT16 | Transition Board Output 31 Map Register
| 0x4C0 | BPOutMap0      | UINT16 | Backplane Output 0 Map Register
| 0x4C2 | BPOutMap1      | UINT16 | Backplane Output 1 Map Register
| 0x4C4 | BPOutMap2      | UINT16 | Backplane Output 2 Map Register
| 0x4C6 | BPOutMap3      | UINT16 | Backplane Output 3 Map Register
| 0x4C8 | BPOutMap4      | UINT16 | Backplane Output 4 Map Register
| 0x4CA | BPOutMap5      | UINT16 | Backplane Output 5 Map Register
| 0x4CC | BPOutMap6      | UINT16 | Backplane Output 6 Map Register
| 0x4CE | BPOutMap7      | UINT16 | Backplane Output 7 Map Register
| 0x500 | FPInMap0       | UINT32 | [Front Panel Input 0 Mapping Register](#input-mapping-registers)
| 0x504 | FPInMap1       | UINT32 | Front Panel Input 1 Mapping Register
| ...| | 
| 0x510 | UnivInMap0     | UINT32 | Universal Input 0 Mapping Register
| 0x514 | UnivInMap1     | UINT32 | Universal Input 1 Mapping Register
| ...| | 
| 0x560 | BPInMap0       | UINT32 | Backplane Input 0 Mapping Register
| 0x564 | BPInMap1       | UINT32 | Backplane Input 1 Mapping Register
| ...| | 
| 0x580 | TBDly0       | UINT32 | Transition Board -DLY Module Output 0 Delay. Value 0-1023
| 0x584 | TBDly1       | UINT32 | Transition Board -DLY Module Output 1 Delay. Value 0-1023
| ...| | 
| 0x5C0 | TBInMap0       | UINT32 | Transition Board Input 0 Mapping Register
| 0x5C4 | TBInMap1       | UINT32 | Transition Board Input 1 Mapping Register
| ...| | 
| 0x610 | GTX0Ctrl       | UINT32 | GTX0 Output Control Register
| 0x614 | GTX0HP         | UINT16 | GTX0 Output High Period Count
| 0x616 | GTX0LP         | UINT16 | GTX0 Output Low Period Count
| 0x618 | GTX0Samp       | UINT32 | GTX0 Output Number of 40 bit word patterns
| 0x61C | GTX0PS         | UINT32 | GTX0 Phase Shift Offset Register
| 0x630 | GTX1Ctrl       | UINT32 | GTX1 Output Control Register
| 0x634 | GTX1HP         | UINT16 | GTX1 Output High Period Count
| 0x636 | GTX1LP         | UINT16 | GTX1 Output Low Period Count
| 0x638 | GTX1Samp       | UINT32 | GTX1 Output Number of 40 bit word patterns
| 0x63C | GTX1PS         | UINT32 | GTX1 Phase Shift Offset Register
| 0x650 | GTX2Ctrl       | UINT32 | GTX2 Output Control Register
| 0x654 | GTX2HP         | UINT16 | GTX2 Output High Period Count
| 0x656 | GTX2LP         | UINT16 | GTX2 Output Low Period Count
| 0x658 | GTX2Samp       | UINT32 | GTX2 Output Number of 40 bit word patterns
| 0x65C | GTX2PS         | UINT32 | GTX2 Phase Shift Offset Register
| 0x670 | GTX3Ctrl       | UINT32 | GTX3 Output Control Register
| 0x674 | GTX3HP         | UINT16 | GTX3 Output High Period Count
| 0x676 | GTX3LP         | UINT16 | GTX3 Output Low Period Count
| 0x678 | GTX3Samp       | UINT32 | GTX3 Output Number of 40 bit word patterns
| 0x67C | GTX3PS         | UINT32 | GTX3 Phase Shift Offset Register
| 0x610 | GTX4Ctrl       | UINT32 | GTX4 Output Control Register
| 0x694 | GTX4HP         | UINT16 | GTX4 Output High Period Count
| 0x696 | GTX4LP         | UINT16 | GTX4 Output Low Period Count
| 0x698 | GTX4Samp       | UINT32 | GTX4 Output Number of 40 bit word patterns
| 0x69C | GTX4PS         | UINT32 | GTX4 Phase Shift Offset Register
| 0x6B0 | GTX5Ctrl       | UINT32 | GTX5 Output Control Register
| 0x6B4 | GTX5HP         | UINT16 | GTX5 Output High Period Count
| 0x6B6 | GTX5LP         | UINT16 | GTX5 Output Low Period Count
| 0x6B8 | GTX5Samp       | UINT32 | GTX5 Output Number of 40 bit word patterns
| 0x6BC | GTX5PS         | UINT32 | GTX5 Phase Shift Offset Register
| 0x800 – 0xFFF   | DataBuf   | | Data Buffer Receive Memory
| 0x1000 – 0x17FF |           | | Diagnostics counters |
| 0x1800 – 0x1FFF | TxDataBuf | | Data Buffer Transmit Memory
| 0x2000 – 0x3FFF | EventLog |  | 512 x 16 byte position Event Log
| 0x4000 – 0x4FFF | MapRam1 |   | Event Mapping RAM 1
| 0x5000 – 0x5FFF | MapRam2 |   | Event Mapping RAM 2
| 0x7200 | Pulse0RepCnt | UINT32 | Pulse 0 Repetition Count Register |
| 0x7204 | Pulse0RepDelay | UINT32 | Pulse 0 Repeat Delay Register |
| 0x7210 | Pulse1RepCnt | UINT32 | Pulse 1 Repetition Count Register |
| 0x7214 | Pulse1RepDelay | UINT32 | Pulse 1 Repeat Delay Register |
| 0x7220 | Pulse2RepCnt | UINT32 | Pulse 2 Repetition Count Register |
| 0x7224 | Pulse2RepDelay | UINT32 | Pulse 2 Repeat Delay Register |
| ...    | ......        | ....... | ...      |
| 0x73F0 | Pulse31RepCnt | UINT32 | Pulse 31 Repetition Count Register |
| 0x73F4 | Pulse31RepDelay | UINT32 | Pulse 31 Repeat Delay Register |
| 0x8000 – 0x80FF | configROM |
| 0x8100 – 0x81FF | scratchRAM |
| 0x8200 – 0x82FF | SFPEEPROM  | | SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x8300 – 0x83FF | SFPDIAG    | | SFP Transceiver diagnostics (SFP address 0xA2)
| 0x8800 | DataBufRXSize0    | UINT32  | Segmented Data Buffer Segment 0 Receive Size Register
| 0x8804 | SDataBufRXSize0   | UINT32 | Segmented Data Buffer Segment 1 Receive Size Register
| ...    | ......        | ....... | ...      |
| 0x89FC | SDataBufRXSize127 | UINT32 | Segmented Data Buffer Segment 127 Receive Size Register
| 0x8F80 – 0x8F8F | SDataBufSIrqEna |  | [Segmented Data Buffer Segment Interrupt Enable Register](#data-buffer-segment-interrupt-enable-register)
| 0x8FA0 – 0x8FAF | SDataBufCSFlag  |  | [Segmented Data Buffer Segment Checksum Flags](#data-buffer-checksum-flag-register)
| 0x8FC0 – 0x8FCF | SDataBufOVFlag  |  | [Segmented Data Buffer Segment Overflow Flags](#data-buffer-overflow-flag-register)
| 0x8FE0 – 0x8FEF | SDataBufRxFlag  |  | [Segmented Data Buffer Segment Receive Flags](#data-buffer-receive-flag-register)
| 0x9000 – 0x97FF | SDataBufData    |  | Segmented Data Buffer Segment Data Memory
| 0xA000 – 0xA7FF | SDataBufData    |  | Segmented Data Buffer Transmit Memory
| 0xC000 – 0xFFFF | SeqRam | | Sequence RAM
| 0x20000 – 0x23FFF  | GTX0MEM | Pattern memory:
| | | | 16k bytes GTX output 0 (VME-EVR-300)
| | | | 16k bytes GTX output 0 (mTCA-EVR-300U/RF TCLKA)
| 0x24000 – 0x27FFF | GTX1MEM  | Pattern memory:
| | | | 16k bytes GTX output 1 (VME-EVR-300)
| | | | 16k bytes GTX output 0 (mTCA-EVR-300U/RF TCLKB)
| 0x28000 – 0x2BFFF | GTX2MEM  | Pattern memory:
| | | | 16k bytes GTX output 2 (VME-EVR-300)
| | | | 16k bytes GTX output 0 (mTCA-EVR-300U/RF UNIV2)
| 0x2C000 – 0x2FFFF | GTX3MEM  | Pattern memory:
| | | | 16k bytes GTX output 3 (VME-EVR-300)
| | | | 16k bytes GTX output 0 (mTCA-EVR-300U/RF UNIV3)
| 0x2C000 – 0x2FFFF | GTX3MEM  | Pattern memory:
| | | | 16k bytes GTX output 4 (VME-EVR-300)
| | | | 16k bytes GTX output 0 (mTCA-EVR-300U/RF GTX/GUN-TX)
| 0x2C000 – 0x2FFFF | GTX3MEM  | Pattern memory:
| | | | 16k bytes GTX output 5 (VME-EVR-300)
| | | | 16k bytes GTX output 0 (mTCA-EVR-300U/RF GTX CML)

### Status Register


| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x000   | DBUS7  | DBUS6  | DBUS5  | DBUS4  | DBUS3  | DBUS2  | DBUS1  | DBUS0  |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x001   |        |        |        |        |        |        |        | LEGVIO |
| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x002
| address | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x003   |  SFPMOD | LINK | LOGSTP |


| Bit   | Function |
| ----- | -------- |
|DBUS7  | Read status of DBUS bit 7
|DBUS6  | Read status of DBUS bit 6
|DBUS5  | Read status of DBUS bit 5
|DBUS4  | Read status of DBUS bit 4
|DBUS3  | Read status of DBUS bit 3
|DBUS2  | Read status of DBUS bit 2
|DBUS1  | Read status of DBUS bit 1
|DBUS0  | Read status of DBUS bit 0
|LEGVIO | Legacy VIO (series 100, 200 and 230)
|SFPMOD | SFP module status:
|       |‘0’ – plugged in
|       |‘1’ – no module installed
|LINK   | Link status:
|       | ‘0’ – link down
|       | ‘1’ – link up
|LOGSTP | Event Log stopped flag

### Control Register


| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x004   | EVREN  | EVFWD  | TXLP   |  RXLP  | OUTEN  | SRST   | LEMDE  | GTXIO  |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x005   |        | DCENA  |
| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x006   | PRPOL  | TSDBUS | RSTS   |        |        |   LTS  | MAPEN  | MAPRS  |
| address | bit 7  | bit 6 | bit 5   |  bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x007   | LOGRS  | LOGEN | LOGDIS  | LOGSE  | RSFIFO |

| Bit    | Function |
| ---    | -------- |
| EVREN  | Event Receiver Master enable
| EVFWD  | Event forwarding enable:
|        | 0 – Events not forwarded
|        | 1 – Events received with forward bit in mapping RAM set are sent back on TX
| TXLP   | Transmitter loopback:
|        | 0 – Receive signal from SFP transceiver (normal operation)
|        | 1 – Loopback EVR TX into EVR RX
| RXLP   | Receiver loopback:
|        | 0 – Transmit signal from EVR on SFP transceiver TX
|        | 1 – Loopback SFP RX on SFP TX
| OUTEN  | Output enable for FPGA external components / IFB-300 (cPCI-EVRTG-300, PCIe-EVR-300, PXIe-EVR-300I)
|        | 0 – disable outputs
|        | 1 – enable outputs
| SRST   | Soft reset IP
| LEMDE  |  Little endian mode (cPCI-EVR-300, PCIe-EVR-300)
|        | 0 – PCI core in big endian mode (power up default)
|        | 1 – PCI core in little endian mode
| GTXIO  | GUN-TX output hardware inhibit override
|        | 0 – honor hardware inhibit signal (default)
|        | 1 – inhibit override, don’t care about hardware inhibit input state
| DCENA  | Delay compensation mode enable
|        | 0 – Delay compensation mode disable (receive FIFO depth controlled by DC Target).
|        | 1 – Delay compensation mode enable (receive FIFO depth controlled by DC Target - Datapath Delay).
| PRPOL  | Prescaler Polarity select 
|        | 0 – Prescalers aligned on falling edge
|        | 1 – Prescalers aligned on rising edge
| TSDBUS |  Use timestamp counter clock on DBUS4
| RSTS   | Reset Timestamp. Write 1 to reset timestamp event counter and timestamp latch.
| LTS    | Latch Timestamp: Write 1 to latch timestamp from timestamp event counter to timestamp latch.
| MAPEN  | Event mapping RAM enable.
| MAPRS  | Mapping RAM select bit for event decoding:
|        | 0 – select mapping RAM 1
|        | 1 – select mapping RAM 2.
| LOGRS  | Reset Event Log. Write 1 to reset log.
| LOGEN  | Enable Event Log. Write 1 to (re)enable event log.
| LOGDIS |  Disable Event Log. Write 1 to disable event log.
| LOGSE  | Log Stop Event Enable.
| RSFIFO | Reset Event FIFO. Write 1 to clear event FIFO.

### Interrupt Flag Register


| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x008 |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x009   |        |        |        | IFSOV  |        |        |        | IFSHF  |
|         | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x00A   |        |        |        | IFSSTO |        |        |        | IFSSTA |
| address | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0 |
| 0x00B   | IFSEGD | IFLINK | IFDBUF | IFHW   | IFEV   | IFHB   | IFFF   | IFVIO |

| Bit    | Function |
| ---    | -------- |
| IFSOV  | Sequence RAM sequence roll over interrupt flag
| IFSHF  | Sequence RAM sequence halfway through interrupt flag
| IFSSTO | Sequence RAM sequence stop interrupt flag
| IFSSTA | Sequence RAM sequence start interrupt flag
| IFSEGD | Segmented data buffer interrupt flag
| IFLINK | Link state change interrupt flag
| IFDBUF | Data buffer interrupt flag
| IFHW   | Hardware interrupt flag (mapped signal)
| IFEV   | Event interrupt flag
| IFHB   | Heartbeat interrupt flag
| IFFF   | Event FIFO full flag
| IFVIO  | Receiver violation flag

### Interrupt Enable Register


| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x00C   | IRQEN |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x00D   |        |        |        | IESOV  |        |        |        | IESHF |
|         | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x00E   |        |        |        | IESSTO |        |        |        | IESSTA |
| address | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
|0x00F    | IESEGD | IELINK | IEDBUF | IEHW   | IEEV   | IEHB   | IEFF   | IEVIO  |

| Bit    | Function |
| ---    | -------- |
| IRQEN  | Master interrupt enable:
|        | 0 – disable all interrupts
|        | 1 – allow interrupts
| IESOV  | Sequence RAM sequence roll over interrupt enable
| IESHF  | Sequence RAM sequence halfway through interrupt enable
| IESSTO |  Sequence RAM sequence stop interrupt enable
| IESSTA |  Sequence RAM sequence start interrupt enable
| IESEGD |  Segmented data buffer interrupt enable
| IELINK |  Link state change interrupt enable
| IEDBUF |  Data buffer interrupt enable
| IEHW   | Hardware interrupt enable (mapped signal)
| IEEV   | Event interrupt enable
| IEHB   | Heartbeat interrupt enable
| IEFF   | Event FIFO full interrupt enable
| IEVIO  |  Receiver violation interrupt enable

### Hardware Interrupt Mapping Register


| address | bit 7     | bit 6     | bit 5     | bit 4     | bit 3     | bit 2     | bit 1     | bit 0     |
| ------- | ------    | ------    | ------    | ------    | ------    | ------    | ------    | ------    |
| 0x013   | MapID [7] | MapID [6] | MapID [5] | MapID [4] | MapID [3] | MapID [2] | MapID [1] | MapID [0] | 

Table: mapping IDs

| Mapping ID  | Signal |
| ----------  | ------ |
| 0 to n-1 | Pulse generator output (number n of pulse generators depends on HW and firmware version)
| n to 31 | (Reserved)
| 32 | Distributed bus bit 0 (DBUS0) 
| ...|  ...
| 39 | Distributed bus bit 7 (DBUS7)
| 40 | Prescaler 0
| 41 | Prescaler 1
| 42 | Prescaler 2
| 43 to 47 | (Reserved)
| 48 | Flip-flop output 0
| ...|  ...
| 55 | Flip-flop output 7
| 56 | to 58 (Reserved)
| 59 | Event clock output (only on PXIe-EVR-300)
| 60 | Event clock output with 180° phase shift (only on PXIe-EVR-300)
| 61 | Tri-state output (for PCIe-EVR-300DC with input module populated in IFB-300’s Universal I/O slot)
| 62 | Force output high (logic 1)
| 63 |  Force output low (logic 0)

#### Flip-flop Outputs (from FW version 0E0207)

There are 8 flip-flop outputs. Each of these is using two pulse generators, 
one for setting the output high and the other one for resetting the output low. 
In the table below you can see the relationship between flip-flops and pulse generators 
and the output mapping IDs.

| flip-flop | Mapping ID  | Set            | Reset       |
| --------- | ----------  | -------------- | ----------- |
| 0         | 48          | Pulse gen.  0  | Pulse gen. 1
| 1         | 49          | Pulse gen.  2  | Pulse gen. 3
| 2         | 50          | Pulse gen.  4  | Pulse gen. 5
| 3         | 51          | Pulse gen.  6  | Pulse gen. 7
| 4         | 52          | Pulse gen.  8  | Pulse gen. 9
| 5         | 53          | Pulse gen. 10  | Pulse gen. 11
| 6         | 54          | Pulse gen. 12  | Pulse gen. 13
| 7         | 55          | Pulse gen. 14  | Pulse gen. 15
         
### Software Event Register


| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x01A   |        |        |        |        |        |        | SWPEND | SWENA  |
| address | bit 7  | bit 6  | bit  5 | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| 0x01B   | EVC[7] | EVC[6] | EVC[5] | EVC[4] | EVC[3] | EVC[2] | EVC[1] | EVC[0] |



| Bit | Function |
| --- | -------- |
| SWPEND   | Event code waiting to be inserted (read-only). A new event code may be written
|          | to the event code register when this bit reads ‘0’.
| SWENA    | Enable software event
|          | When enabled ‘1’ a new event will be inserted into the receive event stream
|          | when event code is written to the event code register.
| EVC[7:0] | Event Code to be inserted into receive event stream

### PCI Interrupt Enable Register

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x01c   |        | PCIIE

| Bit   | Function |
| ---   | -------- |
| PCIIE | PCI core interrupt enable (PCIe-EVR-300DC, mTCA-EVR-300)

This bit is used by the low level driver to disable further interrupts before the
first interrupt has been handled in user space

### Receive Data Buffer Control and Status Register

| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| ------- | ------     | ------      | ----------| --------- | ---------- | ---------- | --------- | ---------- |
| 0x022   | DBRX/DBENA | DBRDY/DBDIS | DBCS      | DBEN      | RXSIZE[11] | RXSIZE[10] | RXSIZE[9] | RXSIZE[8]  |
| address | bit 7      | bit 6       | bit 5     | bit 4     | bit 3      | bit 2      | bit 1     | bit 0      |
| 0x023   | RXSIZE[7]  | RXSIZE[6]   | RXSIZE[5] | RXSIZE[4] | RXSIZE[3]  | RXSIZE[2]  | RXSIZE[1] | RXSIZE[0] |

| Bit    | Function |
| ---    | -------- |
| DBRX   | Data Buffer Receiving (read-only)
| DBENA  |  Set-up for Single Reception (write ‘1’ to set-up)
| DBRDY  |  Data Buffer Transmit Complete / Interrupt Flag
| DBDIS  |  Stop Reception (write ‘1’ to stop/disable)
| DBCS   | Data Buffer Checksum Error (read-only)
|        | Flag is cleared by writing ‘1’ to DBRX or DBRDY or disabling data buffer
| DBEN   | Data Buffer Enable Data Buffer Mode
|        | ‘0’ – Distributed bus not shared with data transmission, full speed distributed bus
|        | ‘1’ – Distributed bus shared with data transmission, half speed distributed bus
| RXSIZE | Data Buffer Received Buffer Size (read-only).

#### Transmit Data Buffer Control Register

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x024
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x025   |        |        |        | TXCPT  | TXRUN  | TRIG   | ENA    | 1      | 
| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x026   |         |         |         |         |         | DTSZ[10] | DTSZ[9] | DTSZ[8] |
| address | bit 7   | bit 6   | bit 5   | bit 4   | bit 3   | bit 2   | bit 1   | bit 0  |
| 0x027   | DTSZ[7] | DTSZ[6] | DTSZ[5] | DTSZ[4] | DTSZ[3] | DTSZ[2] |  0      | 0      |

| Bit        | Function |
| ---        | -------- |
| TXCPT      | Data Buffer Transmission Complete
| TXRUN      | Data Buffer Transmission Running – set when data transmission has been triggered and has not been completed yet
| TRIG       | Data Buffer Trigger Transmission
|            | Write ‘1’ to start transmission of data in buffer
| ENA        | Data Buffer Transmission enable
|            | ‘0’ – data transmission engine disabled
|            | ‘1’ – data transmission engine enabled
| DTSZ(10:2) | Data Transfer size 4 bytes to 2k in four byte increments

#### Transmit Segemented Data Buffer Control Register


| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x028   | SADDR[7] | SADDR[6] | SADDR[5] | SADDR[4] | SADDR[3] | SADDR[2] | SADDR[1] | SADDR[0] |
| address | bit 23   | bit 22   | bit 21   | bit 20   | bit 19   | bit 18   | bit 17   | bit 16 |
| 0x029   |          |          |          |TXCPT     | TXRUN    | TRIG     | ENA      | MODE   |
| address | bit 15   | bit 14   | bit 13   | bit 12   | bit 11   | bit 10   | bit 9    | bit 8  |
| 0x02A   |          |          |          |          |          | DTSZ[10] | DTSZ[9]  | DTSZ[8] |
| address | bit 7    | bit 6    | bit 5    | bit 4    | bit 3    | bit 2    | bit 1    | bit 0   |
| 0x02B   | DTSZ[7]  |  DTSZ[6] | DTSZ[5]  | DTSZ[4]  | DTSZ[3]  | DTSZ[2]  |   0      |   0     |

| Bit        | Function |
| ---        | -------- |
| SADDR      | Transfer Start Segment Address (16 byte segments)
| TXCPT      | Data Buffer Transmission Complete
| TXRUN      | Data Buffer Transmission Running – set when data transmission has been triggered and has not been completed yet
| TRIG       | ata Buffer Trigger Transmission
|            | Write ‘1’ to start transmission of data in buffer
| ENA        | Data Buffer Transmission enable
|            |‘0’ – data transmission engine disabled
|            |‘1’ – data transmission engine enabled
| MODE       | Distributed bus sharing mode
|            | ‘0’ – distributed bus not shared with data transmission
|            | ‘1’ – distributed bus shared with data transmission
| DTSZ(10:2) |Data Transfer size 4 bytes to 2k in four byte increments

### FPGA Firmware Version Register

| address | bit 31 | bit 30 | bit 29 | bit 28    | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------    | ------ | ------ | ------ | ------ |
| 0x02C   |        |        |        | EVR = 0x1 | FF[3]  | FF[2]  | FF[1]  | FF[0]  |
| address | bit 23 | bit 22 | bit 21 | bit 20    | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x02D   | SID[7] | SID[6] | SID[5] | SID[4]    | SID[3] | SID[2] | SID[1] | SID[0] |
| address | bit 15 | bit 14 | bit 13 | bit 12    | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x02E   | FID[7] | FID[6] | FID[5] | FID[4]    | FID[3] | FID[2] | FID[1] | FID[0] |
| address | bit 7  | bit 6  | bit 5  | bit 4     | bit 3  | bit 2  | bit 1  | bit 0  |
| 0x02F   | RID[7] | RID[6] | RID[5] | RID[4]    | RID[3] | RID[2] | RID[1] | RID[0] |


| Bit                    | Function |
| ---                    | -------- |
| Form Factor FF(3:0)    | 0 – CompactPCI 3U
|                        | 1 – PMC
|                        | 2 – VME64x
|                        | 3 – CompactRIO
|                        | 4 – CompactPCI 6U
|                        | 6 – PXIe
|                        | 7 – PCIe
|                        | 8 – mTCA.4
| Subrelease ID SID(7:0) | For production releases the subrelease ID counts up from 00.
|                        | For pre-releases this ID is used “backwards” counting down from ff i.e. when
|                        | approaching release 12000207, we have prereleases 12FF0206, 12FE0206,
|                        | 12FD0206 etc. in this order.
| Firmware ID FID(7:0)   |
|                        | 00 – Modular Register Map firmware (no delay compensation)
|                        | 01 – Reserved
|                        | 02 – Delay Compensation firmware
| Revision ID RID(7:0)   | See end of manual

### Clock Control Register


| address | bit 31 | bit 30   | bit 29   | bit 28   | bit 27 | bit 26   | bit 25   | bit 24 |
| ------- | ------ | ------   | ------   | ------   | ------ | ------   | ------   | ------ |
| 0x050   | PLLLOCK| BWSEL[2] | BWSEL[1] | BWSEL[0] |        | CLKMD[1] | CLKMD[0] |        |
| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x052   |        |        |        |        |        |        | CGLOCK |        |

| Bit | Function |
| --- | -------- |
| PLLLOCK   | Clock cleaner PLL Locked (read-only) to receiver recovered clock
| BWSEL2:0  |PLL Bandwidth Select (see Silicon Labs Si5317 datasheet)
|           | 000 – Si5317, BW setting HM (lowest loop bandwidth)
|           | 001 – Si5317, BW setting HL
|           | 010 – Si5317, BW setting MH
|           | 011 – Si5317, BW setting MM
|           | 100 – Si5317, BW setting ML (highest loop bandwidth)
| CLKMD1:0  | Event clock mode
|           | 00 – Event clock synchronized to upstream EVG. Event clock continues to run with same frequency if link is lost.
|           | 01 – Event clock synchronized to local fractional synthesizer reference.
|           | 10 – Event clock synchronized to upstream EVG. Fall back to local reference if upstream link is lost.
|           | 11 – Event clock synchronized to upstream EVG. Event clock is stopped if link is lost.
| CGLOCK    | Micrel fractional synthesizer SY87739L locked (read-only). This serves as the
|           | reference clock for the FPGA internal transceiver and indicates that a valid
|           | configuration word has been set in the FracDiv control register.

#### Event FIFO

Note that reading the FIFO event code registers pulls the event code and timestamp/seconds value from the
FIFO for access. The correct order to read an event from FIFO is to first read the event code register and
after this the timestamp/seconds registers in any order. Every read access to the FIFO event register pulls a
new event from the FIFO if it is not empty.

#### SY87739L Fractional Divider Configuration Word

The fractional synthesizer serves as the reference clock for the FPGA internal transceiver.

| Configuration Word | Frequency with 24 MHz reference oscillator |
| ------------------ | ------------------------------------------ |
| 0x0891C100         |     142.857 MHz
| 0x00DE816D         |     125 MHz
| 0x00FE816D         |     124.95 MHz
| 0x0C928166         |     124.9087 MHz
| 0x018741AD         |     119 MHz
| 0x072F01AD         |     114.24 MHz
| 0x049E81AD         |     106.25 MHz
| 0x008201AD         |     100 MHz
| 0x025B41ED         |     99.956 MHz
| 0x0187422D         |     89.25 MHz
| 0x0082822D         |     81 MHz
| 0x0106822D         |     80 MHz
| 0x019E822D         |     78.900 MHz
| 0x018742AD         |     71.4 MHz
| 0x0C9282A6         |     62.454 MHz
| 0x009743AD         |     50 MHz
| 0x0C25B43AD        |      49.978 MHz
| 0x0176C36D         |     49.965 MHz

### GPIO Pin Direction Register

| address | bit 31-0      |
| ------- | ----------    | 
| 0x090   | GPDIR         |

| Bit    | Function |
| ---    | -------- |
| GPDIRx | GPIO I/O Direction 
|        | 0:input
|        | 1: output

### SPI Configuration Flash Registers

| address | bit 7      | bit 6      | bit 5      | bit 4      | bit 3      | bit 2      | bit 1      | bit 0      |
| ------- | ---------- | ------     | ------     | ------     | ------     | ------     | ------     | ------     |
| 0x0A3   | SPIDATA[7] | SPIDATA[6] | SPIDATA[5] | SPIDATA[4] | SPIDATA[3] | SPIDATA[2] | SPIDATA[1] | SPIDATA[0] | 
| address | bit 7      | bit 6      | bit 5      | bit 4      | bit 3      | bit 2      | bit 1      | bit 0      |
| 0x0A7   | E          | RRDY       | TRDY       | TMT        | TOE        | ROE        | OE         | SSO        |

| Bit | Function |
| --- | -------- |
| SPIDATA(7:0) |Read SPI data byte / Write SPI data byte
| E            | Overrun Error flag
| RRDY         | Receiver ready, if ‘1’ data byte waiting in SPI_DATA
| TRDY         | Transmitter ready, if ‘1’ SPI_DATA is ready to accept new transmit data byte
| TMT          | Transmitter empty, if ‘1’ data byte has been transmitted
| TOE          | Transmitter overrun error
| ROE          | Receiver overrun error
| OE           | Output enable for SPI pins, ‘1’ enable SPI pins
| SSO          | Slave select output enable for SPI slave device, ‘1’ device selected

### Delay Compensation Status Register


| address | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2    | bit 1    | bit 0    |
| ------- | ------ | ------ | ------ | ------ | ------ | ------   | ------   | ------   |
| 0x0BE   |        |        |        |        |        | PDVLD[2] | PDVLD[1] | PDVLD[0] |
| address | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2    | bit 1    | bit 0    |
| 0x0BF   |        |        |        |        |DLYL    | DLYS     |          | DCLOCK   |

| Bit | Function |
| --- | -------- |
| PDVLD(2:0) | Path delay valid
| | 000 – Path delay value not valid from master EVM to EVR
| | 001 – Path delay value valid (coarse/quick acquisition)
| | 011 – Path delay value valid (medium precision/slow acquisition)
| | 111 – Path delay value valid (fine precision/slow acquisition)
| DLYL | Delay setting too long (delay shorter than target)
| DLYS | Delay setting too short (delay longer than target)
| DCLOCK | Delay fifo locked to setting/delay value

### Sequence RAM Control Register


| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x0E0   |        |        |        |        |        |        | SQRUN  | SQENA
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x0E1   |        |        |  SQSWT | SQSNG  | SQREC  | SQRES  | SQDIS  | SQEN |
| address | bit 7     | bit 6     | bit 5     | bit 4     | bit 3     | bit 2     | bit 1     | bit 0     |
| 0x0E3   | SQTSEL[7] | SQTSEL[6] | SQTSEL[5] | SQTSEL[4] | SQTSEL[3] | SQTSEL[2] | SQTSEL[1] | SQTSEL[0] |

| Bit    | Function |
| ---    | -------- |
| SQRUN  | Sequence RAM running flag (read-only)
| SQENA  | Sequence RAM enabled flag (read_only)
| SQSWT  | Sequence RAM software trigger, write ‘1’ to trigger
| SQSNG  | Sequence RAM single mode
| SQREC  | Sequence RAM recycle mode
| SQRES  | Sequence RAM reset, write ‘1’ to reset
| SQDIS  | Sequence RAM disable, write ‘1’ to disable
| SQEN   |Sequence RAM enable, write ‘1’ to enable/arm
| SQTSEL | 0 to n-1 – Pulse generator output
|        |n to 31 – (Reserved)
|        |32 to 39 – Distributed bus bit 0 (DBUS0) to bit 7 (DBUS7)
|        |40 to 47 – Prescaler 0 to Prescaler 7
|        |48 to 58 – (Reserved)
|        |61 – Software trigger
|        |62 – Continuous trigger
|        |63 – Trigger disabled

### Prescaler Pulse Trigger Registers

Each bit in the Prescaler Pulse Trigger Register corresponds to one pulse generator trigger. If for instance
bit 0 is set, pulse generator 0 gets trigger on each 0 to 1 transition of the corresponding prescaler.

### Distributed Bus Pulse Trigger Registers

Each bit in the Distributed Bus Pulse Trigger Register corresponds to one pulse generator trigger. If for
instance bit 0 is set, pulse generator 0 gets trigger on each 0 to 1 transition of the corresponding distributed
bus bit.

### Pulse Generator Registers


| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x200   | PxMASK[3] | PxMASK[2] | PxMASK[1] | PxMASK[0] | |  |  |  |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x201   | PxMENA[3] | PxMENA[2] | PxMENA[1] | PxMENA[0] |
| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9 | bit 8 |
| 0x202   |        |        |        |        |        |        | PxRME | PxSME |
| address | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x203   | PxOUT | PxSWS | PxSWR | PxPOL | PxMRE | PxMSE | PxMTE | PxENA

| address | bit 31...bit 0 |
| ------- | -------------- |
| 0x204   | Pulse Generator 0 Prescaler Register
| address | bit 31...bit 0
| 0x208   | Pulse Generator 0 Delay Register
| address | bit 31...bit 0
| 0x20C   | Pulse Generator 0 Width Register

| Bit | Function |
| --- | -------- |
| PxMASK(3:0) | Pulse HW Mask Register
| | 0 – HW masking disabled
| | 1 – HW masking enabled. When corresponding gate bit is active ‘1’ pulse triggers are blocked
| PxMENA(3:0) | Pulse HW Enable Register
| | 0 – HW enabling inactive
| | 1 – HW enabling active. When corresponding gate bit is inactive ‘0’ pulse triggers are blocked
| PxRME | Pulse Generator Apply mask to HW Reset
| PxSME | Pulse Generator Apply mask to HW Set
|PxOUT | Pulse Generator Output (read-only)
|PxSWS | Pulse Generator Software Set
|PxSWC | Pulse Generator Software Reset
|PxPOL | Pulse Generator Output Polarity
| | 0 – normal polarity
| | 1 – inverted polarity
|PxMRE | Pulse Generator Event Mapping RAM Reset Event Enable
| | 0 – Reset events disabled
| | 1 – Mapped Reset Events reset pulse generator output
|PxMSE | Pulse Generator Event Mapping RAM Set Event Enable
| | 0 – Set events disabled
| | 1 – Mapped Set Events set pulse generator output
|PxMTE | Pulse Generator Event Mapping RAM Trigger Event Enable
| | 0 – Event Triggers disabled
| | 1 – Mapped Trigger Events trigger pulse generator
|PxENA | Pulse Generator Enable
| | 0 – generator disabled
| | 1 – generator enabled

### Input Mapping Registers

The same bit mapping applies to Front Panel Inputs, Universal Inputs and Backplane Inputs.

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x500   | FPIN0  |        | EXTLV0 | BCKLE0 | EXTLE0 | EXTED0 | BCKEV0 | EXTEV0 |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x501   | T0DB7  | T0DB6  | T0DB5  | T0DB4  | T0DB3  | T0DB2  | T0DB1  | T0DB0  |

| address | bit 15 ... bit 8  |
| ------- | ----------------- |
| 0x502   | Backward Event Code Register for front panel input 0
| address | bit 7  ... bit 0  |
| 0x503   | External Event Code Register for front panel input 0

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x504   | FPIN1  |        | EXTLV1 | BCKLE1 | EXTLE1 | EXTED1 | BCKEV1 | EXTEV1 |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x505   | T1DB7  | T1DB6  | T1DB5  | T1DB4  | T1DB3  | T1DB2  | T1DB1  | T1DB0  |

| address | bit 15 ... bit 8  |
| ------- | ----------------- |
| 0x506 | Backward Event Code Register for front panel input 1
| address | bit 7  ... bit 0  |
| 0x507  | External Event Code Register for front panel input 1


| Bit | Function |
| --- | -------- |
| FPINx | Front panel Input x state.
| | 0 – low
| | 1 – high
| EXTLVx | Backward HW Event Level Sensitivity for input x
| | 0 – active high
| | 1 – active low
| BCKLEx | Backward HW Event Level Trigger enable for input x
| | 0 – disable level events
| | 1 – enable level events, send out backward event code every 1 us when input is
| | active (see EXTLVx for level sensitivity)
| EXTLEx | External HW Event Level Trigger enable for input x
| | 0 – disable level events
| | 1 – enable level events, apply external event code to active mapping RAM
| | every 1 us when input is active (see EXTLVx for level sensitivity)
| EXTEDx | Backward HW Event Edge Sensitivity for input x
| | 0 – trigger on rising edge
| | 1 – trigger on falling edge
| BCKEVx | Backward HW Event Edge Trigger Enable for input x
| | 0 – disable backward HW event
| | 1 – enable backward HW event, send out backward event code on detected
| | edge of hardware input (see EXTEDx bit for edge)
| EXTEVx | External HW Event Enable for input x
| | 0 – disable external HW event
| | 1 – enable external HW event, apply external event code to active mapping
| |RAM on edge of hardware input
| TxDB7-TxDB0 |  Backward distributed bus bit enable:
| | 0 – disable distributed bus bit
| | 1 – enable distributed bus bit control from hardware input: e.g. when TxDB7
| | is ‘1’ the hardware input x state is sent out on distributed bus bit 7.

### GTX Output Control Register
 
| address | bit 31...bit 16 |
| ------- | --------------- |
| 0x610 | Frequency mode trigger position

| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x612   |        |        |        |        | GTX3MD | GTX2MD | GTXPH1 | GTXPH0 |
| address | bit 7  |bit 6   | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| 0x613   | CMLRC  | CMLTL  | CMLMD(1:0) |    |        | CMLRES | CMLPWD | CMLENA |

| Bit | Function |
| --- | -------- |
| GTX3MD | GUN-TX-300 Mode (cPCI-EVRTG-300 only)
|  | 0 – CML/GTX Mode
|  | 1 – SFP output in GUN-TX-300 Mode
| GTX2MD | GUN-TX-203 Mode (cPCI-EVRTG-300 only)
|  | 0 – CML/GTX Mode
|  | 1 – SFP output in GUN-TX-203 Mode
| GTXPH1:0 | GUN-TX-203 Trigger output phase shift (cPCI-EVRTG-300 only)
|  | 00 – no delay
|  | 01 – output pulse delayed by ¼ event clock period ( ̃2 ns)
|  | 10 – output pulse delayed by ½ event clock period ( ̃4 ns)
|  | 11 – output pulse delayed by ¾ event clock period ( ̃6 ns)
| CMLRC | CML Pattern recycle
| CMLTL | CML Frequency mode trigger level
| CMLMD | CML Mode Select:
|  | 00 = classic mode
|  | 01 = frequency mode
|  | 10 = pattern mode
|  | 11 = undefined
| CMLRES | CML Reset
|  | 1 = reset CML output (default on EVR power up)
|  | 0 = normal operation
| CMLPWD | CML Power Down
|  | 1 = CML outputs powered down (default on EVR power up)
|  | 0 = normal operation
| CMLENA | CML Enable
|  | 0 = CML output disabled (default on EVR power up)
|  | 1 = CML output enabled

### Data Buffer Segment Interrupt Enable Register

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x8F80  | DBIE00 | DBIE01 | DBIE02 | DBIE03 | DBIE04 | DBIE05 | DBIE06 | DBIE07 |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x8F81  | DBIE08 | DBIE09 | DBIE0A | DBIE0B | DBIE0C | DBIE0D | DBIE0E | DBIE0F |
| ... |
| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x8F8E  | DBIE70 | DBIE71 | DBIE72 | DBIE73 | DBIE74 | DBIE75 | DBIE76 | DBIE77 |
| address | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| 0x8F8F  | DBIE78 | DBIE79 | DBIE7A | DBIE7B | DBIE7C | DBIE7D | DBIE7E | DBIE7F |


| Bit | Function |
| --- | -------- |
|DBIExx | Data Buffer Segment (16-byte segments) Interrupt Enable:
| | 0 – Interrupt for segment disabled
| | 1 – Interrupt for segment enabled
| | An interrupt will occur when the segment’s receive flag is active. To enable
| | Data Buffer interrupts the IEDBUF bit in the Interrupt Enable Register has to be set.

### Data Buffer Checksum Flag Register

| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x8FA0  | DBCS00 | DBCS01 | DBCS02 | DBCS03 | DBCS04 | DBCS05 | DBCS06 | DBCS07 |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x8FA1  | DBCS08 | DBCS09 | DBCS0A | DBCS0B | DBCS0C | DBCS0D | DBCS0E | DBCS0F |
| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x8FAE  | DBCS70 | DBCS71 | DBCS72 | DBCS73 | DBCS74 | DBCS75 | DBCS76 | DBCS77 |
| address | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| 0x8FAF  | DBCS78 | DBCS79 | DBCS7A | DBCS7B | DBCS7C | DBCS7D | DBCS7E | DBCS7F |

| Bit | Function |
| --- | -------- |
| DBCSxx | Data Buffer Segment (16-byte segments) Checksum Flag:
|  | 0 – Checksum OK
|  | 1 – Checksum error
|  | This flag is cleared by writing a ‘1’ into the segment’s DBRXxx bit in the DataBufRxFlag register.

#### Data Buffer Overflow Flag Register


| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x8FC0  | DBOV00 | DBOV01 | DBOV02 | DBOV03 | DBOV04 | DBOV05 | DBOV06 | DBOV07 |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x8FC1  | DBOV08 | DBOV09 | DBOV0A | DBOV0B | DBOV0C | DBOV0D | DBOV0E | DBOV0F |
| ... |
| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x8FCE  | DBOV70 | DBOV71 | DBOV72 | DBOV73 | DBOV74 | DBOV75 | DBOV76 | DBOV77 |
| address | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| 0x8FCF  | DBOV78 | DBOV79 | DBOV7A | DBOV7B | DBOV7C | DBOV7D | DBOV7E |DBOV7F  |

| Bit | Function |
| --- | -------- |
| DBOVxx | Data Buffer Segment (16-byte segments) Overflow Flag:
| | 0 – No overflow condition
| | 1 – Overflow: a new packet has been received before the DBRX flag for this segment was cleared
| | This flag is cleared by writing a ‘1’ into the segment’s DBRXxx bit in the DataBufRxFlag register.

### Data Buffer Receive Flag Register


| address | bit 31 | bit 30 | bit 29 | bit 28 | bit 27 | bit 26 | bit 25 | bit 24 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x8FE0  | DBRX00 | DBRX01 | DBRX02 | DBRX03 | DBRX04 | DBRX05 | DBRX06 | DBRX07 |
| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| 0x8FE1  | DBRX08 | DBRX09 | DBRX0A | DBRX0B | DBRX0C | DBRX0D | DBRX0E | DBRX0F |
| address | bit 15 | bit 14 | bit 13 | bit 12 | bit 11 | bit 10 | bit 9  | bit 8  |
| 0x8FEE  | DBRX70 | DBRX71 | DBRX72 | DBRX73 | DBRX74 | DBRX75 | DBRX76 | DBRX77 |
| address | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| 0x8FEF  | DBRX78 | DBRX79 | DBRX7A | DBRX7B | DBRX7C | DBRX7D | DBRX7E | DBRX7F |


| Bit | Function |
| --- | -------- |
|DBRXxx | Data Buffer Segment (16-byte segments) Receive Flag:
| | 0 – No packet received
| | 1 – Data packet received in this segment
| | This flag is cleared by writing a ‘1’ into the segment’s DBRXxx bit.

### SFP Module EEPROM and Diagnostics

Small Form Factor Pluggable (SFP) transceiver modules provide a means to identify the module by accessing 
an EEPROM. As an advanced feature some modules also support reading dynamic information
including module temperature, receive and transmit power levels etc. from the module. The EVR gives
access to all of this information through a memory window of 2 × 256 bytes. The first 256 bytes consist of
the EEPROM values and the rest of the advanced values.



**BASE ID FIELDS**

| Byte # | Field size | Notes                     | Value |
| ------ | ---------- | -----                     | ----- |
| 0     | 1         |Type of serial transceiver | 0x03 = SFP transceiver
| 1     | 1         | Extended identifier of type serial transceiver | 0x04 = serial ID module definition
| 2     | 1         | Code for connector type 0x07 = LC
| 3 – 10 | 8        | Code for electronic compatibility or optical compatibility
| 11 | 1 | Code for serial encoding algorithm
| 12 | 1 | Nominal bit rate, units of 100 MBits/sec
| 13 | 1 | Reserved
| 14 | 1 | Link length supported for 9/125 μm fiber, units of km
| 15 | 1 | Link length supported for 9/125 μm fiber, units of 100 m
| 16 | 1 | Link length supported for 50/125 μm fiber, units of 10 m
| 17 | 1 | Link length supported for 62.5/125 μm fiber, units of 10 m
| 18 | 1 | Link length supported for copper, units of meters
| 19 | 1 | Reserved
| 20 – 35 | 16 | SFP transceiver vendor name (ASCII)
| 36 | 1 | Reserved
| 37 – 39 | 3 | SFP transceiver vendor IEEE company ID
| 40 – 55 | 16|  Part number provided by SFP transceiver vendor (ASCII)
| 56 – 59 | 4 | Revision level for part number provided by vendor (ASCII)
| 60 – 62 | 3 | Reserved
| 63 | 1 | Check code for Base ID Fields

**EXTENDED ID FIELDS**

| Byte # | Field size | Notes                     | Value |
| ------ | ---------- | -----                     | ----- |
|64 – 65 | 2 | Indicated which optional SFP signals are implemented
|66 | 1 | Upper bit rate margin, units of %
|67 | 1 | Lower bit rate margin, units of %
|68 – 83 | 16 |  Serial number provided by vendor (ASCII)
|84 – 91 | 8  | Vendor’s manufacturing date code
|92 – 94 | 3  | Reserved
|95 | 1 | Check code for the Extended ID Fields

**VENDOR SPECIFIC ID FIELDS**

| Byte # | Field size | Notes                     | Value |
| ------ | ---------- | -----                     | ----- |
| 96 – 127  |32 | Vendor specific data
| 128 – 255 |   | Reserved

**ENHANCED FEATURE SET MEMORY**

| Byte # | Field size | Notes                     | Value |
| ------ | ---------- | -----                     | ----- |
| 256 – 257 | 2  | Temp H Alarm       | Signed twos complement integer in increments of 1/256 °C
| 258 – 259 | 2  | Temp L Alarm       | Signed twos complement integer in increments of 1/256 °C
| 260 – 261 | 2  | Temp H Warning     | Signed twos complement integer in increments of 1/256 °C
| 262 – 263 | 2  | Temp L Warning     | Signed twos complement integer in increments of 1/256 °C
| 264 – 265 | 2  | VCC H Alarm        | Supply voltage decoded as unsigned integer in increments of 100 μV
| 266 – 267 | 2  | VCC L Alarm        | Supply voltage decoded as unsigned integer in increments of 100 μV
| 268 – 269 | 2  | VCC H Warning      | Supply voltage decoded as unsigned integer in increments of 100 μV
| 270 – 271 | 2  | VCC L Warning      | Supply voltage decoded as unsigned integer in increments of 100 μV
| 272 – 273 | 2  | Tx Bias H Alarm    | Laser bias current decoded as unsigned integer in increment of 2 μA
| 274 – 275 | 2  | Tx Bias L Alarm    | Laser bias current decoded as unsigned integer in increment of 2 μA
| 276 – 277 | 2  | Tx Bias H Warning  | Laser bias current decoded as unsigned integer in increment of 2 μA
| 278 – 279 | 2  | Tx Bias L Warning  | Laser bias current decoded as unsigned integer in increment of 2 μA
| 280 – 281 | 2  | Tx Power H Alarm   | Transmitter average optical power decoded as unsigned integer in increments of 0.1 μW
| 282 – 283 | 2  | Tx Power L Alarm   | Transmitter average optical power decoded as unsigned integer in increments of 0.1 μW
| 284 – 285 | 2  | Tx Power H Warning | Transmitter average optical power decoded as unsigned integer in increments of 0.1 μW
| 286 – 287 | 2  | Tx Power L Warning | Transmitter average optical power decoded as unsigned integer in increments of 0.1 μW
| 288 – 289 | 2  | Rx Power H Alarm   | Receiver average optical power decoded as unsigned integer in increments of 0.1 μW
| 290 – 291 | 2  | Rx Power L Alarm   | Receiver average optical power decoded as unsigned integer in increments of 0.1 μW
| 292 – 293 | 2  | Rx Power H Warning | Receiver average optical power decoded as unsigned integer in increments of 0.1 μW
| 294 – 295 | 2  | Rx Power L Warning | Receiver average optical power decoded as unsigned integer in increments of 0.1 μW
| 296 – 311 | 16 |  Reserved
| 312 – 350 | | External Calibration Constants
| 351 | 1 | Checksum for Bytes 256 – 350
| 352 – 353 | 2 | Real Time Temperature              | Signed twos complement integer in increments of 1/256 °C
| 354 – 355 | 2 | Real Time VCC Power Supply Voltage | Supply voltage decoded as unsigned integer in increments of 100 μV
| 356 – 357 | 2 | Real Time Tx Bias Current          | Laser bias current decoded as unsigned integer in increment of 2 μA
| 358 – 359 | 2 | Real Time Tx Power                 | Transmitter average optical power decoded as unsigned integer in increments of 0.1 μW
| 360 – 361 | 2 | Real Time Rx Power                 | Receiver average optical power decoded as unsigned integer in increments of 0.1 μW 
| 362 – 365 | 4 | Reserved
| 366 | 1 | Status/Control                          | bit 7: TX_DISABLE State
|     |   |                                         | bit 6 – 3: Reserved
|     |   |                                         | bit 2: TX_FAULT State
|     |   |                                         | bit 1: RX_LOS State
|     |   |                                         | bit 0: Data Ready (Bar)
| 367 | 1 | Reserved                         
| 368 | 1 | Alarm Flags                             | bit 7: Temp High Alarm
|     |    |                                        | bit 6: Temp Low Alarm
|     |    |                                        | bit 5: VCC High Alarm
|     |    |                                        | bit 4: VCC Low Alarm
|     |    |                                        | bit 3: Tx Bias High Alarm
|     |    |                                        | bit 2: Tx Bias Low Alarm
|     |    |                                        | bit 1: Tx Power High Alarm
|     |    |                                        | bit 0: Tx Power Low Alarm
| 369 |  1 | Alarm Flags cont.                      | bit 7: Rx Power High Alarm
|     |    |                                        | bit 6: Rx Power Low Alarm
|     |    |                                        | bit 5 – 0: Reserved
370 – 371| 2 | Reserved
372   |  1 | Warning Flags                          | bit 7: Temp High Warning
|     |    |                                        | bit 6: Temp Low Warning
|     |    |                                        | bit 5: VCC High Warning
|     |    |                                        | bit 4: VCC Low Warning
|     |    |                                        | bit 3: Tx Bias High Warning
|     |    |                                        | bit 2: Tx Bias Low Warning
|     |    |                                        | bit 1: Tx Power High Warning
|     |    |                                        | bit 0: Tx Power Low Warning
373   | 1  | Warning Flags cont.                    | bit 7: Rx Power High Warning
|     |    |                                        | bit 6: Rx Power Low Warning
|     |    |                                        | bit 5 – 0: Reserved
|374 – 511 |                                        | Reserved/Vendor Specific




### Hardware Configuration Summary


|                | VME-EVR-300 | mTCA-EVR-300 | PCIe-EVR-300DC |
| -------------- | ----------- | ------------ | -------------- |
| Pulse Generators | 24 |16 |16
| FP TTL inputs  | 2  | 2 | 0
| FP TTL outputs | 0  | 4 | 0
| FP GTX outputs | 4{sup}`1` | 0 | 0
| FP UNIV I/O / slots | 4 | 0 | 16 / 8{sup}`2`
| FP UNIV GPIO pins / slots 16/4 0 / 0 0 / 0
| TB Outputs     |  16 | 32 | 0
| TB Inputs      | 16  | 32 | 0
| Prescalers     |8 x 32 bit | 8 x 32 bit | 8 x 32 bit |


Pulse Generator: Prescaler, Delay, Pulse Width Range (bits)
|                | VME-EVR-300 | mTCA-EVR-300 | PCIe-EVR-300DC |
| -------------- | ----------- | ------------ | -------------- |
|    0           | 16, 32, 32  | 16, 32, 32   | 16, 32, 32     |   
|    1           | 16, 32, 32  | 16, 32, 32   | 16, 32, 32     |   
|    2           | 16, 32, 32  | 16, 32, 32   | 16, 32, 32     |   
|    3           | 16, 32, 32  | 16, 32, 32   | 16, 32, 32     |   
|    4           | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    5           | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    6           | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    7           | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    8           | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    9           | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    10          | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    11          | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    12          | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    13          | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    14          | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |   
|    15          | 0, 32, 16   | 0, 32, 16    | 0, 32, 16      |

(^1) One Universal I/O slot (2 outputs), 2 x CML output
(^2) Universal I/O is available on the external I/O box





### PCIe-EVR-300DC and IFB-300 Connections

Due to its small bracket the PCIe-EVR-300DC has only a SFP transceiver and a micro-SCSI type con-
nector to interface to the IFB-300. The cable between the PCIe-EVR-300DC and IFB-300 should be 
connected/disconnected only when powered down.


Connector / Led Style Level Description
Link TX (SFP) LC Optical 850 nm Event link Transmit
Green: TX enable
Red: Fract.syn. not locked
Blue: Event out
Link RX (SFP)
Next to micro-SCSI


LC Optical 850 nm Event link Receiver
Green: link up
Red: link violation detected
Blue: event led

The interface board IFB-300 has eight Universal I/O slots which can be populated with various types of
Universal I/O modules. If an input module is populated in any slot a jumper has to be mounted in that
slot’s two pin header with marking “Insert jumper for input module”. Please note that if an input module
is mounted the corresponding Universal Output Mapping has to be tri-stated. Refer to Table 1: Signal
mapping IDs for details.

Universal Slot 0/1 signals are hard-wired to the TTLIN 0/1 signals.


Figure 22: IFB-300 Front Panel


Connector / Led Style Level Description
UNIV0/1 Universal slot TTL Input / Universal I/O 0/1
UNIV2/3 Universal slot Universal I/O 2/3
UNIV4/5 Universal slot Universal I/O 4/5
UNIV6/7 Universal slot Universal I/O 6/7
UNIV8/9 Universal slot Universal I/O 8/9
UNIV10/11 Universal slot Universal I/O 10/11
UNIV12/13 Universal slot Universal I/O 12/13
UNIV14/15 Universal slot Universal I/O 14/15
LINK Green led RX link up
EVIN Yellow led RX event in
EVOUT Yellow led RX event led (mapped)
RXFAIL Red led RX violation detected

### mTCA-EVR-300 Connections


Figure 23: mTCA-EVR-300 Front Panel


Connector / Led Style Level Description
USB Micro-USB MMC diagnostics serial port / JTAG interface
Link TX (SFP) LC Optical 850 nm Event link Transmit
Green: TX enable
Red: Fract.syn. not locked
Blue: Event out
Link RX (SFP) LC Optical 850 nm Event link Receiver
Green: link up
Red: link violation detected
Blue: event led
IFB VHDCI LVDS IFB-300 Interface Box connection
IN0 LEMO TTL FPTTL0 Trigger input
IN1 LEMO TTL (3.3V / 5V) FPTTL1 Trigger input
OUT0 LEMO 3.3V LVTTL TTL Front panel output 0
OUT1 LEMO 3.3V LVTTL TTL Front panel output 1
OUT2 LEMO 3.3V LVTTL TTL Front panel output 2
OUT3 LEMO 3.3V LVTTL TTL Front panel output 3
TCLKA mTCA.4 LVDS TCLKA clock on backplane
This signal is driven by CML/GTX logic block 0
Mapped as Universal Output 16
TCLKB mTCA.4 LVDS TCLKB clock on backplane
This signal is driven by CML/GTX logic block 1
Mapped as Universal Output 17
RX17 mTCA.4 MLVDS Backplane output 0
TX17 mTCA.4 MLVDS Backplane output 1
RX18 mTCA.4 MLVDS Backplane output 2
TX18 mTCA.4 MLVDS Backplane output 3
RX19 mTCA.4 MLVDS Backplane output 4
TX19 mTCA.4 MLVDS Backplane output 5
RX20 mTCA.4 MLVDS Backplane output 6
TX20 mTCA.4 MLVDS Backplane output 7

### PCIe-EVR-300DC Firmware Upgrade

The PCIe-EVR-300DC firmware image can be upgraded with the following command after loading the
driver in Linux:

dd if=new_image.bit of=/dev/era1

A power cycle is required to load the new configuration image on the PCIe-EVR-300DC.