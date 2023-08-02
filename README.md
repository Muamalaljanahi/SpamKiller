# SpamKiller
SpamKiller is a powerful tool designed to protect your TeamTalk server from spam activitiessss
## downloads
[download SpamKiller_Ubuntu_x86_64](https://github.com/Muamalaljanahi/SpamKiller/releases/download/1.1.2/SpamKiller_Ubuntu_x86_64.zip)

[Download SpamKiller latest version for Windows 64 bit](https://github.com/Muamalaljanahi/SpamKiller/releases/download/1.1.2/SpamKiller_v1.1.2_win64.zip)

## SpamKiller Installation Guide

### Windows
1. Unzip the SpamKiller archive and run `SpamKiller.exe`.
2. If it's the first time running SpamKiller, it will prompt you to customize your preferences.

### Linux
1. Unzip the SpamKiller archive and navigate to the directory using the terminal: `cd SpamKiller`.
2. Grant necessary permissions to execute the program: `chmod +x SpamKiller`.
3. Run the program: `./SpamKiller`.
4. If it's the first time running SpamKiller, it will prompt you to configure your preferences.

#### Running SpamKiller as a System Service
1. Navigate to the `systemctl` folder inside the bot folder: `cd systemctl`.
2. Edit the `spamkiller.service` file and update the `WorkingDirectory` and `ExecStart` paths.
   - `WorkingDirectory` should point to the bot's folder.
   - `ExecStart` should point to the executable file.
3. Move the `spamkiller.service` file located inside the bot's folder: `mv spamkiller.service /etc/systemd/system`.
4. Activate the bot to start on system boot: `systemctl enable spamkiller`.
5. Start the bot: `systemctl start spamkiller`.

## what's new
### Version 1.1.2
- Save nickname/status after changing them.
- Bug fix for changing nickname/status on Ubuntu version.
- Bug fix where adding an empty line to the badwords.txt file would result in kicking noname.
- Other minor fixes.

### Version 1.1
- Automatic login after running SpamKiller in order to add it to systemctl.
- After several requests: I am pleased to announce that the program now supports Ubuntu.

- The black list has been removed as we have the most accurate badwords blocking feature ever
- Added the "s" command where you can modify the bot settings from the command prompt, more options will be added later
- You can now add any ip to the exception list, by default "stats" ip address is added
- now you can add/remove public accounts, The bot protects the server from public accounts listed in the config.ini file. such as checking - vpn status etc.
- added badwords
- Added the ability to change bot's name/status
