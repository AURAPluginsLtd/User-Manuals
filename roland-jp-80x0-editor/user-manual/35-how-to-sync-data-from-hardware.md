# Roland JP-80×0 Editor – How To Sync Data From Hardware

## Performance data and individual layers

## Method #1

If **PERFORMANCE [1]** mode is toggled on, **Sync Data from HW [2]** button will request **performance data [3]** and individual layers to the user interface like discussed earlier. This will take some time depending on the selected JP model. JP-8080 requests take a bit longer due to differences in the data package.

![JP-80x0 Editor User Manual - Sync Data Method #1](images/jp-80x0-editor-user-manual-sync-data-method-1.jpg)

*Figure: JP-80x0 Editor User Manual - Sync Data Method #1*

## Method #2

If **BROWSER [1]** view is toggled on, **Sync Data from HW [2]** button will request performance data and individual layers to the user interface just like the previous method. This will also request Global data which is essential on the first sync.

![JP-80x0 Editor User Manual - Sync Data Method #2](images/jp-80x0-editor-user-manual-sync-data-method-2.jpg)

*Figure: JP-80x0 Editor User Manual - Sync Data Method #2*

## Individual Layers

You can also make a quick request for individual layers when **BROWSER [1]** is toggled off. **Sync Data from HW [2]** will request active data to the **selected layer [3]** instead of complete data request, but ONLY if data mode is set to **Patch Mode [4]** .

![JP-80x0 Editor User Manual - Sync Individual Layers](images/jp-80x0-editor-user-manual-sync-individual-layers.jpg)

*Figure: JP-80x0 Editor User Manual - Sync Individual Layers*

**TIP** : Be patient and do not disturb the data flow with any knob movements or so. This will ensure the data packages are being sent and received as expected and you are not going to receive any SysEx error messages!

If you feel like your MIDI device can do faster requests than what we have set, you can try to play around with the Request Interval multiplier. **Open Utilities [1]** menu, select **Editor Preferences [2]** and select first value from the **options [3]** available. The editor will automatically increase the value if it experiences drop-outs during the request process.

![JP-80x0 Editor User Manual - Sync Request Interval](images/jp-80x0-editor-user-manual-sync-request-interval.jpg)

*Figure: JP-80x0 Editor User Manual - Sync Request Interval*
