# Arma Scheduler

Created for the Taskforce47 Community (see: taskforce47.com)
[![alt text](https://taskforce47.com/images/2019/01/20/tf47.png)](taskforce47.com) 

Arma Scheduler is an easy to use RCON scheduler
It features:
  - Schedule setup via json
  - RCON commands
  - Server start, stop and restarts
  - Auto server restart on crash
  - more to come

### How to use
run the ArmaScheduler.exe application. On your first start an settings.json will be automaticly generated and placed on the desktop for you.
ArmaScheduler will always try to read the settings file from the desktop at the moment.

### Json settings

settings:
| Item | Description |
|----------- |------------|
| *ip* | IP Adress RCON is reachable |
| *port* | Port RCON is reachable |
| *password* | RCON passowrd |
| *repeat* | How many times the programm will try to reconnect to the server via RCON before terminating |
| *timeout* | `not used atm` |
| *hcCount* | amount of headless clients the application is gonna start with the normal gameserver|
| *serverExecutable* | path to server exectuable. Normally it looks like D:\Arma3\arma3_server64bit.exe|
| *hcParameter*| headless client launch arguments |
| *serverParameter* | server launch arguments |

Example setup:
```
{
	"settings": {
		"ip": "127.0.0.1",
		"port": 2307,
		"password": "myfancyrcon",
		"repeat": 100,
		"timeout": 100,
		"hcCount": 3,
		"serverExecutable": "D:\\arma3\\arma3server_x64.exe",
		"hcParameter": "-client -connect=127.0.0.1 -port=2302",
		"serverParameter": "-port=2302 -config=D:\\Arma3\\TADST\\TF47\\TADST_config.cfg -cfg=D:\\Arma3\\TADST\\TF47\\TADST_basic.cfg -profiles=D:\\Arma3\\TADST\\TF47 -name=TF47-GM -filePatching -mod=gm;@ace;@ADV__ACE_CPR;@CBA_A3;@Task_Force_Arrowhead_Radio_BETA__;-autoInit -enableHT -servermod=@TCL;@InterceptDB"
	},
	"scheduledTasks": [
		{
			"time": "01:00:00",
			"rconCommand": "say -1 Server restart in 1 hour.",
			"executeTask": 0
		},
		{
			"time": "01:30:00",
			"rconCommand": "say -1 Server restart in 30 minutes.",
			"executeTask": 0
		},
		{
			"time": "01:50:00",
			"rconCommand": "say -1 Server restart in 10 minutes. Please bring all vehicles back to base. Bitte bringt alle Fahrzeuge zurück zur Basis.",
			"executeTask": 0
		},
		{
			"time": "02:00:00",
			"rconCommand": "say -1 RESTART!",
			"executeTask": 1
		},
		{
			"time": "07:00:00",
			"rconCommand": "say -1 Server restart in 1 hour.",
			"executeTask": 0
		},
		{
			"time": "07:30:00",
			"rconCommand": "say -1 Server restart in 30 minutes.",
			"executeTask": 0
		},
		{
			"time": "07:50:00",
			"rconCommand": "say -1 Server restart in 10 minutes. Please bring all vehicles back to base. Bitte bringt alle Fahrzeuge zurück zur Basis.",
			"executeTask": 0
		},
		{
			"time": "08:00:00",
			"rconCommand": "say -1 RESTART!",
			"executeTask": 1
		},
		{
			"time": "13:00:00",
			"rconCommand": "say -1 Server restart in 1 hour.",
			"executeTask": 0
		},
		{
			"time": "13:30:00",
			"rconCommand": "say -1 Server restart in 30 minutes.",
			"executeTask": 0
		},
		{
			"time": "13:50:00",
			"rconCommand": "say -1 Server restart in 10 minutes. Please bring all vehicles back to base. Bitte bringt alle Fahrzeuge zurück zur Basis.",
			"executeTask": 0
		},
		{
			"time": "14:00:00",
			"rconCommand": "say -1 RESTART!",
			"executeTask": 1
		},
		{
			"time": "19:00:00",
			"rconCommand": "say -1 Server restart in 1 hour.",
			"executeTask": 0
		},
		{
			"time": "19:30:00",
			"rconCommand": "say -1 Server restart in 30 minutes.",
			"executeTask": 0
		},
		{
			"time": "19:50:00",
			"rconCommand": "say -1 Server restart in 10 minutes. Please bring all vehicles back to base. Bitte bringt alle Fahrzeuge zurück zur Basis.",
			"executeTask": 0
		},
		{
			"time": "20:00:00",
			"rconCommand": "say -1 RESTART!",
			"executeTask": 1
		}
	],
	"repeatingServices": [
		{
			"startupDelay": 0,
			"repeating": -1,
			"delay": 1500,
			"rconCommand": "say -1 Restart times: [02:00, 08:00, 14:00, 20:00]",
			"executeTask": 0
		},
		{
			"startupDelay": 2,
			"repeating": 1,
			"delay": 1600,
			"rconCommand": "#say -1 Schaut auch auf unserer Website und im Forum vorbei, unter taskforce47.com / forum.taskforce47.com",
			"executeTask": 0
		}
	]
}
```


### Tech

you will need an .NetFramework 4.6 or newer installed on your server to run this software.
It could be made ready for .NetCore but i leave this up to you fellow readers.


### Installation

Dillinger requires [.Net Framework v.4.6.1](https://dotnet.microsoft.com/download/thank-you/net462) or higher to run.

### Build

Just load the project in visual studio 2017 or higher and build it yourself!

License
----
MIT
