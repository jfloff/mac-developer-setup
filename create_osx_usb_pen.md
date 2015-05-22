# Create OSX Yosemite USB Pen

You have your backup, now you need to put OSX onto a USB Pen drive. At least I'm assuming that you have a a USB port on your Mac.

1. First, go to the App Store and download Yosemite. When the installer pops up the installer, just quit it.
2. Connect to your Mac a 8GB (or larger) drive, and rename the drive SAM - don't judge me. The following Terminal command assumes the drive is named SAM. Also, make sure the Yosemite installer, called `Install OS X Yosemite.app`, is in its default location in your main Applications folder (`/Applications`).
3. Launch Terminal and paste the following command into it. Warning: This step will erase the destination drive or partition, so make sure that it doesn’t contain any valuable data.
```shell
sudo /Applications/Install\ OS\ X\ Yosemite.app/Contents/Resources/createinstallmedia --volume /Volumes/SAM --applicationpath /Applications/Install\ OS\ X\ Yosemite.app --nointeraction```
4. Then the Terminal window displays the progress of the process, in a very Terminal sort of way, by displaying a textual representation of a progress bar: Erasing Disk: 0%... 10 percent...20 percent... and so on. 
5. The program then tells you it’s copying the installer files, making the disk bootable, and copying boot files. Wait until you see the text Copy Complete. Done. This process can take as long as 20 or 30 minutes, depending on how fast your Mac can copy data to your destination drive. It can be a frustating experience since Terminal doesn't provide a lot of input on the status of the process, but just hang on.
6. You now have a bootable Yosemite install drive.
![](http://i.imgur.com/hJwiO.gif)

Onto formatting ... Just restart the computer and press the Option Key (⌥ - ALT) 