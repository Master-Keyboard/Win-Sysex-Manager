# WIN SYSEX MANAGER
Version 2.00 · by GBC Masterkeyboard

WIN SYSEX MANAGER is a Windows program to store, edit, send and receive MIDI System Exclusive (SysEx) messages. It uses the standard Windows MIDI drivers, so any MIDI interface or instrument that Windows can see can be used. No installation is needed.

![Main window](screenshots/01%20Main.jpg)


![Main window](screenshots/02%20Send%20by%20group.jpg)


![Main window](screenshots/03%20Send%20by%20type.jpg)


MAIN FEATURES

List of SysEx rows with name, group, type, delay and MIDI output (Sub MIDI Out) for each row, with a green/red LED showing whether the port is available.
Hexadecimal editor, load and save of `.syx` files, Copy / Paste buttons and right-click menu in the text boxes
Send by Group and Send by Order windows.

Dump Request (RQ1) list and Receive window. A request can have up to three variable bytes (D1, D2, D3) with minimum, maximum and step, with the checksum calculated at every send, and an Auto all range cycle that asks for all the combinations in sequence.

A Note for every row (button after the name, the text is shown when the mouse stops over it).

Marks, a right-click menu to duplicate, copy and paste rows, and a number on every row.

Export and import of rows between projects (File menu), with their group and type.

Filter to show only some rows of the main window (by text, group or type) or to sort them by name.

Hex Table (decimal / hexadecimal, 0-127).

Checksum calculator (Roland, Yamaha and custom formulas).

One project file (`.wsm`) with all the SysEx data inside.

Black, grey or white background; English or Italian interface; window scale from 100% to 80%.


Download

Download the latest zip from the Releases page of this repository. It contains:
File	Description;
`WIN_SYSEX_MANAGER_V2.00.exe`	the program (no installation needed);
`WIN_SYSEX_MANAGER_User_Manual.pdf`	the user manual (English);
`README.txt`	short instructions.


Requirements

Windows 10 or Windows 11. 
A MIDI interface or instrument with a Windows driver.
Close other MIDI programs that use the same port: many Windows MIDI drivers allow only one program per port
How to start
Unzip the files into a normal folder of your own, for example `C:\Tools\WinSysexManager`, or anothher partiotion. Do not use `C:\Program Files` or other folders protected by Windows (see Settings file below). Avoid the Desktop.
Double-click `WIN_SYSEX_MANAGER.exe`.
Choose your MIDI Output Default (and MIDI Input Default if you want to receive data). The LED next to each menu turns green when the port is available.
Click Load or Edit on a row to put a SysEx in it, then click Send.
To remove the program, delete its folder.
Windows warning ("Windows protected your PC")
The program is not digitally signed, so Windows SmartScreen may show a warning the first time you run it. Click More info, then Run anyway. Some antivirus programs may also report a false alarm on programs of this kind.
You can check that your download is the original file by comparing the SHA-256 value of the zip with the one published in the release notes:
```
certutil -hashfile Win_Sysex_Manager_V2.00.exe SHA256
```
Settings file
The settings (background, language, scale, MIDI ports, last project, last folder and checksum formats) are saved in a file called `config.json`, created in the same folder as the program. To use the same settings on another PC, copy the program and `config.json` together.
If you move or rename the folder of the program, move `config.json` with it: without it the program starts again with the default settings, and the last project and last folder are forgotten, so open your `.wsm` file again. If the program cannot write in its folder, it saves the settings in `%APPDATA%\WinSysexManager` and tells you once.
Your SysEx data is not in `config.json`: it is in the project files (`.wsm`) that you save with File > Save.
Project files and versions
Projects saved by earlier versions open in V 2.00 without problems (notes empty, dump requests without variables). V 2.00 saves projects in a new format (number 2) that contains the notes and the variables: versions 1.00 and 1.10 refuse to open it and tell you to update the program, without changing the file. Keep a copy of your projects before using an older version.
Important notice
The author accepts no responsibility for the integrity of your data. SysEx messages, device settings and saved project files are used at your own risk. Always keep backups.
This program is free to use, but all rights are reserved.

Do you like this app?
Donate with PayPal: https://paypal.me/masterkeyboard/5
