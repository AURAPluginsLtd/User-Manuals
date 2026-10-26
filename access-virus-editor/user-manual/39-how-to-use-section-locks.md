# Access Virus Editor – How To Use Section Locks

We added a Section Lock function to lock certain sections of the Editor to prevent changes up on part program changes or when a randomizer is triggered. This is great when you find a perfectly adjusted filter or oscillator: lock the section to keep those settings locked in.

You can lock any of the sections which have the **LOCK [1]** symbol in it – There are more locks available in the other tabs too!

When **LOCK [1]** is toggled on at any section, **RELEASE ALL LOCKS [2]** button will allow you to release all locks with one click. This is ideal if you have overlooked your layers and data is being transmitted back and forth even if you don’t want that.

**LOCKS [3]** on the “ **QUICK MIXER** ” view locks or unlocks the entire part at once. There are individual locks for each part.

![how to use section locks](images/how-to-use-section-locks.jpg)

*Figure: how to use section locks*

> **NOTE:** When you have sections locked, there will double the amount of SysEx traffic in the MIDI stream due to the fact that the Editor has to send the ”locked” info back to the hardware after the patch is changed. If you scroll patches from the librarian, then the data stream is normal.
