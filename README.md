# ESP8266-wifi-light-dimmer
Wifi light dimmer based off of the inexpensive ESP8266 wifi modules.

### Circuit design ###
I'm using a dimming circuit by [diy_bloke] (http://www.instructables.com/id/Arduino-controlled-light-dimmer-The-circuit/step1/Arduino-controlled-light-dimmer-The-PCB/).<br />
Find my [Fritzing](http://fritzing.org/) schematics under the schematics folder.

### Installing ###
1. [Download Arduino-compatible IDE with ESP8266 support] (https://github.com/esp8266/Arduino)
2. Load smartSwitch.ino in IDE
3. Fill in SSID and password
4. Upload to ESP

### Control ###
Browse to IP of ESP. Use GET variables to configure settings:
- s = state (0 or 1)
- b = brightness 
- f = fade (0 or 1)

	ex1: View current settings: http://ip.of.esp/
	ex2: Set brightness to 50% and set state to on: http://ip.of.esp/?s=1&b=128
	ex3: Set brightness to 100% and enable dimming: http://ip.of.esp/?b=255&d=1
	ex4: Toggle state (on->off or off->on): http://ip.of.esp/?s=t
