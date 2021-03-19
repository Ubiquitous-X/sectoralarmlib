Added support for the Sector Alarm smart plugs to the original library written by  [Per-Øyvind Bruun.](https://github.com/peroyvind)

First get the id of your smart plug(s), then send either 'on' or 'off'.

#### Example

``` python
import sectoralarmlib.sector as sector

alarm = sector.SectorAlarm("username", "password", "siteid", "code", "plugid", "on/off")  

# Get smart plug(s) id and status
smartplugs = alarm.GetPlugs()
print(smartplugs)

# Send either on or off to the smart plug
alarm.SwitchPlug()

# Get status of your alarm
status = alarm.AlarmStatus()
print(status)  

# Get temperatures
temps = alarm.GetTemps()
for x, y in temps:
print(x, y)  

# Turn on alarm
alarm.Arm()  

# Turn off alarm
alarm.Disarm() 

```