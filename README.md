# GM.Rainmeter
My Rainmeter skins. They are based on the [Zepha Skin V2](https://ani07789.deviantart.com/art/Zepha-Skin-V2-Rainmeter-328013162).

[![Release](https://img.shields.io/github/release/GregaMohorko/Rainmeter.svg?style=flat-square)](https://github.com/GregaMohorko/Rainmeter/releases/latest)

## Preview
![Desktop preview](/Screenshots/Screenshot%20Desktop.png?raw=true "Desktop preview")

## GM.Main
The main skin with all the main elements. It is always positioned at the horizontal center of the screen.

![Main skin](/Screenshots/Screenshot%20Main.png?raw=true "Main skin")

Variations:
- 8 CPU cores, 2 disk drives
- 4 CPU cores, 2 disk drives

## GM.Trash
![Trash skin](/Screenshots/Screenshot%20Trash.png?raw=true "Trash skin")

## Installation
[Instructions for installation (Rainmeter docs)](https://docs.rainmeter.net/manual/installing-skins/#InstallManually)

#### If you have User Account Control (UAC) enabled, then the SpeedFan will not automatically start on Windows start up, because it needs elevated privileges. The solution is to create a task that runs on start up and starts the SpeedFan program with elevated privileges. Here are the steps to configure the task:
- Open up Task Scheduler
- Click on 'Create Task...'
- General:
  - Run only when user is logged on
  - Run with highest privileges
- Triggers:
  - Click on 'New...':
    - Begin the task: 'At log on'
    - Any user
    - Delay task for: 30 seconds
    - Enabled
- Actions:
  - Click on 'New...':
    - Action: 'Start a program'
    - Program/script: cmd.exe
    - Add arguments: /c start "SpeedFan Elevated" "[path to the speedfan.exe]"
- Conditions:
  - None
- Settings:
  - Allow task to be run on demand
  - If the task fails, restart every: 10 minutes
  - If the task is already running, then the following rule applies: 'Do not start a new instance'
- OK

## Author and License
Gregor Mohorko ([www.mohorko.info](https://www.mohorko.info))

Copyright (c) 2022 Gregor Mohorko

[MIT License](./LICENSE)
