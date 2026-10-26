# Ableton Live and Virus TI USB Audio with macOS

### Selecting the right Audio Devices

Lets open Ableton Live and set everything up in it. First, click **Live [1]** menu and open **Preferences [2]**

![access virus editor ableton live settings](images/access-virus-editor-ableton-live-settings.jpg)

Start by setting the Audio **Input Device [1]** and select the **Aggregate Device [2]** you created from the list

![access virus editor ableton live select input device](images/access-virus-editor-ableton-live-input-device.jpg)

Next we can select the Audio **Output Device [1]**, but this time, we want to select our **master device [2]**, *in my case that would be Fireface 800*!

![access virus editor ableton live select output device](images/access-virus-editor-ableton-live-output-device.jpg)

Audio devices are now set, however, if you want to rename your input channels, click **Input Config [1]** to open the inputs view

![access virus editor ableton live input config toggle](images/access-virus-editor-ableton-live-input-config-toggle.jpg)

Remember how we had inputs configured earlier in the **Aggregate Device view [1]**, well, you can now rename your **Live inputs [2]** with same titles so it is easier to select the proper inputs in your DAW!

![access virus editor ableton live configure inputs](images/access-virus-editor-ableton-live-input-config.jpg)

Here is my result after renaming the titles, **Aggregate Device input [1]** names match **Live input [2]** names. Notice that I have manually enabled each input (the numbered titles are lit). Once you have configured your names, click **OK [3]** to close the window.

![access virus editor ableton live rename inputs](images/access-virus-editor-ableton-live-input-rename.jpg)

Final step before closing the Settings view is to make sure that you adjust your **buffer settings [1]**. I would personally start with lowest possible value you know your soundcard can handle. I’m setting mine to 64 Samples. Click **close [2]** toggle once you’re set!

![access virus editor ableton live adjust buffer](images/access-virus-editor-ableton-live-buffer.jpg)

> **NOTE:** If buffer setting is too low or too high, Virus TI USB stream will experience clicks and pops. You have to find a right balance for your setup by testing which works the best.

I personally don’t have any issues running 64 Samples with my M1 powered Mac. In fact, I can easily run 256 inputs in the studio with all channels being enabled for monitoring / recording.

### Insert the Access Virus Editor

Lets insert the Access Virus Editor into the project now. We are gonna use Audio Unit since it provides best macOS integration with best stability. VST3 is the worst with MIDI, especially with multi channel configuration.

**Drag’n’drop** the Editor to Live (we recommend Audio Unit).

![access virus editor ableton live insert plugin](images/access-virus-editor-ableton-live-insert-plugin.jpg)

After a few seconds, this will open the Editor user interface.

![access virus editor ableton live plugin initialized](images/access-virus-editor-ableton-live-plugin-initialized.jpg)

Lets adjust the User Interface and preferences before jumping into loading patches etc:

- 1) set **UI Scheme** to match your taste.
- 2) set **Model** to match your Virus TI model (**Virus TI-series** covers TI and TI2, **Virus TI Snow** is for TI Snow desktop users).
- 3) check **Device ID** and ensure it matches your Virus TI Device ID. (we recommend DeviceID 1).  
  *rest of the settings are requested from the Virus once MIDI input and output are set.*
- 4) set **MIDI IN** port **FROM: Virus TI USB Plugin I/O**.
- 5) set **MIDI OUT [5]** port **TO: Virus TI USB Plugin I/O**.
- 6) Editor will start **automatic sync with the hardware**, getting global settings and parts from the Virus to the Editor User Interface. Wait until it’s done.

![access virus editor ableton live plugin settings](images/access-virus-editor-ableton-live-plugin-settings.jpg)

And the final result after the request process has been completed:

![access virus editor ableton live plugin syncronized](images/access-virus-editor-ableton-live-plugin-syncronized.jpg)

Part 1 of the Editor setup is done, lets **minimize** the view with left mouse click on the **triangle at the top left corner [1]** and move to adding Audio and MIDI tracks!

![access virus editor ableton live minimize editor view](images/access-virus-editor-ableton-live-plugin-minimize.jpg)

**HEADS UP #1**: When using USB connection, our Editor works with the Virus TI ONLY via the Plugin I/O ports on macOS. Windows has other options available. We will cover that later on with another article.

**HEADS UP #2**: External I/O is used for additional gear, like keyboard to trigger DAW or additional sound modules like Novation Supernova II Rack etc.

### Create MIDI tracks

To get sample accurate MIDI from your DAW, we recommend to add MIDI tracks for each part used in your session. Our Editor is missing Audio DSP, therefore MIDI output is not compensated which might lead to timing errors.

**Right click [1]** on the Live mixer background and choose **Insert MIDI Track** or use key command **SHIFT + CMD + T**. I’ve added 4 tracks for this example – you can add up-to 4 channels with Virus TI Snow and 16 channels with other TI models.

![access virus editor ableton live add midi tracks](images/access-virus-editor-ableton-live-add-midi-tracks.jpg)

Now assign **MIDI To** pointing towards **Virus TI USB (Plugin I/O) [1]** for all channels you’ve created. Next assign each **MIDI Track channel [3]** to match the Editor/Hardware channels. As you can see from the image below, Part 1 has CHA 1 assigned to it, etc.

If you can’t see the MIDI port in the list, click **Configure… [2]** and see image further below how to make it visible.

![access virus editor ableton live assign midi ports and channels](images/access-virus-editor-ableton-live-assign-midi-ch.jpg)

MIDI port configure opens the Settings dialog MIDI settings page. Scroll down the list and Locate Virus TI USB (Plugin I/O). **Enable tracking [1]** and **sync [2]** for the port and close the window. Now the port name is visible in Live.

![access virus editor ableton live set midi clock and tracking](images/access-virus-editor-ableton-live-assign-midi-clock.jpg)

> **NOTE:** After Initial sync is done with the Virus TI, you should double check the MIDI channels per parts. Virus TI doesn’t transmit the channel settings back to the Editor User Interface when Sequencer mode is toggled on.

### Create Audio tracks

**Right click [1]** on the Live mixer background and choose **Insert Audio Track** or use key command **CMD + T**. I’ve added 6 tracks for this example – if you use USB only, then you can add 3 tracks – I’m combining USB + Analog Outputs.

![access virus editor ableton live add audio tracks](images/access-virus-editor-ableton-live-add-audio-tracks.jpg)

Assign **Inputs [1]** in the mixer view. Audio 10 has inputs **31/32 VirusTI usb1 L&R [2]** etc. After you’ve assigned all the inputs, toggle on **Input Monitoring [3]** to hear the Audio from the Virus TI once notes are triggered. **Audio 13 – Audio 15 input ports [4]** are my Fireface 800 inputs 1-6 enabled, where my Virus TI analog outputs are routed to.

![access virus editor ableton live assign audio inputs](images/access-virus-editor-ableton-live-assign-audio-inputs.jpg)

Now the final step is to MAKE SURE THAT THE EDITOR PART OUTPUT is routed to USB 1, USB 2 or USB 3 in order to hear the Audio!

In the Editor window, double click the triangle in the **top left corner [1]** to enlarge the User Interface.

Now open **output [2]** dropdown for each PART and select your desired output. **usb1-usb3 outputs [3]** are listed at the bottom, while **analog outputs [4]** are listed on the top.

![access virus editor ableton live assign audio outputs](images/access-virus-editor-ableton-live-assign-audio-outputs.jpg)

USB outputs from Virus TI are now routed to tracks 10-12 while Analog outputs are routed to tracks 13-15.

Now select a MIDI track you assigned for Virus TI and start playing! Make sure you have **Input Monitoring enabled [1]** for the specific MIDI track to send the notes to the hardware. In this last screenshot, we can follow the signal path as follows:

**2)** MIDI from Live tracks 6-9 is assigned to Editor / Hardware Parts 1-4.  
**3)** Audio from Hardware is assigned to Audio tracks 10-15 with Input Monitoring enabled.

![access virus editor ableton live audio and midi routing](images/access-virus-editor-ableton-live-virus-ti-configure.jpg)

**This is it!** Access Virus TI USB Audio with macOS is working! It is really simple once you get it going – You can save the template after everything is configured, but keep in mind that you should check the Aggregate Device and make sure the Virus TI is enabled before you start your session.

## Conclusion

It was all about creating aggregate device in the macOS Audio and MIDI Setup app so that I could add the Virus TI device in the chain. Caveat is that USB connection can get “killed” when the synth is powered off and the synth communication is VERY slow, especially when data is being requested from the Virus TI to the Editor. Overall the Virus TI USB Audio setup is simple.

Data flowing out from the Editor to Virus TI works out just fine.

Checkout our Access Virus Editor and spread the word – Its been a long road.

[Access Virus Editor](https://auraplugins.com/product/access-virus-editor/) Product page (requires Access Virus synthesizer or DSP56300Emulator with Virus OS) (DSP56300 Setup Guide is coming soon!)

[Access Virus Editor](https://auraplugins.com/downloads/access-virus-editor/) Downloads page (logged in customers can see full downloads, guests can see demo downloads).

For those who don’t like to read, here is a video how we setup Access Virus TI USB Audio with macOS:

[Access Virus TI with Apple Silicon MAC and USB](https://www.youtube.com/watch?v=WF4qOYuwH5c)

[Return](../user-manual/09-virus-ti-usb-audio-connection.md) to Virus TI USB Audio connection article
