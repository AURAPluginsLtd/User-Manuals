# Roland JP-80×0 Editor – Request Performance Data from Hardware

**NOTE:** To successfully request the multi data from the hardware, STOP all activities on your DAW so that the SysEx data is received as expected!

## from Temp Buffer to Editor GUI

Open the **BANK EDIT** menu and choose **Request Performance Data … -> from Temp Buffer to Editor GUI** to get the buffer data from the Hardware to the Editor User Interface. This action will request performance data, which includes both layers.

![request performance to ui](images/request-performance-to-ui.jpg)

*Figure: request performance to ui*

## from Temp Buffer to Librarian

Open the **BANK EDIT** menu and choose **Request Performance Data … -> from Temp Buffer to Librarian** to get the buffer data from the hardware to the Librarian.

![request performance to librarian](images/request-performance-to-librarian.jpg)

*Figure: request performance to librarian*

You can achieve the same result with **right mouse click** at the top of slot 68 and choose **Get DATA from … -> Hardware Edit Buffer** .

![request performance to librarian via right click](images/request-performance-to-librarian-via-right-click.jpg)

*Figure: request performance to librarian via right click*

## Editor User Interface

If the JP Edit buffer differs from the Editor buffer, you can also request User Interface data to the Librarian slot with **right mouse click** at the top of the slot and choose **Get DATA from … -> Editor (active performance)** .

![request performance to librarian from editor](images/request-performance-to-librarian-from-editor.jpg)

*Figure: request performance to librarian from editor*

## from Selected Program Slot

Open the **BANK EDIT** menu and choose **Request Performance Data … -> from Selected Program Slot** to get Performance from U 68.

U is defined in the REQ DATA FROM menu on the left hand side view. Slot is determined by the user selection in the Librarian View.

![request performance from slot](images/request-performance-from-slot.jpg)

*Figure: request performance from slot*

You can achieve the same result with **right mouse click** at the top of slot 68 and choose **Get DATA from … -> Hardware by Prog No** .

![request performance from slot via right click](images/request-performance-from-slot-via-right-click.jpg)

*Figure: request performance from slot via right click*

**NOTE:** REQ DATA FROM menu selection defines the Bank Address for hardware requests!

## All Data from USER Bank

Open the **BANK EDIT** menu and choose **Request Performance Data … -> All Performances from USER Bank** .

This action will request all USER bank Performances to the Librarian from your hardware.

![request user performances](images/request-user-performances.jpg)

*Figure: request user performances*

## All Data from PRESET Bank

Open the **BANK EDIT** menu and choose **Request Performance Data … -> All Performances from PRESET Bank** .

This action will request all PRESET bank Performances to the Librarian from your hardware.

![request preset performances](images/request-preset-performances.jpg)

*Figure: request preset performances*

When **Hardware MODEL [1]** is set to JP-8080, you have a lot more options for PRESET banks as well as for Smart Memory Card slots (if inserted).

![request performances from jp-8080](images/request-performances-from-jp-8080.jpg)

*Figure: request performances from jp-8080*
