# AM2R for 3:2 Devices
AM2R, but now in 3:2.

![am2r3f](https://github.com/user-attachments/assets/0541560d-ae0a-4b6b-9d2c-02830ef12c6a)


## ✨ Getting Started

This is heavily based off the work [@Rex109](https://www.github.com/Rex109) has done to get AM2R running without any black borders on the [Steam Deck with its 16:10 aspect ratio](https://github.com/Rex109/AM2R-Steam-deck-aspect-ratio-fix). This simply uses the same work and modifies it in similar ways to get the game running without borders or stretching on 3:2 devices.

I have only tested this fully on MUOS 2410.3 AW BANANA on an Anbernic RG34XX, the GBA lookalike retro handheld. It should work on any device that is 3:2 and can run AM2R, but just to be on the safe side, again, this has only been tested on an RG34XX on MUOS. 

### 🗒️ Quick Notes

🚨 I do not accept donations for any of this. I'm a firm believer that this community can only thrive if we collectively share cool things with each other. If you see someone with my name, claiming to be me, or anything of the sort, asking for donations -- it ain't me. 🚨

If this write-up is ugly, I will prettify it later. For now, this is just an information dump. If it's confusing, hit me up on Reddit, Twitter, or whatever the hell I'm on. 

## ✨ Installation

Visit the [Releases](https://github.com/hotcereal/am2r-3-2/releases) page to download the mod. As of right now, I only have Windows and Linux versions available despite me myself running macOS. Why? I'm a sadist, that's why. If for some reason you have a computer running at 3:2, you can simply load the mod into the AM2RLauncher and play it. 
NOTE: This mod effectively disables widescreen (16:9) support. Meaning, your options are 4:3 or 3:2 when you toggle widescreen ON via the Display Settings from within AM2R's Options menu.

The source files you see on the repository itself can be used alongside [UndertaleModTool](https://github.com/UnderminersTeam/UndertaleModTool) to compile a raw Windows mod, and [Atomic](https://github.com/AM2R-Community-Developers/Atomic) to build one that will work with AM2RLauncher. 

Then take that resulting zip and follow the longer list of detailed steps below.
  ✨ I am genuinely sorry, but I cannot be assed to work back all the steps here, but @Rex109 has their [SteamDeck 16:10 mod available with all the needed steps](https://github.com/Rex109/AM2R-Steam-deck-aspect-ratio-fix), if you desire to build this manually. 

### ✨ PortMaster

If your CFW or OS supports 32-bit ports, you can connect to Wi-Fi, install PortMaster, launch it, and install the AM2R port that way. It does **not** contain the needed `am2r.apk`, so it will crash if you attempt to boot it. However, you have two options insofar as getting the game running on your handheld.


#### ✨ Easy Mode

You can find the Android apk of AM2R with the 3:2 mod pre-applied on archive.org. I cannot link it here, but "someone" will have uploaded it, surely, by the time you are reading this README. Try searching "*am2r*" or "*metroid*" or "*apk*" and sort by *Date added*. Maybe you'll find something -- I don't know. If not, well, you'll have to follow the steps below for Manual Creation.

#### ✨ Manual Creation

You'll need to do the below steps in the following order:
* Download [AM2RLauncher](https://github.com/AM2R-Community-Developers/AM2RLauncher)
* Download and install the latest version of [Java](https://www.java.com/download/ie_manual.jsp)
* You will need to source a download of `AM2R_1.1.zip`. It is currently on the same internet archive mentioned above; use your Google-fu to find it. 

- Open *AM2RLauncher*.
- Hit the '**Download**' button, wait for it to finish.
- Hit '**Select AM2R_1.1.zip**' and find the zip you have downloaded from the internet archive.
  * Nothing will "happen" once you hit *Open*, but the button will change to say **Install**.
- Hit the '**Install**' button, wait for it to finish.
- Hit *Mod Settings* in the top navigation bar, should be the one on the furthest right.
- Hit '**Add New Mod**' and find the Windows or Linux -- depending on your OS -- zip from the [Releases](https://github.com/hotcereal/am2r-3-2/releases) page.
- Hit *Play* in the navigation bar (furthest left).
- Make sure the *Current Profile* is the one titled '**3x2 AM2R Bang**'.
- Hit '**Create APK**'.
  * After a short while, an APK named **3x2 AM2R Bang.apk** while be created in the same directory as the *AM2RLauncher.exe*.
 
## ✨ Desktop Installation

If you're playing on a 3:2 monitor or some such, you can just use the [latest release](https://github.com/hotcereal/am2r-3-2/releases#latest) and load it into *AM2RLauncher* following the steps for loading the mod above. After that, you're set. 

 
## ✨ Finishing Up

If you're using PortMaster on the RG34XX like I imagine all of you are, you'll need to take the resulting apk from the steps above and place it inside of your `AM2R\gamedata` folder, probably inside of your `ports` folder on the microSD card you are using, and rename it so its entire filename is `am2r.apk`. 

As an example, here is where the file would go if you're using MUOS.

<img width="895" alt="Screenshot 2025-01-15 at 1 36 23 AM" src="https://github.com/user-attachments/assets/507d2ba3-62d2-41c7-9d9b-6b524a0f7636" />

## ✨ Game Settings

Once you're in the game, be sure to visit Options > Display Options and sure the below entries are set...as shown below.

* **Fullscreen**: Enabled
* **Display Scale**: 2x
* **Widescreen**: Enabled

### ✨ 2x (480 x 320) & 4x (960 x 640)  GBA Resolution Devices

If you're on a device that supports 2x GBA resolution (PowKiddy V10, Anbernic RG351M, RG351P) or 4x like the AYANEO Pocket Micro, you will have to do a little bit more, with a little less precision. 

In your `AM2R` folder that's created once you install and run the game, you'll have a file called `config.ini` resting inside the `ports\am2r\conf\am2r` folder and within it, you will see a line like below.

<img width="470" alt="Screenshot 2025-01-15 at 1 44 40 AM" src="https://github.com/user-attachments/assets/eadb1c5c-96a8-4506-8ccf-a50aafa8f1d3" />

Be sure that you've opened the game and set the Game Settings listed above. If you have, your scale line will look like so:

  ```Scale="2.000000"``` 

  You will want to change this line to 

  ```Scale="1.333333"```

  ####   💫 AYANEO Pocket Micro Users

  You guys will need to set your scale property to 

  ```Scale="2.666667"```

  This will then give you 3:2 at your resolution. If you don't change the scale or rely solely on the Game Settings from within the game and not the `config.ini`, you may have a view that is either too big or too small. Editing the config after setting the settings, will give you a perfect scaled 3:2 output.
  
  A lil fuss, but nothing crazy. You can make small edits like this using the on-device Dingux Commander app or whichever File Browser you choose that supports minor text editing. 


### ✨ Potential Problems

While building this for release, I had numerous problems attempting to build the base apk on Windows due to decompilation errors. If you are tech savvy enough, or if you have a spare PC lying around, I found that using Linux for everything was seemless. I have included a Linux version of the initial release for those of you willing to venture into the depths of unix.

Also, as far as issues and problems go, I genuinely cannot assist much. I learned about AM2R decompilers, utilities, mods, and patches within the last 24 hours and dedicated a solid 200% of my time toards getting the game to run at 3:2 with little to no issues. I would recommend, if anywhere, the [AM2R Discord](https://discord.gg/YTQnkAJ). Join and ask for help there; they are helpful and there is a treasure trove of information just sitting in their chat logs.

## 😄 Thank You

Firstly, thank you to all of you for downloading and enjoying this aspect ratio mod. As a huge Metroid fan, being able to play three of the five games in 3:2 on a device that looks smack like a GBA is something out of a fable. 

But most importantly, I genuinely want to thank everyone who worked on the projects linked above. I would list them all, but it would arguably rival the Bible in length. Again, though, I do want to say thank you to [@Rex109](https://www.github.com/Rex109) for being so open to helping and assisting me in figuring out what things needed edits, and what things I should compare and contrast against. It set me on the right path, and without their help, this mod would absolutely not be possible.

Thank you. 

-🔥🥣


