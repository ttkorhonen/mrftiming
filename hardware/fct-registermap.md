# FCT Function Register Map

The EVM module can be configured for use as an Event Generator (EVG) or a fanout/concentrator.

This is the register map when EVM is configured as a fanout/concentrator.

| Address         | Register     | Type   |  Description |
| -------         | -----------  | ------ | ------------ |
| 0x000           | Status       | UINT32 | [Status Register](#status-register)
| 0x004           | Control      | UINT32 | [Control Register](#control-register)
| 0x010           | UpDCValue    | UINT32 | Upstream Data Compensation Delay Value
| 0x014           | FIFODCValue  | UINT32 | Receive FIFO Data Compensation Delay Value
| 0x018           | IntDCValue   | UINT32 | FCT Internal Datapath Data Compensation Delay Value
| 0x02C           | TopologyID   | UINT32 | Timing Node Topology ID
| 0x040           | Port1DCValue | UINT32 | Port 1 loop delay value
| 0x044           | Port2DCValue | UINT32 | Port 2 loop delay value
| 0x048           | Port3DCValue | UINT32 | Port 3 loop delay value
| 0x04C           | Port4DCValue | UINT32 | Port 4 loop delay value
| 0x050           | Port5DCValue | UINT32 | Port 5 loop delay value
| 0x054           | Port6DCValue | UINT32 | Port 6 loop delay value
| 0x058           | Port7DCValue | UINT32 | Port 6 loop delay value
| 0x05C           | Port8DCValue | UINT32 | Port 8 loop delay value
| 0x1000 – 0x10FF | SFP1EEPROM   |        | Port 1 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1100 – 0x11FF | SFP1DIAG     |        | Port 1 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1200 – 0x12FF | SFP2EEPROM   |        | Port 2 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1300 – 0x13FF | SFP2DIAG     |        | Port 2 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1400 – 0x14FF | SFP3EEPROM   |        | Port 3 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1500 – 0x15FF | SFP3DIAG     |        | Port 3 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1600 – 0x16FF | SFP4EEPROM   |        | Port 4 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1700 – 0x17FF | SFP4DIAG     |        | Port 4 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1800 – 0x18FF | SFP5EEPROM   |        | Port 5 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1900 – 0x19FF | SFP5DIAG     |        | Port 5 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1A00 – 0x1AFF | SFP6EEPROM   |        | Port 6 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1B00 – 0x1BFF | SFP6DIAG     |        | Port 6 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1C00 – 0x1CFF | SFP7EEPROM   |        | Port 7 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1D00 – 0x1DFF | SFP7DIAG     |        | Port 7 SFP Transceiver diagnostics (SFP address 0xA2)
| 0x1E00 – 0x1EFF | SFP8EEPROM   |        | Port 8 SFP Transceiver EEPROM contents (SFP address 0xA0)
| 0x1F00 – 0x1FFF | SFP8DIAG     |        | Port 8 SFP Transceiver diagnostics (SFP address 0xA2)

Some information about the transceiver EEPROM contents can be found in [this document](https://www.coherent.com/resources/application-note/networking/ddmi-for-sfp-and-sfp-plus-an-2030.pdf).

## Status Register


| address | bit 23 | bit 22 | bit 21 | bit 20 | bit 19 | bit 18 | bit 17 | bit 16 |
| ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 0x001   | LINK8  | LINK7  | LINK6  | LINK5  | LINK4  | LINK3  | LINK2  | LINK1  |
|         | bit 7  | bit 6  | bit 5  | bit 4  | bit 3  | bit 2  | bit 1  | bit 0  |
| 0x003   | VIO8   | VIO7   | VIO6   | VIO5   | VIO4   | VIO3   | VIO2   | VIO1   |
 
| Bit   | Function | 
| ---   | -------- |
| LINK8 | Port8 RXStatus, 1–link up, 0–link down | 
| LINK7 | Port7 RXStatus, 1–link up, 0–link down | 
| LINK6 | Port6 RXStatus, 1–link up, 0–link down | 
| LINK5 | Port5 RXStatus, 1–link up, 0–link down | 
| LINK4 | Port4 RXStatus, 1–link up, 0–link down | 
| LINK3 | Port3 RXStatus, 1–link up, 0–link down | 
| LINK2 | Port2 RXStatus, 1–link up, 0–link down | 
| LINK1 | Port1 RXStatus, 1–link up, 0–link down | 
| VIO8  | Port 8 RX Violation |
| VIO7  | Port 7 RX Violation |
| VIO6  | Port 6 RX Violation |
| VIO5  | Port 5 RX Violation |
| VIO4  | Port 4 RX Violation |
| VIO3  | Port 3 RX Violation |
| VIO2  | Port 2 RX Violation |
| VIO1  | Port 1 RX Violation |

## Control Register

| address | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
| ------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| 0x007   | CLRV8 | CLRV7 | CLRV6 | CLRV5 | CLRV4 | CLRV3 | CLRV2 | CLRV1 |


| Bit   | Function |
| ----- | -------- |  
| CLRV8 | Clear RX Violation Port 8 |
| CLRV7 | Clear RX Violation Port 7 |
| CLRV6 | Clear RX Violation Port 6 |
| CLRV5 | Clear RX Violation Port 5 |
| CLRV4 | Clear RX Violation Port 4 |
| CLRV3 | Clear RX Violation Port 3 |
| CLRV2 | Clear RX Violation Port 2 |
| CLRV1 | Clear RX Violation Port 1 |


 
 
 
 
 
 
 
