# Introduction

**NOTE**: Video link to setup Virus TI USB Audio with macOS available at the end of this User Guide!

## Access Virus TI USB Audio with macOS 10.12 and greater – Is it going to work?

**Yes**. We were been able to get **all** Virus TI USB Audio channels to work inside our DAW – NATIVELY. We are running **macOS 12.7.6 Monterey with M1 powered MacBook Pro**. As a long time Logic Pro user, it was just an experimental idea to check “what if…” and boom! It worked! Note that Logic Pro is NOT required, this works with every macOS out of the box – natively! You can optionally use Audiomovers [Omnibus](https://audiomovers.com/products/omnibus) and/or [Inject](https://audiomovers.com/products/inject) to route audio from the Virus to your DAW.

OK, let’s get into it. What do you need?

- Access Virus TI and/or Access Virus TI Snow (obviously)….
- USB cable.
- USB-C to USB 2 or USB 3 Hub.
- Access Virus Editor.

Install our Access Virus Editor from the [downloads](https://auraplugins.com/downloads/access-virus-editor/) page. Demo works too, but you are missing a lot features with it ($69.95 is a very small fee for a fully working editor)!

### Step 1

Turn off power from your Virus TI. UNINSTALL Access Virus Control software, if you have it installed on your computer. Once your computer has rebooted, open new Finder window and navigate to:

```
/Library/Audio/MIDI Drivers/
```

check and make sure *Virus TI MIDI Driver.plugin* is **removed**.

Next navigate to:

```
/Library/Extensions/
```

check and make sure *AccessVirusTI.kext* is **removed**.

If either one of the files are present in your system, the Editor and MIDI won’t work as expected. You can manually remove the files by selecting the correct file name and click cmd + backspace.

### Step 2

Unplug USB and MIDI cables from your Virus TI.

Install our Access Virus Editor with all Editor formats enabled even if you are not using them (VST2, VST3, Audio Unit, AAX). This ensures the Editor and all the drivers are installed properly. Once installer is completed, navigate to:

```
/Library/Audio/MIDI Drivers/
```

check and make sure that *AURA Plugins Virus TI USB Midi.plugin* is **installed** – if not, run the installer again!

### Step 3

Reboot your computer. Power up your Virus TI and wait until it is booted. Plug in the USB cable. Virus TI display will say “Audio clock changed” and “USB” text will appear in the top right corner.

**NOTE**: Read our Access Virus User Manual article about USB & MIDI connections here: [../user-manual/06-prepare-your-hardware.md](../user-manual/06-prepare-your-hardware.md)
