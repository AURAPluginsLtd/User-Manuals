# Roland JP-80×0 Editor – Configure Standalone APP

If DAW is not your thing and you just want to edit JP right from your computer, you can use the standalone application. Below is a guide to connect the Editor to the JP and do all the fun stuff DAW users do (without automation).

## Select MIDI ports with Standalone Application

If you use the Standalone Application, click “ **Roland JP-80x0 Editor [1]** ” from the top bar and choose **Preferences [2]** . This will open **Preferences dialog [3]** where you can set **MIDI Input Device** and **MIDI Output Device** .

On Windows machines, the same dialog can be opened from the File menu.

![JP-80x0 Editor User Manual – Setting MIDI Ports](images/jp-80x0-editor-user-manual-setting-midi-ports.jpg)

*Figure: JP-80x0 Editor User Manual – Setting MIDI Ports*

## Remote Keyboard MIDI Input

If you have an external MIDI controller you want to use with the Editor to trigger notes and tweak knobs with, you can select **MIDI IN** from the Editor top bar. This port won’t work with the synth itself and is only used for triggering MIDI events.

![Remote Keyboard Input available in Standalone App only!](images/remote-keyboard-input-available-in-standalone-app-only.jpg)

*Figure: Remote Keyboard Input available in Standalone App only!*

> **NOTE:** Audio Device Settings in the preferences dialog does not have capability to transmit audio in this stage. Choose Audio Drivers, but keep in mind that audio has to go through Audio Jacks to console or sound card inputs.

## Hardware Check / Ping

After setting MIDI OUT, our Editor will start scanning for the hardware. If there is no immediate response, the Editor will attempt 3 more times. If there is no response, you might get a “ **Connection Timed Out** ” message. If so, double check your hardware settings and make sure your cables are good!

> **NOTE:** MIDI ports for plug-in are set from the main window while Standalone Application MIDI ports are set from the Editor Preferences.

Editor **Control Display** will say “ **Editor is ready to go!** ” when response is received from the JP.

![JP-80x0 Editor User Manual – Ready to go!](images/jp-80x0-editor-user-manual-ready-to-go.jpg)

*Figure: JP-80x0 Editor User Manual – Ready to go!*

You can optionally enable Device ID probing function, which will check for the Device ID for you. This is good IF you have only one JP model in your setup. Function can be enabled from **Utilities [1]** menu -> **Editor Preferences [2]** -> **Enable DeviceID Scanning [3]** .

![JP-80x0 Editor User Manual – DeviceID Scanning](images/jp-80x0-editor-user-manual-deviceid-scanning.jpg)

*Figure: JP-80x0 Editor User Manual – DeviceID Scanning*

Check Main Functions and Librarian guides to learn more about the Editor usage.

> **NOTE:** If you have Device ID set to 17 on the JP and 17 on the Editor, our Editor will find and establish connection to your JP if everything else is configured properly.
