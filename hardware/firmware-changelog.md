## EVM Firmware Version Change Log

| FW Version | Date | Changes | Affected HW |
| ---------- | ---- | ------- | ------------|
| 0200 | 11.06.2015 | - Prototype release | VME-EVM-300
| 0201 | 24.09.2015 | - Added segmented data buffer | VME-EVM-300
|      |            |   Fixed Port 1 TX polarity 
| 010202 | 01.10.2015 | - Changed receive FIFO delay target to 00060000 | VME-EVM-300
|        |            |   Added LED test mode (production testing)
|        |            |   Removed test signals from TBOUT
| 010203 | 23.11.2015 | - Added changes for running with a slower clock on fan-out. | VME-EVM-300
| 020203 | 18.12.2015 | - Changes to data buffer forwarding | VME-EVM-300
| | |     Changes for rate conversion forwarding, using internal div/2.
| 0204   | 12.01.2016 | - /2 rate conversion working on events, dbuf and dbits. | VME-EVM-300
| | |     Improvements to delay measurement system.
| 0205   | 13.04.2016 | - Moved delay compensation segment from segment 0 to | VME-EVM-300
| | |     last segment in memory.
| | |     Fixed front panel TTL input order.
| | |     Fixed race condition in segmented memory buffer trans-
| | |     mission that caused dropped software buffers.
| FB0206 | 23.12.2016 | - Added upstream and downstream event receivers. |  VME-EVM-300
| | |     Changed beacon event from 0x7A to 0x7E.
| | |     Added topology ID
| | |     Added delay measurement validity information to delay VME-EVM-300
| | |     compensation data
| 000207 | 19.01.2017 | - Added front panel input phase monitoring and phase | VME-EVM-300
| | | select features.
| | | Added external AC input synhronisation features.
| 010207 | 09.02.2017 | - Fixed occasional dropped out downstream and upstream VME-EVM-300
data buffers/segmented data buffers.
| 030207 | 03.05.2017 | - Added RF input monitoring logic to automatically recover |   VME-EVM-300
| | |      from lost RF signal.
| | |     Added a way to toggle distributed bus transmission
| | |     phase when an external AC synchronisation clock is used.
| 040207 | 23.05.2017 | - Fixed readout of diagnostics information on single | VME-EVM-300
| | | mode transceivers.
| 050207 | 26.06.2017 | - Fixed transceiver_channel to turn off receiver on first | VME-EVM-300
| | | error to prevent propagation of errors up stream. |
| 070207 | 04.05.2020 | - Changed VME CSR registers to readback unused bits as zero. | VME-EVM-300
| | | - Fixed bus error on write to fct registers |
| | | - Added external reset for MXC |

### mTCA.4 development branch

| 070207 | 31.01.2019 | - Moved MIRQ to 0x1C register. Moved DCDataBuf-Control from 0x1c to 0x30. | mTCA-EVM-300
| 0A0207 | 15.11.2019 | - Fixed RX polarity of mTCA-EVM-300 ports 6 and 7. | mTCA-EVM-300
| | | - Defaults for fan-out.|
| | | - Added support for mTCA backplane I/O on trigger bus. |
| 0B0207 | 15.11.2019 | - Fixed EVRU/D to EVG signal and added pullup to MOD_SDA. | mTCA-EVM-300
| 0C0207 | 02.04.2020 | - Added settings files. | mTCA-EVM-300
| | | - Changed event clock contraint to 6 ns.|


### Merging of VME and mTCA.4 development branches

| 0C0207 | 11.09.2020 | - Merge VME tested successfully. | VME-EVM-300
| 0E0207 | 24.02.2021 | - Merge mTCA.4 tested successfully. | mTCA-EVM-300
