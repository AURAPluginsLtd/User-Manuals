---
question: "Why Editor fails to connect with the hardware?"
department: "Troubleshooting"
source_url: "https://auraplugins.com/kb/faq/why-editor-fails-to-connect-with-the-hardware/"
---
# Why Editor fails to connect with the hardware?

There are a few reasons why this could happen, so let’s make sure everything is right:

1. MIDI out from your hardware is connected to your MIDI interface input.
2. MIDI out from your MIDI interface is connected to your hardware input.
3. Hardware has Global MIDI Channel set as instructed.
4. Hardware has Device ID set as instructed.
5. Hardware is in Performance / Multi mode (mono timbral and FX Editors excluded).

If all of these conditions are right and the Editor still fails, check the MIDI interface specs to ensure it can handle large SysEx packages which the Editor & Hardware uses to send program data back and forth.

You can open a ticket with our Support Team if you’re stuck.
