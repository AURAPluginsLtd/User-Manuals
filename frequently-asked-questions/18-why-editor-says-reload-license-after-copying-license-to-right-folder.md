---
question: "Why Editor says reload license after copying license to right folder?"
department: "License"
source_url: "https://auraplugins.com/kb/faq/why-editor-says-reload-license-after-copying-license-to-right-folder/"
---
# Why Editor says reload license after copying license to right folder?

There are usually two reasons for that:

1. Editor has failed to read the license file. Make sure the license doesn’t have any additional extensions ie. “Access Virus Editor.license.txt”. If you see .txt appended, rename the file to “Access Virus Editor.license” and try to validate again.
2. Editor has failed to locate the license file. Make sure the license is in the Editor data folder (versions 1.x-2.x):

```
Macintosh HD/Library/Audio/Presets/Mystery Islands Music/(plugin name)/license.key
```

**Note** that new version has a new location AND name for license. Sample below:

```
~/Music/AURA Plugins/Access Virus Editor/Access Virus Editor.license
```
