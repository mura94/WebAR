# WebAR
Testing AR visualization for Safari on iOS devices. Click 👉[here](https://mura94.github.io/WebAR/) to view the Web AR test page in Safari on an iOS device.



### Packages Required
- A 3D Modeling Software that can export to GLTF 2.0 (Blender works)
- [XCode 11](https://apps.apple.com/us/app/xcode/id497799835?mt=12)
- [USDZ Tools](https://developer.apple.com/download/more/?=USDPython)

# Current Workflow
`Note: In progress. Subject to change`

## 1. Prepare Model
- Import model into Blender
- Animate and texture model
- Export the model in GLTF 2.0 format
  - `Note: This is the only type I've found that will carry over skinned/rigged animations using Apple's USDZ Python tools`
- Transfer to macos device (if neccessary)
  - Google drive, usb, box, however you want

## 2. Convert Model to USDZ
- Open the USDZ python command line tools
  - Can be done by opening `~/Applications/usdpython/USD.command`
- In the terminal window, navigate to the directory of your .gltf file that you transfered over
  - do this by entering `cd <yourfolder>` (exclude the gltf file from this path, you just want to be in the directory)
- Convert your .gltf model to .usdz
  - do this by entering `usdzconvert <modelFileName>.gltf <newfilename>.usdz`
- When that's finished, you should see your new .usdz file in that directory in Finder

`Note: You may also use Apple's Reality Converter Beta tool, which is essentially a GUI for the USDZ command line tools` 

## 3. Customize Interactions in Reality Composer
- Open Reality Composer
  - This can be done in the iPad app from the App Store, or on a mac via the XCode menu (`XCode>Open Developer Tool>Reality Composer`)
  - If using the iOS Reality Composer app, you will have to transfer the converted .usdz file to the iPad's local storage (Drive, Box, etc) before importing the file into a scene
- Drag & Drop or Add (+ symbol) and import the converted .usdz file to view it in the scene
- To start an animation by tapping (or however you would like it to trigger), select the Behaviours icon (asterisks/right arrow icon)

`To be continued`
