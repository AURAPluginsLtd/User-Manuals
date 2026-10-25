# Troubleshooting

## Troubleshooting

**NOTE:** FAQs are listed first, then we have some random Troubleshooting scenarios listed below!

### General FAQs

### Do I need to remove the DEMO before installing the FULL version?

No. The FULL installer will overwrite the DEMO version in your hard drive.

### Where is the Editor User Manuals located?

We are writing User Manuals as we proceed with the version xx.xx.xx updates.

All manuals will be available in https://auraplugins.com/support/ once the product update is wrapped up. Alternatively you can find the manual download from the product downloads page.

### I am unable to run the Installer, what can I do?

If for some reason the installer fails to run, try opening the installer with right click -> open.

This usually solves the problem. Our Editors only interact with the hardware unit, so they’re safe to use.

### Which functions are not available in the DEMO version?

1. Users can not save requested data from hardware to HDD.
2. Users can not store patches from librarian to hardware.
3. Total Recall is disabled. This means, your last used Editor settings will not be sent to your hardware automatically upon loading the project.
4. MIDI Learn is disabled. Users can not map favorite CC controls to Editor parameters.
5. Editor parameters are not visible for DAW to automate.
6. Users can not store UI DATA files (arrangements).
7. The demo version can not be registered.

### What are the Editor requirements?

1. You must have the real hardware (or DSP Emu), which the editor is made for.
2. Version xx.xx.xx requires 64-bit AAX, Audio Unit, VST2 or VST3 host for Mac or PC.
3. Version xx.xx.xx requires Mac with Metal supported graphics.
4. Version 1.x and 2.x requires a 32/64-bit Audio Unit / VST host for Mac or PC.
5. MIDI interface. A good one which supports SysEx messages. ESI MIDIMATE XT is proven to work.
6. Direct MIDI in / out connection between your hardware and the MIDI interface. No MIDI Thru connections or MIDI in only / MIDI out only connections OR direct USB connection to computer if USB is available in hardware.
7. Audio cables from the synth to the sound card or mixer in order to hear the sound.
8. At least FULL HD resolution display.

### Do these Editors generate any sound?

Not at the moment. Our Editors are designed to control the real hardware unit from your favorite DAW or with the Standalone Application.

### License FAQs

### Can I transfer my license to someone else when I sell the synth?

No. Editor license fee covers support for one customer only. If the license is transferred to a 3rd party, we will revoke the license and download access.

### Can I use my license on multiple computers?

Yes, as long as the computer is yours. If we get a support request made with your license data, your account might be compromised and opted for permanent removal.

### Why does the Editor say reload license after copying the license to the right folder?

The editor has failed to read the license file. Make sure the license doesn’t have any additional extensions ie. “Access Virus Editor.license.txt”. If you see .txt appended, rename the file to “Access Virus Editor.license” and try to validate again.

**Note** that the new version has a new location AND name for license.

License should be placed in

```
~/Music/AURA Plugins/“plug-in named folder”/”plug-in name”.license
```

### How do I add the license for the Editor to register?

Downloaded license.key must be renamed to “(plugin name).license” and placed in:

`~/Music/AURA Plugins/(plugin name)/` folder.

To make this easy, click on “register” text in the top left corner to open the file browser dialog and open the license file with it. Rest will be automated.

### Do I need an internet connection to activate the Editor?

No, you can purchase the Editor license from our store and download the license.key + full installers and take them to your offline computer for setup. Internet connection has advantages like automated update check which usually is something that improves the Editor usage!

### I just purchased the Editor, where can I download the license?

1. Login at https://auraplugins.com/my-account/
2. Click the Downloads page link. Once you are there, select the product you are looking for and you can download the license and Editor full installers for macOS or Windows.

### Troubleshooting FAQs

### Why Editor displays DEMO version after purchasing the license?

You need to download and install the FULL version of our Editor in order to register it.

Head down to https://auraplugins.com/my-account/ (login if prompted) – Navigate to the downloads page and select the product you want.

1. Download the full installer and license.
2. Install full version.
3. Check license instructions and install license.
4. Re-open the Editor to validate the license.
5. When validation succeeds, the Editor says “Registered” in the top left corner.

### Why does my DAW crash when I set MIDI in / out from the editor?

This is usually caused by the fact that your DAW has the MIDI port in use.

Be sure to follow our DAW User Guides to set up your environment properly before setting the MIDI ports.

Start with the Setting MIDI Devices guide and follow up with the specific hardware instructions.

### Why does the Editor fail to connect with the hardware?

There are a few reasons why this could happen, so let's make sure everything is right:

1. MIDI out from your hardware is connected to your MIDI interface input.
2. MIDI out from your MIDI interface is connected to your hardware input.
3. Hardware has Global MIDI Channel set as instructed.
4. Hardware has Device ID set as instructed.
5. Hardware is in Performance / Multi mode (mono timbral and FX Editors excluded).

If all of these conditions are right and the Editor still fails, check the MIDI interface specs to ensure it can handle large SysEx packages which the Editor & Hardware uses to send program data back and forth.

You can open a ticket with our Support Team if you’re stuck.

### I think I found a BUG, how can I report it?

You can report any BUGs via our Bug Report form. It is very important to include all of the details that can help us solve the issue. https://auraplugins.com/my-account/bug-report/

- Your computer specs
- Your hardware specs
- How we can reproduce the issue

The more information we get from the Bug Report, the easier it is for our team to resolve it.

Updates are not immediate, if another update process is in the works.

### When I change preset in hardware, Editor is not receiving the data

**Cause 1** : If hardware DeviceID differs from the Editor DeviceID set. Usually when DeviceID matches with the hardware, then data flow works perfectly.

**Cause 2** : If DAW playback is on, then data transfers are held back because of excessive MIDI data flows. This is to prevent hanging notes and mis-aligned data.

**Cause 3** : Request Data on Program Change is toggled OFF. In this case you can change presets in hardware without interactions with the Editor. Use case: you want to quickly go through sounds to find the sound you need. Remember to Sync Data from HW if this is toggled off on purpose.

### I get connection timed-out messages when changing programs

See above!

### I don’t get sound from Hardware after chancing programs

**Cause 1** : During the initial MIDI Input / MIDI Output configuration step, Editor was unable to sync data with the hardware, therefore Editor can not route MIDI channel messages to appropriate Layer.

**Cause 2** : When Multi is changed, it might have changed the Part MIDI Channels to different channels configured on your DAW MIDI track.

### My DAW freezes when I insert the Virus Editor or when I import a bank

**Cause** : Our Editor checks the file you have chosen to import into the Editor. During this time, if the Editor detects an error with the file, it might get stuck.

Check further details on How to Enable LOG article for details to reveal which bank is causing the issue and how to resolve it.

### I can only play one Part when MIDI is triggered on Editor track

**Cause** : Incoming MIDI channel from DAW track usually determines which Part is played, if channels match. You can engage the SHOW KEYBOARD function to force incoming MIDI data to the currently selected part.

### Data is not recalled properly when I re-open my project

**Cause** : Maybe the DeviceID has changed or something else is wrong with the configs. Double check your MIDI ports on the Editor, DeviceID on both ends and then try PUSH DATA TO HW from LIBRARIAN VIEW.

### MIDI input and MIDI output is not memorized on new instances

**Cause** : This is by design. We have learned that in some cases where MIDI input and output ports are stored within the Editor, it has the potential to crash the DAW on plug-in insertion. We are looking to fix this in the upcoming release.

In the meanwhile, if you are confident your setup can handle memorizing the MIDI ports, you can set up the Editor as usual and then save the entire channel strip as a preset to your DAW channel strip settings. Next time you recall the channel strip setting, MIDI is assigned and data from the Editor is pushed to the hardware (unless it's disabled via the Utilities menu).

### Something else that buzzles me…

You can open a ticket from my-account page (https://auraplugins.com/my-account/tickets/) if your issue is not listed above. We will update the FAQs and Troubleshooting page as time goes on.

### Closure

Hopefully this User Manual helped you understand how the Editor works and how it is designed to work. Now start making some awesome tunes and don’t forget to review our product – that would make our day!
