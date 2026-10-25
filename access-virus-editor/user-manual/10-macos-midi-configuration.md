# Access Virus Editor – macOS MIDI Configuration

This setup **is not mandatory if you remember** all of your port numbers & routings out of your head. This guide will help you, if your setup is anything like ours: dozens and dozens of ports in use!

## Virus TI and USB on macOS

If you are using USB with Virus TI, check the previous article here: https://auraplugins.com/kb/article/access-virus-editor-virus-ti-usb-audio-with-macos/

**HEADS UP :** This is usually the step which is skipped and then you get connection timed out errors and such. Read the guide, it will help you to succeed with the setup in the long run!

## Audio MIDI Setup.app

Start by opening **Audio MIDI Setup.app [1]** – You can find the app from `/Applications/Utilities`

![Open Audio MIDI Setup app](images/open-audio-midi-setup-app.jpg)

*Figure: Open Audio MIDI Setup app*

Next we want to view MIDI devices and to do that, click **Window [1]** and select **Show MIDI-Studio [2]**

![Open MIDI-Studio](images/open-midi-studio.jpg)

*Figure: Open MIDI-Studio*

And this is what you get (contents of the window will vary depending what your setup has configured already!):

![macos midi configuration start](images/macos-midi-configuration-start.jpg)

*Figure: macos midi configuration start*

## Creating new Devices

If you haven’t added the Virus to your MIDI-studio yet, here is how to do it:

**Click + -sign [1]** from the top right corner (add external midi-device)

![macos midi configuration new device](images/macos-midi-configuration-new-device.jpg)

*Figure: macos midi configuration new device*

The newly added device will pop somewhere in the window (without any logical placement!)

![macos midi configuration device created](images/macos-midi-configuration-device-created.jpg)

*Figure: macos midi configuration device created*

Double click the newly added **device [1]** so we can start to modify its properties

![macos midi configuration open device](images/macos-midi-configuration-open-device.jpg)

*Figure: macos midi configuration open device*

In this example, I am gonna add a Virus Rack (classic 1U rack unit) to my rig. Lets update the properties:

- **Device Name [1]** = Virus Rack
- **Manufacturer [2]** = Access
- **Model [3]** = Virus Rack
- **Check MIDI clock [4]** if you want your Virus model to receive MIDI clock information. Some DAWs require additional steps to transmit the MIDI clock.

You can update the **device color [5]** if you want, but it is only visual feedback to find the device from the jungle.

Once all fields are good to go, hit **Apply [6]** and you can see the device name and color gets updated **[7]** .

![macos midi configuration update device](images/macos-midi-configuration-update-device.jpg)

*Figure: macos midi configuration update device*

If you have multiple Viruses in your setup, add more devices and make sure each of the devices have individual **Device Name [1]** as set above. Like Virus Rack #1 and Virus Rack #2 etc. This helps you down the road when we connect the hardware to the Editor.

## Connecting Device to MIDI-interface (virtually)

Making virtual connections within MIDI-studio helps us later down the line when we connect the hardware to the Editor and when we make external connections from DAW to hardware. Some DAWs like Logic Pro can see the Device Name created here in MIDI-studio.

Start by drawing the connection points from your external device output port to your MIDI-interface input port. Click and hold down the mouse button from **output port [1]** , start dragging the **cable [2]** towards your MIDI-interface **input port [3]** .

![macos midi configuration connect device](images/macos-midi-configuration-connect-device.jpg)

*Figure: macos midi configuration connect device*

Apply the same procedure for the MIDI input port from your device towards your MIDI-interface output port. The final result should have both cables connected as seen below. I have highlighted Virus Rack, Virus C Desktop and Virus TI2 Desktop and their cables from the spaghetti. (Keep in mind, this is our studio, yours can look a lot different).

![macos midi configuration all connected](images/macos-midi-configuration-all-connected.jpg)

*Figure: macos midi configuration all connected*

These settings are stored within macOS so you don’t have to re-do these settings unless you change your MIDI-interface.
