# GM.Rainmeter
My Rainmeter skins. They are based on the [Zepha Skin V2](https://ani07789.deviantart.com/art/Zepha-Skin-V2-Rainmeter-328013162).

[![Release](https://img.shields.io/github/release/GregaMohorko/Rainmeter.svg?style=flat-square)](https://github.com/GregaMohorko/Rainmeter/releases/latest)

## Preview
![Desktop preview](/Screenshots/Screenshot%20Desktop.png?raw=true "Desktop preview")

## GM.Main
The main skin with all the main elements. It is always positioned at the horizontal center of the screen.

![Main skin](/Screenshots/Screenshot%20Main.png?raw=true "Main skin")

It is designed for computers with 4 CPU cores and 2 disk drives.

## GM.Trash
![Trash skin](/Screenshots/Screenshot%20Trash.png?raw=true "Trash skin")

## Installation
[Instructions for installation (Rainmeter docs)](https://docs.rainmeter.net/manual/installing-skins/#InstallManually)

### Additional recommended settings
#### Sometimes the disk usage meter starts showing wrong percentages. The solution is to refresh the skin. Here are the steps to configure a task scheduled to refresh it once per hour:
- Open up Task Scheduler
- Click on 'Create Task...'
- General:
  - Run only when user is logged on
- Triggers:
  - Click on 'New...':
    - Begin the task: 'On a schedule'
    - Daily
    - Repeat task every: 1 hour; for a duration of: Indefinitely
    - Enabled
- Actions:
  - Click on 'New...':
    - Action: 'Start a program'
    - Program/script: [path to the Rainmeter.exe]
    - Add arguments: !Refresh "GM"
- Conditions:
  - Start the task only if the computer is on AC power
- Settings:
  - Allow task to be run on demand
  - Run task as soon as possible after a scheduled start is missed
  - Stop the task if it runs longer than: 1 hour
  - If the running task does not end when requested, force it to stop
  - If the task is already running, then the following rule applies: 'Do not start a new instance'
- OK

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
Grega Mohorko ([www.mohorko.info](https://www.mohorko.info))

Copyright (c) 2018 Grega Mohorko

[MIT License](./LICENSE)
