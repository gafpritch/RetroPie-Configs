# Xin-Mo 2 Player Fix

The Xin-Mo (and newer Xinmotek) have an issue when used with RetroPie on a Raspberry Pi ... Despite being a two player interface intended to be seen by the Pi as two separate USB controllers, "out of the box" it's not seen as such.  To fix this problem, append the **/boot/cmdline.txt** file of your RetroPie install with the following ...

**usbhid.quirks=0x16c0:0x05e1:0x040**

Make sure you add a space at the end of the existing entry, so it's all one line once the above has been added.  Save the file and reboot the Pi for the changes to take effect.  Check the **/dev/input** directory to see the two joypad entries and use **jstest** to confirm is necessary. 
