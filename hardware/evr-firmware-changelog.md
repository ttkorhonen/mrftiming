## EVR Firmware Version Change Log


| FW Version | Date          | Changes                                                                   | Affected HW |
| ---------- | ----          | -------                                                                   | ----------- |
| 0200       | 11.06.2015    | - Prototype release                                                       | VME-EVR-300
| 0201       | 24.09.2015    | - Added segmented data buffer block status flags
|            |               | - Changed delay compensation FIFO depth from 2k to 4k event cycles
|            |               | - Added DCM modulation to improve jitter performance
| 0203       | 12.01.2016    | - Delay compensation amendments, non-GTX outputs are compensated properly |  VME-EVR-300
| 0204       | 25.01.2016    | - First release for PCIe-EVR-300DC                                        | all
|            |               | - Fixed segmented data buffer flag writes
| 0204       | 03.02.2016    | - Fixed initial values of GTX outputs                                     | VME-EVR-300
|            |               | - GTX output aligment
| 0205       | 07.04.2016    | - Changed PCIe-EVR-300DC class code to 0x118000.                          | all
|            |               |- Moved delay compensation data from first segment to last segment.
|            |               |- Fixed dual output mapping for transition board outputs.
|            |               |- Added backplane signals to mTCA-EVR.
|            |               |- Added delay compensation disabled mode to be able to use DC capable EVRs with pre-DC EVG and fan-outs.
| 0206       | 12.08.2016    | - Relocated segmented data buffer to new address location.                | all
|            |               |- Replaced earlier data buffer in its original position (maintaining compatibility with 230 series protocol).
|            |               |- Changed segmented data buffer protocol to use K28.2 as a start symbol
| 0207       | 30.08.2016    | - Added stand-alone capability: using its internal reference              | all
|            |               | the EVR can now operate as a stand-alone pulse generator without event link.
|            |               |- EVR can operate as a simple EVG by forwarding internal events
|            |               |- Added software event capability
|            |               |- Added one EVG type sequencer
| 030207     |  23.12.2016 | - Changed beacon event code from 0x7a to 0x7e.                              | all 
|            |               |- Added status bits for delay compensation path delay value validity.
|            |               |- Added register for topology ID.
| 040207     |  09.1.2017  |  - Repaired “trigger allways” problem with triggering sequencer with pulse generator 19. | all
|            |             |- Added mapping 61 for sequencer software triggering.
| 050207     | 19.1.2017   | - Fixed running on internal reference for VME-EVR-300.VME-EVR-300
| 060207     | 9.2.2017    | - Added configurability to handling a lost event clock:                                  |  VME-EVR-300
|            |               |  continue, stop, fallback to reference clock.
|            |               | - Further fix to running on internal reference for VME-EVR-300.
| 070207     | 6.4.2017    | - Fixed CML/GTX operation in stand-alone mode without receiver event stream.             | mTCA-EVR-300
|            |               |- Fixed mapping of TCLKA/TCLKB backplane clocks on mTCA-EVR-300.
| 080207     | 7.8.2017    | - PCIe AXI to OPB bridge fix for overloapping read/write                                 | PCIe-EVR-300DC
|            |               | operation during block transfers.
|            |               | - Added pullup to MODU_SDA and MODU_DEF0.
| 090207     | 27.2.2018   |  - Changes to get design built on Vivado 2017.4                                          | All
| 0A0207     | 18.9.2018   |  - Changed number of external inputs to 16.                                              | PCIe-EVR-300DC
| 0D0207     | 20.5.2019   |  - Added programmable phase shift to prescalers.                                         | mTCA-EVR-300
| 0E0207     | 2.7.2019    | - Fix to event FIFO.                                                                     | mTCA-EVR-300
|      |                   |- Added flip-flop outputs.
| 0F0207     | 3.3.2020    | - Added support for RTM on mTCA-EVR-300..                                                | mTCA-EVR-300
| 100207     | 9.4.2021    | - Allow disabling receive databuf mode.                                                  | mTCA-EVR-300
| 110207     | 2.6.2021    | - Added support for mTCA-EVR-300RF                                                       | mTCA-EVR-300RF
| 130207     | 14.2.2022    | - 32 bit pulse width for HW mask pulse generators                                       | VME-EVR-300
| 140207     | 11.5.2022    | - Added pulse generator masking capability for HW set and reset                         | mTCA-EVR-300DC
| 150207     | 15.6.2022    | - Added VME-UTB-64x support for VME-EVR-300.                                            | VME-EVR-300
| 160207     | 6.10.2022    | - Changed pulse with and delay to 32 bits on all pulse generators..                     | mTCA-EVR-300DC and VME-EVR-300
| 170207     | 6.10.2022    | -  Use LOS from SFP transceiver to reset receiver..                                     | mTCA-EVR-300DC
| 180207     | 17.01.2023    | -Added support for new mTCA-EVR-300DC hardware with improved backplane triggers.       | mTCA-EVR-300DC
| 190207     | 27.05.2023    | - Added support pulse trains for pulse generators.                                     | mTCA-EVR-300DC
| 200207     | 26.06.2023    | - Fixed pulse trains issues with single width pulses.                                  | mTCA-EVR-300DC
