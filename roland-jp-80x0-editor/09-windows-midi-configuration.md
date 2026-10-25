# Roland JP-80×0 Editor – Windows MIDI Configuration

**HEADS UP :** Windows 11 with multiclient MIDI drivers will enable MIDI devices to be shared between applications - If you are on Windows 11, you can skip creating Virtual paths if you don’t have use for them.

If you plan to route MIDI messages from your DAW to the plug-in channel and send it to the synthesizer from there, then you don’t need to read this, and you can proceed with the DAW guide that is relevant to you.

However, if you use the synth as a master keyboard in your rig or you want to delay compensate the MIDI output with the DAW, then check the advanced procedure below.

Windows **CAN NOT** share MIDI devices between applications (DAW & Editor), therefore virtual ports are the only way to to use the hardware within the DAW and the Editor at the same time.

**ATTENTION** : This is usually the step which is skipped and then you get connection timed out errors and such. Read the guide, it will save our time, your time and you will succeed with the setup!

## Additional Applications needed

Before we jump ahead to launch our DAW, let's do some tweaks in our system to ensure the plug-in can work with maximum efficiency. For that, we are going to need some additional tools.

- MIDI-OX for making routings behind the scenes and
- loopMIDI to create virtual MIDI ports.

We recommend installing an old but trusty MIDI-OX application for Windows to make some virtual routings behind the scenes.

You can download MIDI-OX from here: http://www.midiox.com/zip/midioxse.exe

OR go to MIDI-OX website http://www.midiox.com and download the installer there.

The second application is loopMIDI by Tobias Erichsen which is perfect for creating Virtual MIDI cables inside your workstation.

You can download loopMIDI from here: https://www.tobias-erichsen.de/software/loopmidi.html

**NOTE:** Windows remembers loopMIDI and MIDI-OX settings during each launch. If you do this once, that's all it takes!

## Install MIDI-OX and loopMIDI

Install both MIDI-OX and loopMIDI.

This will allow us to clone the MIDI data from the physical MIDI interface ports to virtual ports and then later on route it inside MIDI-OX back to your DAW while the main port is assigned to the plug-in.

**Example**: MIDI out from JP-8000 -> Roland UM-ONE MIDI input -> MIDI-OX -> loopMIDI virtual port.

This configuration allows us to open the loopMIDI virtual port in the DAW while we use the Roland UM-ONE MIDI port with the plug-in itself. This way there won’t be a crash!

## Configure loopMIDI

Now that loopMIDI is installed, we can configure the ports. The reason why we are installing loopMIDI is so that we can loop back (clone) the MIDI data from the hardware MIDI port to the DAW via MIDI-OX.

*In the example below, we will add Virtual Ports for* ***JP-8000*** *and* ***JP-8080*** *. This is pretty straight forward, but we will guide you through.*

Open loopMIDI settings dialog from the Windows menu bar with right clicking the **loopMIDI icon [1]** and then choose **Configure loopMIDI [2]** .

![Right Click and choose Configure loopMIDI](images/right-click-and-choose-configure-loopmidi.jpg)

*Figure: Right Click and choose Configure loopMIDI*

Once loopMIDI opens up, it should look something like the image below.

![loopMIDI initial view](images/loopmidi-initial-view.jpg)

*Figure: loopMIDI initial view*

## Create Virtual Ports (JP-8000)

In the example below, we are gonna add our JP-8000 ports to loopMIDI. Click the **New port name: field [1]** and type in “JP-8000 vIn”. Click the **+ -sign [2]** to actually add it in.

![Type in your port name and click + to add it in](images/type-in-your-port-name-and-click-to-add-it-in.jpg)

*Figure: Type in your port name and click + to add it in*

Next up we will add another port for output connection. Click the **New port name: field [1]** and type in your Virtual MIDI port connection name. Type in “JP-8000 vOut” and click the **+ -sign [2]** to actually add it in.

![Add another virtual port and click + to add it](images/add-another-virtual-port-and-click-to-add-it.jpg)

*Figure: Add another virtual port and click + to add it*

## Create Virtual Ports (JP-8080)

Since we have JP-8080 in our setup as well, we are going to add the virtual port for it. Click the **New port name: field [1]** and type in “JP-8080 vOut” and click the **+ -sign [2]** to actually add it in.

![Add JP-8080 virtual port and click + to add it](images/add-jp-8080-virtual-port-and-click-to-add-it.jpg)

*Figure: Add JP-8080 virtual port and click + to add it*

Since we are not using our JP-8080 to trigger notes or any other CC data to our DAW, we are only adding a virtual output port. There is no point in adding a virtual input port because it is not used in our case.

**NOTE:** If you have multiple JP’s in your setup, add ports accordingly. We have JP-8000 and JP-8080, so we added both.

If you have two or more JP-8000’s, then make the virtual ports naming obvious to yourself i.e. JP-8000 #1 vIn, JP-8000 #2 vIn etc.

## Advanced Settings

**Open the Advanced [1]** settings tab and change the **SysEx Buffer [2]** size to 512. This will ensure there is enough buffer for incoming data flow.

![Adjust SysEx buffer size](images/adjust-sysex-buffer-size.jpg)

*Figure: Adjust SysEx buffer size*

## Finalize Setup

Right click on the **loopMIDI icon [1]** in the menu bar and toggle on “ **Start minimized** ” & “ **Autostart loopMIDI** ” **[2]** so you don’t have to worry about it during the next boot.

![Finishing touches to loopMIDI setup](images/finishing-touches-to-loopmidi-setup.jpg)

*Figure: Finishing touches to loopMIDI setup*

You can now **close [1]** loopMIDI configuration window.

![Close loopMIDI configuration](images/close-loopmidi-configuration.jpg)

*Figure: Close loopMIDI configuration*

## Configure MIDI-OX

MIDI-OX is the second application needed in order to loop back the MIDI data to the DAW without crashing it. Windows / your DAW will crash if you try to open the MIDI ports twice since most MIDI devices don’t have multicast drivers available.

There are few steps to take in with MIDI-OX, but it will be worth the hassle to get data passing from the synthesizer to your DAW as well as in the plug-in without **crashing** your session.

**Search MIDI-OX [1]** from the Windows startup menu and **open [2]** the application.

![Search MIDI-OX and open it](images/search-midi-ox-and-open-it.jpg)

*Figure: Search MIDI-OX and open it*

The default view of MIDI-OX setup should look like this when you first open it. If not, close all the windows inside MIDI-OX to follow the guide.

![MIDI-OX Initial state](images/midi-ox-initial-state.jpg)

*Figure: MIDI-OX Initial state*

**Click View [1]** menu item and choose **Port Routings… [2]** . This should open a blank routing sheet where we will make our connections.

![Open Port Routings View](images/open-port-routings-view.jpg)

*Figure: Open Port Routings View*

After the Port Routings is opened, we need to open the **Physical** and **Virtual** MIDI ports for the MIDI-OX.

Click **Options [1]** and then choose **MIDI Devices… [2]** .

![Select MIDI Devices from the menu](images/select-midi-devices-from-the-menu.jpg)

*Figure: Select MIDI Devices from the menu*

**NOTE:** There are no Input Ports and Output Ports defined yet in the MIDI Port Routing Window!

Now that the MIDI Devices config window is open, we can see all of your Physical and Virtual MIDI ports which are in our disposal. Before selecting any ports, **uncheck [1]** “ *Automatically attach Inputs to Outputs during selection.* ” or you will end up with a massive connection spaghetti which isn’t what we are making here!

![Uncheck “Automatically attach Inputs to Outputs during selection”](images/uncheck-automatically-attach-inputs-to-outputs-during-select.jpg)

*Figure: Uncheck “Automatically attach Inputs to Outputs during selection”*

## Open MIDI Inputs

Since we have JP-8000 and JP-8080 in our setup, this is very simple.

**UM-ONE [1]** is where our JP-8000 is connected. **JP-8000 vOut [2]** connects to JP-8000 via DAW and **JP-8080 vOut [3]** connects to JP-8080 via DAW.

![Opening appropriate MIDI input ports](images/opening-appropriate-midi-input-ports.jpg)

*Figure: Opening appropriate MIDI input ports*

You might wonder why the “vOut” ports are opened in the INPUT area.. Once we do the routing in MIDI-OX, the port names will appear in opposite order, making it odd to choose JP-8000 vOut in our DAW as a MIDI Input. That might not make sense at this point, but trust me, we’ve done this quite a few times now so follow along.

## Open MIDI Outputs

Now opening output ports is where this might get tricky. **UM-ONE [1]** is where our JP-8000 is connected. **JP-8000 vIn [2]** connects our JP-8000 to the DAW. **UMC1820 MIDI Out [3]** is where your JP-8080 is connected.

Same rule applies here for vIn ports being opened on the opposite side. More details in the port routing section below.

![Opening appropriate MIDI output ports](images/opening-appropriate-midi-output-ports.jpg)

*Figure: Opening appropriate MIDI output ports*

**Click OK [1]** after you have verified your port selections.

![Click OK after Port selections](images/click-ok-after-port-selections.jpg)

*Figure: Click OK after Port selections*

**NOTE:** Your MIDI input and MIDI output ports for your synth might be different to our example so we are only using them to refer where our JP is connected.

Once the MIDI ports are defined, MIDI-OX might automatically assign “MIDI-OX Event Port” to any of the Output Ports chosen.

In case there are pre-made connections in the window, right click one of the **gray nodes [1]** in the wire and choose **Disconnect All [2]** . This will clear all the pre-made connections so we can start from fresh!

![In some cases, MIDI-OX might auto assign some connections..](images/in-some-cases-midi-ox-might-auto-assign-some-connections.jpg)

*Figure: In some cases, MIDI-OX might auto assign some connections..*

## Cloning Devices (virtually)

Start by drawing the connection points from your vOut device input port to your MIDI-interface output port. Click and hold down the mouse button from **JP-8000 vOut port [1]** , start dragging the **cable [2]** towards your **MIDI-interface output port [3]** .

![Making connections in MIDI-OX](images/making-connections-in-midi-ox.jpg)

*Figure: Making connections in MIDI-OX*

Apply the same procedure for the MIDI input port from your device towards your JP-8000 vIn output port. The final result should have both cables connected as seen below.

![JP-8000 ports cloned](images/jp-8000-ports-cloned.jpg)

*Figure: JP-8000 ports cloned*

**NOTE:** In order to establish the connection, you must drag the wire on top of the MIDI plug icon!

## Filtering Virtual connection data

Next up, we will modify the connection properties so that we will block unnecessary data flow. Right click on the **gray dot [1]** at the connection to reveal the menu and choose **Properties… [2]** . You should apply this only for the physical hardware **input port [3]** .

![Right click the dot in connection for Properties](images/right-click-the-dot-in-connection-for-properties.jpg)

*Figure: Right click the dot in connection for Properties*

From the Properties window, let’s block **Common (MTC …)** , **Realtime (Clock, AS …)** and **Exclusive (SysEx)** message by unchecking the boxes in **System [1]** section.

We simply don’t need this data **unless** you send realtime clock info from your Synthesizer to the DAW!

![Filter out unwanted messages](images/filter-out-unwanted-messages.jpg)

*Figure: Filter out unwanted messages*

Click **OK [1]** to apply and close the properties window.

![Close connection properties](images/close-connection-properties.jpg)

*Figure: Close connection properties*

## Finalize Setup

Here is our final connections:

1. JP-8000 vOut routed to Hardware port.
2. JP-8080 vOut routed to Hardware port.
3. UM-ONE routed to JP-8000 vIn port. (with data filter applied).

![Final connections for Roland JP-8000 and JP-8080](images/final-connections-for-roland-jp-8000-and-jp-8080.jpg)

*Figure: Final connections for Roland JP-8000 and JP-8080*

Now after all of the connections are done and we are ready to proceed, click the **traffic light [1]** icon in the MIDI-OX tool bar to toggle MIDI-OX in the taskbar tray.

![Run MIDI-OX in taskbar tray](images/run-midi-ox-in-taskbar-tray.jpg)

*Figure: Run MIDI-OX in taskbar tray*

You can now **minimize [1]** the window so it is out of the way!

![Minimize MIDI-OX to continue!](images/minimize-midi-ox-to-continue.jpg)

*Figure: Minimize MIDI-OX to continue!*

![MIDI-OX sent to taskbar tray](images/midi-ox-sent-to-taskbar-tray.jpg)

*Figure: MIDI-OX sent to taskbar tray*

**TIP** : You should be able to add MIDI-OX in the Windows start up menu so that it will launch automatically when you boot your OS. All the connections will remain, IF the MIDI Devices are connected as they were while making this guide.
