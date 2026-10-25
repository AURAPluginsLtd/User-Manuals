# Access Virus Editor – Request Patch Data from Hardware

**NOTE:** To successfully request the patch data from the hardware, STOP all activities on your DAW so that the SysEx data is received as expected!

## from Active Layer to Editor GUI

Open the **BANK EDIT** menu and choose **Request Patch Data … -> from Active Slot to Editor GUI** to get the buffer data from the Hardware to the Editor User Interface. In this case, Librarian will get the data to Editor UI from the currently selected PART.

![request patch data - from part to user interface](images/request-patch-data-from-part-to-user-interface.jpg)

*Figure: request patch data - from part to user interface*

## from Active Slot to Librarian

Open the **BANK EDIT** menu and choose **Request Patch Data … -> from Active Slot to Librarian** to get the buffer data from the currently selected part to the Librarian. In this case, Part 7 data is requested to the selected slot, which is slot 31.

![request patch data - from part to librarian](images/request-patch-data-from-part-to-librarian.jpg)

*Figure: request patch data - from part to librarian*

You can achieve the same result with **right mouse click** at the top of any slot and choose **Get DATA from … -> Editor (active patch)** .

![request patch data - from part to librarian](images/request-patch-data-from-part-to-librarian-2.jpg)

*Figure: request patch data - from part to librarian*

## Hardware Edit Buffer

If the Virus edit buffer differs from the Editor buffer, you can also request the Edit Buffer to the Librarian slot with **right mouse click** at the top of the slot and choose **Get DATA from … -> Hardware Edit Buffer** .

![request patch data - from edit buffer](images/request-patch-data-from-edit-buffer.jpg)

*Figure: request patch data - from edit buffer*

## from Selected Program Slot

Open the **BANK EDIT** menu and choose **Request Patch Data … -> from Selected Program Slot** to get Patch from Bank A prog 31.

Bank A is defined in the BANK menu on the editor control display. Slot is determined by the user selection in the Librarian View.

![request patch data - from program slot](images/request-patch-data-from-program-slot.jpg)

*Figure: request patch data - from program slot*

You can achieve the same result with **right mouse click** at the top of any slot and choose **Get DATA from … -> Hardware by Prog No** .

![request patch data - request from program slot](images/request-patch-data-request-from-program-slot.jpg)

*Figure: request patch data - request from program slot*

**NOTE:** BANK menu selection in **Editor Control Display** defines the Bank Address for hardware requests!

## All Patches from RAM A…D

Open the **BANK EDIT** menu and choose **Request Patch Data … -> All Patches from RAM A … D** of your choice.

This action will request all RAM bank Patches to the Librarian from your hardware.

![request patch data - ram slots](images/request-patch-data-ram-slots.jpg)

*Figure: request patch data - ram slots*

## All Patches from ROM A…Z

Open the **BANK EDIT** menu and choose **Request Patch Data … -> All Patches from ROM A … Z** of your choice.

This action will request all ROM bank Patches to the Librarian from your hardware.

![request patch data - rom slots](images/request-patch-data-rom-slots.jpg)

*Figure: request patch data - rom slots*
