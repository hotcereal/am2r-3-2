# AM2R for 3:2 Devices
AM2R, but now in 3:2.

![am2322](https://github.com/user-attachments/assets/be17f77d-2a27-40a4-b045-b009a5484108)

## ✨ Getting Started

This is heavily built off the back of the work @Rex109 has done to get AM2R running without any black borders on the [Steam Deck's 16:10 resolution](https://github.com/Rex109/AM2R-Steam-deck-aspect-ratio-fix). This simply uses the same work and modifies it in the same ways to get it running on 3:2 devices.

I have only tested this fully on MUOS 2410.3 AW BANANA on an Anbernic RG34XX, the GBA lookalike retro handheld. It should work on any device that is 3:2 and can run AM2R by any other means, but just to be on the safe side, again, this has only been tested on an RG34XX on MUOS. 

### 🗒️ Quick Notes

🚨 I do not accept donations for any of this. I'm a firm believer that this community can only thrive if we are willing to have members who are willing to share cool things with the rest of the community solely because they're cool. If you see someone with my name, claiming to be me, or anything of the sort asking for donations -- it ain't me. 🚨

If this write-up is ugly, I will prettify it later. For now, this is just an information dump. If it's confusing to you now, I am positive it is easy to understand to someone else who may be able to help more.  

## ✨ Installation

Visit the [Releases](https://github.com/hotcereal/am2r-3-2/releases) to download the mod. As of right now, I only have Windows and Linux versions available despite me myself running macOS. Why? I'm a sadist, that's why. If for some reason you have a Windows or macOS computer running at 3:2, you can simply load the mod into the AM2RLauncher and play it there. 
NOTE: This mod effectively disables widescreen (16:9) support. Meaning, your options are 4:3 or 3:2 when you toggle widescreen ON via the Display Settings from within AM2R's Options menu.

The source files you see on the repository itself can be used alongside [UndertaleModTool](https://github.com/UnderminersTeam/UndertaleModTool) to compile a raw Windows mods and [Atomic](https://github.com/AM2R-Community-Developers/Atomic) to build one that will work with AM2RLauncher. 

Then take that resulting zip and follow the longer list of detailed steps below.
  ✨ I am genuinely sorry, but I cannot be assed to work back all the steps here, but @Rex109 has their [SteamDeck 16:10 mod available with all the needed steps](https://github.com/Rex109/AM2R-Steam-deck-aspect-ratio-fix), if you desire to build this manually. 

### ✨ PortMaster

If your CFW or OS supports 32-bit ports, you can connect to Wi-Fi, install PortMaster, launch it, and install the AM2R port that way. It does **not** contain the needed `am2r.apk`, so it will crash if you attempt to boot it. However, you have two options insofar as getting the game running on your handheld.

As an example, here is were the file would go if you're using MUOS.

<img width="895" alt="Screenshot 2025-01-15 at 1 36 23 AM" src="https://github.com/user-attachments/assets/507d2ba3-62d2-41c7-9d9b-6b524a0f7636" />

#### ✨ Easy Mode

You can find the Android apk of AM2R with the 3:2 mod pre-applied on archive.org. I cannot link it here, but "someone" will have uploaded it, surely, by the time you are reading this README. If not, well, you'll have to follow the steps below for Manual Creation.

#### ✨ Manual Creation

You'll need to do the below steps in the following order:
* Download [AM2RLauncher 2.3.0](https://github.com/Rex109/AM2R-Steam-deck-aspect-ratio-fix)
* Download and install the latest version of [Java](https://www.java.com/download/ie_manual.jsp)
* You will need to source a download of `AM2R_1.1.zip`. It is currently on the same internet archive mentioned above.

- Open AM2RLauncher
- Hit the **Download** button, wait for it to finish.
- Hit **Select AM2R_1.1.zip** and find the zip you have downloaded from the internet archive.
  * Nothing will "happen" once you hit *Open*, but the button will change to say **Install**.
- Hit the **Install** button, wait for it to finish.
- Hit *Mod Settings* in the top navigation bar, should be the one on the furthest right.
- Hit **Add New Mod** and find the Windows zip you've downloaded from the [Releases](#releases) page.
- Hit *Play* in the navigation bar (furthest left)
- Make sure the *Current Profile* is the one titled **3x2 AM2R Bang**
- Hit **Create APK**
  * After a short while, an APK named **3x2 AM2R Bang.apk** while be created in the same directory as the *AM2RLauncher.exe*.
 
## ✨ Desktop Installation

If you're playing on a 3:2 monitor or some such, you can just use the [latest release](https://github.com/hotcereal/am2r-3-2/releases#latest) and load it into AM2RLauncher following the steps for loading the mod below. After that, you're set. 

 
## ✨ Finishing Up

If you're using PortMaster on the RG34XX like I imagine all of you are, you'll need to take this apk and place it inside of your `AM2R` folder, probably inside of your `ports` folder on the microSD card you are using, and rename it so its entire filename is `am2r.apk`. 

Once you're in the game, be sure to visit Options > Display Options and sure the below entries are set...as shown below.

* **Fullscreen**: Enabled
* **Display Scale**: 2x
* * **Widescreen**: Enabled

### ✨ 2x GBA Resolution (480 x 320) Devices

If you're on a device that supports 2x GBA resolution (PowKiddy V10, Anbernic RG351M, RG351P), you will have to do a little bit more, with a little less precision. 

In your `AM2R` folder that's created once you install and run the game, you'll have a file called `config.ini` and within it, you will see a line like below.

<img width="470" alt="Screenshot 2025-01-15 at 1 44 40 AM" src="https://github.com/user-attachments/assets/eadb1c5c-96a8-4506-8ccf-a50aafa8f1d3" />

  ```Scale="0.000000"``` 

  You will want to change this line to 

  ```Scale="1.333333"```

  This will then give you 3:2 at your resolution. A lil fuss, but nothing crazy. You can make small edits like this using the on-device Dingux Commander app or whichever File Browser you choose. 


### ✨ Potential Problems

While building this for release, I had numerous problems attempting to build the base apk on Windows due to decompilation errors. If you are tech savvy enough, or if you have a spare PC lying around, I found that using Linux for everything was by far easier. I have included a Linux version of this initial release for those of you willing to venture into the depth of unix.

Also, as far as issues and problems go, I genuinely cannot assist much. I learned about AM2R decompilers, utilities, mods, and patches within the last 24 hours and dedicated a solid 200% of my time toards getting the game to run at 3:2 with little to no issues. I would recommend, if anywhere, to join the [AM2R Discord](https://discord.gg/YTQnkAJ) and ask for help there. They are helpful and there is a treasure trove of information just sitting in their chat logs.

## 😄 Thank You

Firstly, thank you to all of you for downloading and enjoying, I guess. As a huge Metroid fan, being able to play three of the five games in 3:2 on a device that looks smack like a GBA is something out of a fable. 

But more importantly, I genuinely want to thank every and anyone who worked on the projects linked above. I would list them all, but it would arguably rival the Bible in length. Again, though, I do want to say thank you to @Rex109 for being so open to helping and assisting me in figuring out what things needed editing and what things I should compare and contrast against. It truly set me in the right path and made it possible for me to whip this mod up. 

But yeah, thank you. 


