# SpamKiller

SpamKiller is a robust tool designed to safeguard your TeamTalk server against spam activities.

## Downloads

- [Download SpamKiller for Ubuntu (x86_64)](https://github.com/Muamalaljanahi/SpamKiller/releases/download/1.1.2/SpamKiller_Ubuntu_x86_64.zip)
- [Download Latest Version of SpamKiller for Windows 64-bit](https://github.com/Muamalaljanahi/SpamKiller/releases/download/1.1.2/SpamKiller_v1.1.2_win64.zip)

## SpamKiller Installation Guide

### Windows

1. Unzip the SpamKiller archive and run `SpamKiller.exe`.
2. Upon the first run, SpamKiller will prompt you to configure your preferences.

### Linux

- Unzip the SpamKiller archive and navigate to the directory using the terminal: 
```
cd SpamKiller
```
- Grant the necessary execution permissions: 
```
chmod +x SpamKiller
```
- Execute the program: 
```
./SpamKiller
```
- If it's your first time using SpamKiller, you'll be guided to set up your preferences.

### Running SpamKiller as a System Service

- Navigate to the `systemctl` folder within the bot directory: 
```
cd systemctl
```
- Edit the `spamkiller.service` file and update the `WorkingDirectory` and `ExecStart` paths:
  - Set `WorkingDirectory` to the directory containing the bot.
  - Set `ExecStart` to point to the executable file.
- Move the `spamkiller.service` file from the bot's directory to `/etc/systemd/system`: 
```
mv spamkiller.service /etc/systemd/system
```
- Enable automatic bot startup on system boot and start it: 
```
systemctl enable spamkiller
systemctl start spamkiller
```

## What's New

### Version 1.1.2

- Save nickname/status after changes.
- Fixed issue with changing nickname/status on Ubuntu version.
- Addressed bug where adding an empty line to `badwords.txt` would result in unintended kicks.
- Various other minor bug fixes.

### Version 1.1

- Added automatic login after running SpamKiller to enable adding it to systemctl.
- Ubuntu support
- Removed the black list as the new badwords blocking feature is more accurate.
- Introduced the "s" command to modify bot settings via the command prompt, with plans for more options in the future.
- Added flexibility to include IP addresses in the exception list; "stats" IP address is included by default.
- Implemented the ability to add/remove public accounts, protecting the server from public accounts listed in the `config.ini` file and performing tasks like VPN status checks.
- Introduced badwords feature.
- Enabled changing the bot's name/status.
