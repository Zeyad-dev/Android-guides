# Prerequisites:
* Make sure you take a full backup of your phone since this process will cause a complete wipe of data on the phone
* Make sure your phone is not intended for use in US or Canada since these phones can't unlock their bootloaders, making them impossible to root.
* You will require a computer for this process.
* Make a note of your key combo to enter **Download Mode**. You can get that from a google search (`how to enter download mode on (device model)`)
* Make sure that your bootloader is unlocked. The unlock process will **wipe your data**, so make sure you have already taken a backup. To unlock the bootloader:
  - Go to Settings > About Phone > Software information > and Keep tapping `Build number` (typically 7 times) till you get a text underneath saying `You are now a developer!`
  - Go back to settings and at the very bottom you should see a new settings category; `Developer Options`. Press it and find `Allow OEM unlocking` and toggle it.
  - Next is you want to go to download mode. To do so, shutdown your phone and then when the screen goes blank, connect your phone to a USB c cable (to a computer) and keep holding down your **Download mode key combo** till a blue screen appears.
  - If you see a warning that says `A custom OS can cause critical problems.....` press vol up once. If you don't see such warning, go to the next step.
  - You should see a message asking to `Unlock the bootloader`, with two options, to unlock the bootloader, hold the combo key it asks for to unlock. `Usually it's pressing vol up once`
  - Congrats. Your bootloader is unlocked and you can now root your phone.
 
# Necessary files to download:
* [Odin](https://odindownload.com/download/Odin3_v3.14.4.zip) (Download on computer)
* [Magisk](https://github.com/topjohnwu/Magisk/releases/tag/v26.4) (Download the file ending with `.apk` on the device)
* [Frija tool](https://github.com/SlackingVeteran/frija/releases/download/v2.0.23262.4/Frija_v2.0.23262.4.zip) (Download on computer)
  ### Important Notice:
  * Frija tool might throw an error saying: `To run this application, you must install .NET.`

### Necessary information to know about your device:
* Your device's codename : Can be retrieved from Settings > About Phone > Model Number
* Your device's CSC code (region): Can be retrieved from Settings > About Phone > Software information > Service provider SW ver. If for example your's is:
`SAOMC_SM-0980F_OXM_TPA_00_0006`
Then your CSC code will be the third word after the two `_` (which in this case is `OXM`)

### Step 1 : Get the stock firmware
* You will require a computer for this step.
* Extract the zip file of [Frija tool](https://github.com/SlackingVeteran/frija/releases/download/v2.0.23262.4/Frija_v2.0.23262.4.zip) and run the exe in the folder extracted.
*  You should see 2 textboxes at the left of the screen, in the first one, enter your phone's model (the codename you previously got.
* In the second one, enter your CSC code (region).
* Let it load the firmware then press download to start downloading the file.
* Expect it to take some time since the full firmware can reach upto 8 gb of size.
