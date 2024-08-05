---
orphan: true
---

# Property descriptions

## Global

```{glossary}
PLL Lock Status
    This indicates whether the phase locked loop which synchronizes an EVR's local oscillator with the phase of the EVG's oscillator. 
    Outputs will not be stable unless the PLL is locked.
    Except for immediately (≪ 1sec) after a change to the fractional synthesizer this property should always read as true (locked). Reading false for longer then one second is likely an indication that the fractional synthesize is misconfigured, or that a hardware fault has occured.

Link Status
     Indicates when the event link is active. This means that the receiver sees light, and that valid data is being decoded.
     A reading of false may be caused by a number of conditions including: EVG down, fiber unplugged or broken, and/or incorrent fractional synthesizer fre- quency.

Timestamp Valid
    Indicates if the EVR has a current, valid timestamp. Condition under which the timestamp is declared invalid include:
        • TS counter reset event received, but "seconds" value not updated.
        • Found timestamp with previous invalid value. Catches old timestamp in buffers.
        • TS counter exceeded limit (eg. missed reset event)
        • New "seconds" value is less then the last valid values, or more then two greater then the last valid value. (Light Source time model only). This will reject single "bad" values sent by the EVG.
        • Event Link error (Status is error).
    The timestamp will become valid when a new "seconds" value is received from the EVG.

Model
    The hardware model number.

Version
    The firmware version.

FIFO Overflow counter
    Counter the number of hardware event buffer overflows. There is a single hard- ware buffer for all event codes. When it overflows arbitrary events will fail to be delivered to software. This can cause the timestamp to falsely be invalidated, and can disrupt database processing which depends on event reception.
    This is a serious error which should be corrected. Note: An overflow does not effect physical output.

FIFO Over rate
    Counts overflows in all of the per event software buffers.
    This indicates that the period between successive events is shorter then the runtime of the code (callbacks, and database processing) that is causes. Extra events are being dropped and cause no action.
    Actions of other event codes are not effected.

Clock
    Frequency of an EVR's local oscillator. This must be close enough to the EVG master oscillator to allow the phase locked loop in the EVR to lock.
    The native analog units are Hertz (Hz). This can be changed with the LINR and ESLO fields. Use ESLO of 1e-6 to allow user setting/reading in MHz.

Timestamp Source
    Determines what causes the timestamp event counter to tick. There are three possible values.
    Event clock Use an integer divisor of the EVR's local oscillator.
    Mapped code(s) Increments the counter whenever certain events arrive. These codes can be defined using special mapping records.
    DBus 4 Increments on the 0->1 transition of DBus bit #4.

Timestamp Clock
    Specifies the rate at which the timestamp event counter will be incremented. This determines the resolution of all timestamps.
    This setting is used in conjunction with the 'Timestamp Source'.
    When the timestamp source is set to "Event clock" this property is used to compute an integer divider from the EVR's local oscillator frequency to the given frequency. Since this may not be exact it is recommended to read back the actual divider setting via the "Timestamp Prescaler" property.
    In all modes this value is stored in memory and used to convert the timestamp event counter values from ticks to seconds.
    By default the analog units are Hertz (Hz). This can be changed with the LINR and ESLO fields. Use ESLO of 1e-6 to allow user setting/reading in MHz.

Timestamp Prescaler
    When using the "Event clock" timestamp source this will return the actual divisor used. In other modes it reads 0.

Timestamp
    When processed creates a human readable string with either the current event link time, or the event link time when code # was last received.

Event Clock TS Div
    This is an approximate divider from the event link frequency down to 1MHz. It is used to determine the heartbeat timeout.

Receive Error Count
    The number of event link errors which have occurred.
```

## Pulse Generator

Properties in this section apply to the Pulse Generator (Pulser) sub-unit. Records accessing properties in this section will have DTYP set to "EVR Pulser". See: evrApp/Db/evrpulser.db
:::{glossary}
Enable
   When not set, the output of the Pulse Generator will remain in its inactive state (normally low). The generator must be enabled before mapped actions will have any effect.

Polarity
   Reverses the output polarity. When set, changes the Pulse Generator's output from normally low to normally high.

Prescaler
   Decreases the resolution of both delay and width by an integer multiple. De- termines the tick rate of the internal counters used for delay and width with respect to the EVR's local oscillator.

Delay
   Determines the time between when the Pulse Generator is triggered and when it changes state from inactive to active (normally low to high).
   This can be given in integer ticks, or floating point seconds. This can be changed with the LINR and ESLO fields. Use ESLO of 1e6 to allow user setting/reading in microseconds.

Width
   Determines the time between when the Pulse Generator changes state from inactive to active (normally low to high), and when it changes back to inactive.
   This can be given in integer ticks, or floating point seconds. This can be changed with the LINR and ESLO fields. Use ESLO of 1e6 to allow user setting/reading in microseconds.
:::

## Prescaler (Clock Divider)
Properties in this section apply to the Prescaler sub-unit.
Records accessing properties in this section will have DTYP set to "EVR Prescaler". See: evrApp/Db/evrscale.db

Divide
implemented for: longout, ao, longin
Sets the integer divisor between the Event Clock and the sub-unit output.
By default the analog units are Hertz (Hz). This can be changed with the LINR and ESLO fields. Use ESLO of 1e-6 to allow user setting/reading in MHz.
:::