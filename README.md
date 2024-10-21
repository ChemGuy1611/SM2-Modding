# SM2-Modding
Tools and instruction for how to mod Space Marine 2

**THESE INSTRUCTIONS ARE FOR LEGITIMATE MODDING PURPOSES ONLY. DO NOT USE THIS TO MAKE CHEATS FOR THE GAME. YOU WILL BE REPORTED AND BANNED.**

**Check out my mods on Nexus Mods!**

[Space Marine 2 Vortex Extension](https://www.nexusmods.com/site/mods/961)

[Anti-Stutter for Space Marine 2](https://www.nexusmods.com/warhammer40000spacemarine2/mods/1)

[Disable Screen FX](https://www.nexusmods.com/warhammer40000spacemarine2/mods/29)

[Simple Armor Unlocker](https://www.nexusmods.com/warhammer40000spacemarine2/mods/61?tab=posts)


**INSTRUCTIONS**

First tool you need is [ImHex](https://github.com/WerWolv/ImHex). This allows you to make direct hexidecimal edits to Space Marine 2 pak files. 

When modding these files, you need to make sure that the byte size of the pak ends up being exactly the same as the original, with all files inside having the same size and CRC-32 value as well. This is easier than it sounds.


**Steps:**
1. Look through the pak files and find something you want to change. The easiest would be a value like a RGB color or some other numerical value.
2. Extract the pak file with WinRAR or 7-zip to get the loose files.
3. Edit the file(s) with the changes you want in a text editor.
4. Check the byte size of the file by right-clicking on it and selecting "Properties". If you added or removed characters when making your edits, the file needs to be balanced out to reach the same final byte count. 
5. If you need to add bytes to your file to make the size match, add a "//" comment to the end of the file and insert characters until you get the right size (each normal character is 1 byte).
6. If you need to remove bytes to make your size match, try to remove text that was already inside a comment (//) or whitespace.
7. If you want to take the "belt and suspenders" approach, you can also have the file match the original file's CRC-32 using this tool. I personally make my mods this way to make the file as close to the original as possible: [CRC Manipulator](https://github.com/rr-/CRC-manipulator).
8. The size of the modified files must be *EXACTLY* the same as the original, down to the byte.
9. Now, using ImHex, open both the original pak file and the text file(s) you modified. Make a backup of the pak file in case you make a mistake and need to start over.
10. In the pak file, you need to locate the byte address for the contents of the file(s) to be changed. You can "Search" the file name to find it. The starting byte to select is the one just after the file name. Create a Bookmark to make it easy to find this later.
11. **Note -** When looking for the file, make sure you find the actual file contents, not the directory listing. You will know you are looking at the file contents because they have readable text in the ASCII column (for uncompressed files).
12. <img width="560" alt="Snap0176" src="https://github.com/user-attachments/assets/537e6236-de7b-49a2-85b1-ec90f3775521">
13. Now find the end of the file contents. This will be the byte before "PK", which separates the files. Create a Bookmark to make it easy to find this later.
14. <img width="582" alt="Snap0175" src="https://github.com/user-attachments/assets/727fb4d6-5db2-48d3-84a0-f1559a85a8da">
15. Select all the bytes for the file contents. The easiest way to do this is to make a bookmark that starts at the beginning of the file contents (just after the file name) and ends at the byte just before the "PK" separator.
16. In the text file you modified, select all bytes and Copy them.
17. Back in the pak file, use the "Fill" function to fill in the selected section (the file) with the bytes from the text file. Paste the bytes you copied into the dialogue popup.
18. Check the last few bytes of the file contents to make sure they are correct. If bytes are missing, you need to remove some characters from the modified file to get it to fit.
19. Save your pak file.
20. Run the [PackCacher](https://www.nexusmods.com/warhammer40000spacemarine2/mods/65?tab=posts) mod to generate a .cache file for your new .pak file. This should be distributed with your .pak file if you share your mod.
21. Done! Share your file on Nexus Mods so that others can enjoy it too!

These instructions are a bit brief right now, but will be fleshed out as I set aside time to improve them.

If you would like to support my work and the free sharing of modding knowledge, you can do so below. Your support is greatly appreciated!

[Buy Me a Coffee](https://buymeacoffee.com/chemboy1)

[Join My Patreon](https://www.patreon.com/chemboy1)
