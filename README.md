# WoW-Tools-PyPort 
This version is formally know as version 5. This is a python port of the previous version of WoW-Tools

This version uses Python for the front-end to create some nicer looking terminals to interact with. The backend is still powered by batch scripts just to ensure no problems with permission issues. Due to this being created with Python you will need a version of Python run time, which can be obtained at https://www.python.org/downloads/ . WoWTools is designed to manage AC-Repack World of Warcraft Wrath of the Lich King servers! For further infomation about how to setup or manage your TrinityCore server please visit https://www.trinitycore.org/ .

### Patch Notes

- Created a dedicated installer to automate installs
- Removed unusable functions, for now 😉
- Fixed the problem where the installer would't apply the drive letter specficied to the config script

### Future Features

- Automated start menu shortcut
- User account management
- Database management

## Script Setup

**Your WoW server files has to be on the C: drive.** This is a requirment of the actual server itself, not wowTools. If you really wanted wowTools could be install on any drive you want.

1 - Download the latest version of the installer from the released tab. 

2 - Unzip your download and run install.bat

3 - Enter the directory you want the scripts to be installed to, for example if you wanted it to be in the root of your C: drive you would put C:\

4 - It will ask you to enter a SERVERDIR value. This is the actual folder your WOW server is in. This is the folder that contains the following folders: "Core" "_Server" "Extras".
   Your directory may be something like C:\WoWServer . **This is case sensitive. If your folder contains spaces please put quotations around the folder to prevent errors**

5 - Next, you will be asked for a DRIVE value. THis is the drive that containes your wow game client. E.G. C:, E:, F: **If you are running a standalone server, you can set it to empty, but function 6 won't work**

6 - The CLIENTDIR value is the actual directory your game is in. E.G. E:\"World of Warcraft WOTLK" or C:\wowgame 
    **Make sure you put the root directory that is the home of the Wow.exe application**

7 - For CLIENTMOUNTPOINT just enter the same value you did for DRIVE value. This setting is just there for compatibility

🥳 You have successfully setup your version of wowTools!!

## What does each function do?

**Option 1 - Start Game Server**

Its pretty obvious, but this opens the following applications
GAMEDIR\_Server\SQL.bat
GAMEDIR\Core\AuthServer.exe
GAMEDIR\Core\Worldserver.exe

**Option 2 - Stop Game Server**

Again quite obvious, but this time is closes these applications
MySQL.bat
AuthServer.exe
WorldServer.exe

**Option 3 - Start SQL Database**

This function is intended if you only want to start the database. Possibly for editing or if it just isn't running. This command will run GAMEDIR\_Server\MySQL.bat

**Option 4 - Start Apache Server**

In the ACWEBPACK version of the server there is a optional web interface that can be accessed when you start the apache server. It broadcasts on localhost at a certain port. 
This command will execute GAMEDIR\_Server\Apache.bat

**Option 5 - Start SQL and Apache**

Just executes both option 4 and option 5 at the same time.

**Option 6 - Open Warcraft Client**

It does what it says on the box, opens your game client. ⚠️ Don't run this command if you do not have the game installed ⚠️

**Option 7 - Release Notes**

This will allow you to read the release notes, just a copy of this github README

**2025 wowTools PyPort - Version 5 // Release 2**
**Created by Lisoft Software Solutions**
