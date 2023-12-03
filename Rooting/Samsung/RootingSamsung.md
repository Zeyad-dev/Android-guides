# Prerequisites:
* Make sure you take a full backup of your phone since this process will cause a complete wipe of data on the phone
* Make sure your phone is not intended for use in US or Canada since these phones can't unlock their bootloaders, making them impossible to root.
* You will require a computer for this process.
* Make a note of your key combo to enter **Download Mode**. You can get that from a google search (`how to enter download mode on (device model)`)
* Make sure that your bootloader is unlocked. The unlock process will **wipe your data**, so make sure you have already taken a backup. To unlock the bootloader:
  - Go to Settings > About Phone > Software information > and Keep tapping `Build number` (typically 7 times) till you get a text underneath saying `You are now a developer!`
  - Go back to settings and at the very bottom you should see a new settings category; `Developer Options`. Press it and find `Allow OEM unlocking` and toggle it.
     - **IMPORTANT:** If you do not find `Allow OEM unlocking` option, then you're device can't be rooted. This is mainly because the phone **is intended for use in the US or Canada, and these phones are usually (if not always) unable to unlock their bootloaders.
  - Next is you want to go to download mode. To do so, shutdown your phone and then when the screen goes blank, connect your phone to a USB cable (to a computer) and keep holding down your **Download mode key combo** till a blue screen appears.
  - If you see a warning that says `A custom OS can cause critical problems.....` press vol up once. If you don't see such warning, go to the next step.
  - You should see a message asking to `Unlock the bootloader`, with two options, to unlock the bootloader, hold the combo key it asks for to unlock. `Usually it's pressing vol up once`
  - Congrats. Your bootloader is unlocked and you can now root your phone.
 
# Necessary files to download:
* [Odin](https://odindownload.com/download/Odin3_v3.14.4.zip) (Download on computer)
* [Magisk](https://github.com/topjohnwu/Magisk/releases/) (Download the file ending with `.apk` on the device)
* [Frija tool](https://github.com/SlackingVeteran/frija/releases) (Download on computer)

### Necessary information to know about your device:
* Your device's codename : Can be retrieved from Settings > About Phone > Model Number
* Your device's CSC code (region): Can be retrieved from Settings > About Phone > Software information > Service provider SW ver. If for example your's is:
`SAOMC_SM-0980F_OXM_TPA_00_0006`
Then your CSC code will be the third word after the two `_` (which in this case is `OXM`)

### Step 1 : Get the stock firmware
* You will require a computer for this step.
* Extract the zip file of [Frija tool](https://github.com/SlackingVeteran/frija/releases) and run the exe in the folder extracted.
  - If frija asks to download some .net core stuff, then [Download this](https://dotnet.microsoft.com/download/dotnet/thank-you/runtime-desktop-3.1.21-windows-x86-installer). Frija executable requires x86 version of the runtime even on x64 platform so make sure you have the right version installed.
* When the application launches, you should see 2 textboxes at the left of the screen, in the first one, enter your phone's model (the codename you previously got).
* In the second one, enter your CSC code (region).
* Let it load the firmware then press download to start downloading the file.
* Expect it to take some time since the full firmware can reach upto 8 gb of size.

### Step 2 : Patch the firmware with Magisk
* Once frija tool finishes downloading the firmware, extract the compressed file and you should see 5 files, each starting with either `AP`, `BL`, `CP`, `CSC` and `HOME_CSC`.
* Connect your phone with the computer.
* Move the file starting with `AP` from your computer to your phone. (Don't `ctrl+x`, move a copy with `ctrl+c`
* Install the magisk apk that was downloaded earlier on your phone.
* On the home screen, select the first install button (the one inside the box labelled as "Magisk").
* Select the option that says `Select and patch a file` then select the file starting with `AP` (the file you have previously moved from your computer to your phone) then press `Let's go`
* Wait for magisk to finish patching the file, and when it's done, magisk should tell you the path to the newly patched file.
* Move that new patched file (should start with `magisk.....`) to your computer.
* Congrats, we are now half-way through the rooting process.

### Step 3 : Enter download mode on your phone
* To do so, power off your phone and when the screen goes blank, start holding the key combo to enter dlm (Download Mode).
* When it has successfully entered download mode, you should see a blue screen.
* If you encounter a warning screen, typically the one with the text saying: `A custom OS can cause critical problems.....`, press vol up once
* You are now on download mode. Leave your phone connected to your computer for now.

### Step 4 : Flash the rooted firmware to your phone
* Extract [Odin](https://odindownload.com/download/Odin3_v3.14.4.zip) file and run the exe.
* If your phone is detected by odin (It shows at the top something like `0:[COM8]`). Check the below image to see how odin shows if a device is connected or not:

![This image shows how odin should display whether a phone is detected or no](https://forensic.manuals.mobiledit.com/__attachments/1818460206/odin%20(2).PNG?inst-v=6e773f4d-7a7a-40f7-bbe3-7018b31bb210)
  * If it shows, then skip the next additional step. Otherwise:
     - **Additional step:** Download [Samsung's USB Drivers](https://developer.samsung.com/sdp/file/2ad30860-0932-44e3-bf63-765a5cfa1010) and then run it and continue with the setup. If odin still doesn't detect your phone after that, a restart to your computer might be helpful.
* In the 5 options that odin shows (the ones saying `AP`, `BL`, and so on, select the following files in each:
  - In the option `BL`, select the file that frija tool downloaded starting with `BL`
  - In the option `AP`, select the file that magisk patched (the one moved from your phone to computer).
  - In option `CP`: select the file that frija tool downloaded starting with `CP`.
  - In option `CSC`: select the file that frija tool downloaded starting with `CSC` (**DON'T SELECT `HOME_CSC`!**).
  - Skip the option `USERDATA`.
* Once everything is set, press the start button on your computer. This process should take upto 10 mins.

### Step 5 : Complete magisk setup
* After Odin displays the text `PASS!` in green, and the phone has rebooted, you are now free to disconnect your phone from the computer.
* Continue with the initial setup on the phone.
* When it's done, You should see an app on your phone called `Magisk`, delete this app.
   - If you couldn't find the app on your phone, then don't worry, carry on to the next step.
* Install magisk delta apk (Link for it is above) and open it.
* It will ask you for additional setup, just press next and it will reboot your phone.
* When your phone reboots successfully, you have finally rooted your phone. Congrats!
