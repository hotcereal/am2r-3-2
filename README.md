# AM2R for 3:2 Devices
AM2R, but now in 3:2.

## Getting Started

This is heavily built off the back of the work @Rex109 has done to get AM2R running without any black borders on the [Steam Deck's 16:10 resolution](https://github.com/Rex109/AM2R-Steam-deck-aspect-ratio-fix). This simply uses the same work and modifies it in the same ways to get it running on 3:2 devices.

I have only tested this fully on MUOS 2410.3 AW BANANA on an Anbernic RG34XX, the GBA lookalike retro handheld. It should work on any device that is 3:2 and can run AM2R by any other means, but just to be on the safe side, again, this has only been tested on an RG34XX on MUOS. 

## Installation

Visit the Releases to download the Windows or Mac version of the mod. If for some reason you have a Windows or macOS computer running at 3:2, you can simply load the mod into the AM2RLauncher and play it there. 
NOTE: This mod effectively disables widescreen (16:9) support. Meaning, your options are 4:3 or 3:2 when you toggle widescreen ON via the Display Settings from within AM2R's Options menu.

The source files you see on the repository itself can be used alongside UndertaleModTool and Atomic to build a raw Windows mod. 
Then take that resulting zip and follow the longer list of detailed steps below.
  • I am genuinely sorry, but I cannot be assed to work back all the steps here, but @Rex109 has his SteamDeck 16:10 mod available with all the needed steps, if you desire to build this manually. 

### Android/PortMaster

If your CFW or OS supports 32-bit ports, you can install PortMaster, launch it, and install the AM2R port that way. It does **not** contain the needed am2r.apk, so it will crash if you attempt to boot it. However, you have two options.

#### Easy mode

You can find the Android apk of AM2R with the 3:2 mod pre-applied on archive.org. I cannot link it here, but "someone" will have uploaded it, surely, by the time you are reading this README. If not, well, you'll have to follow the steps below for Manual Creation.

#### Manual Creation

You'll need to do the below steps in the following order:

Download [AM2RLauncher 2.3.0](https://github.com/Rex109/AM2R-Steam-deck-aspect-ratio-fix)

 Download and install the latest version of [Java](https://www.java.com/download/ie_manual.jsp) (if on Windows)
 
 You will need to source a download of AM2R v1.1. It should be a zip file. It is currently on the same internet archive mentioned above.

- Open AM2RLauncher
- Hit the **Download** button, wait for it to finish.
- Hit **Select AM2R_1.1.zip** and find the zip you have downloaded from the internet archive.
  * Nothing will "happen" once you hit *Open*, but the button will change to say **Install**.
- Hit the **Install** button, wait for it to finish.
- Hit *Mod Settings* in the top navigation bar, should be the one on the furthest right.
- Hit **Add New Mod** and find either the Mac or Windows zip (depending on your current OS) you've downloaded from the Releases page.
- Hit *Play* in the navigation bar (furthest left)
- Make sure the *Current Profile* is the one titled **3x2 AM2R Bang**
- Hit **Create APK**
  * After a short while, an APK named **3x2 AM2R Bang.apk** while be created in the same directory as the *AM2RLauncher.exe*.

If you're using PortMaster on the RG34XX like I imagine all of you are, you'll need to take this apk and place it inside of your `AM2R` folder, probably inside of your `ports` folder on the microSD card you are using, and rename it so its entire filename is `am2r.apk`. 
