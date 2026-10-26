# Roland JP-80×0 Editor – Configure JP-8080

![Configure Roland JP-8080 - Edit Function Buttons](images/configure-roland-jp-8080-edit-function-buttons.jpg)

*Figure: Configure Roland JP-8080 - Edit Function Buttons*

## Click EDIT and choose MIDI (button 5) and apply these settings:

```
Tx/Rx Edit SW    = ON
Tx/Rx Edit Mode  = MODE1
Tx/Rx ProgChg SW = BANK SEL + PC
Local Switch     = Up to your desire. OFF means extra MIDI traffic back to JP!
MIDI Sync        = If on, hardware will sync to MIDI clock from MIDI.
Device ID        = 17 (for multiple JP’s in setup, choose individual ID for each).
Rx Exclusive SW  = ON
Perform Ctrl CH  = 3
Remote KBD CH    = 16
MIDI Thru        = OFF
```

## Next click PART (button 3) and apply these settings:

```
MIDI CH (LOWER)  = 1
MIDI CH (UPPER)  = 2
```

All set! We are now ready to open our plug-in in DAW or Standalone Application!

To get more information about how to adjust your synth, read the Roland JP-8000 / JP-8080 User Manual.

> **NOTE:** Arpeggiator will not play unless your DAW is able to provide a MIDI Clock. Windows: Check our method of using MIDI OX and LoopBe together to provide MIDI clock from DAW to your synth.

> **NOTE:** The only way to trigger arpeggiator with JP-8080 is to add a second MIDI cable from the MIDI splitter device or MIDI interface to the KBD Input port. Hardware control happens via regular MIDI port while arpeggio can be triggered with notes via KBD input port.
