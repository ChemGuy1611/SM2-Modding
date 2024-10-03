# SM2-Modding
Tools and instruction for how to mod Space Marine 2

**THESE INSTRUCTIONS ARE FOR LEGITIMATE MODDING PURPOSES ONLY. DO NOT USE THIS TO MAKE CHEATS FOR THE GAME. YOU ARE LIKELY TO BE REPORTED AND BANNED.**

**Check out my mods on Nexus Mods!**

[Space Marine 2 Vortex Extension](https://www.nexusmods.com/site/mods/961)

[Anti-Stutter for Space Marine 2](https://www.nexusmods.com/warhammer40000spacemarine2/mods/1)

[Disable Screen FX](https://www.nexusmods.com/warhammer40000spacemarine2/mods/29)

[Simple Armor Unlocker](https://www.nexusmods.com/warhammer40000spacemarine2/mods/61?tab=posts)


**INSTRUCTIONS**

First tool you need is [ImHex](https://github.com/WerWolv/ImHex). This allows you to make direct hexidecimal edits to Space Marine 2 pak files. 

When modding these files, you need to make sure that the byte size of the pak ends up being exactly the same as the original, with all files inside having the same size and CRC-32 value as well. This is easier than it sounds.


Steps:
1. Look through the pak files and find something you want to change. Easiest would be a value like a RGB color or some other numerical value.
2. Extract the pak file with WinRAR or 7-zip to get the loose files.
3. Edit the file with the changes you want in a text editor.
4. Check the byte size of the file. If you added or removed characters when making your edits, the file needs to be balanced out to reach the same final byte count. 
5. If you need to add bytes to your file to make the size match, add a "//" comment to the end of the file and insert characters until you get the right size (each normal character is 1 byte).
6. If you need to remove bytes to make your size match, try to remove text that was already inside a comment (//) or whitespace.
7. Now, using ImHex, open both the original pak file and the text file(s) you modified.
8. You need to locate the byte address for the file to be changed. You can search the file name to find it.
9. Once you find the file, find the other end of the file. You can create a Bookmark to make it easy to find this later.
10. Select all the bytes for that file.
11. In the text file you modified, select all bytes and Copy them.
12. Back in the pak file, use the "Fill" function to fill in the selected section (the file) with the bytes from the new file.
13. Save your pak and install to the game!

These instructions are a bit brief right now, but will be fleshed out as I set aside time to improve them.


