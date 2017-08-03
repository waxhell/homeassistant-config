# homeassistant-config

My Example [Home Assistant](https://home-assistant.io/) Config

## Devices: 

### Base Setup:

* Home Assistant Version 0.50.1
* Virtualenv Install
* Running on Pogoplug_E02
* Arch Linux ARM (ARMv5te)
* Sigma Designs UZB Z-Wave USB Adapter

### Amazon Echo Dot:

* Integrated via the emulated_hue component (i.e Alexa, Turn on Dining Room Ceiling Fan)
* Also running [Pizzaface/Alexa-Chromecast-Skill2.0](https://github.com/Pizzaface/Alexa-Chromecast-Skill-2.0) (i.e. Alexa, Tell Chromecast to play [Youtube Video])
* Additional [scripting](https://community.home-assistant.io/t/simple-script-to-enable-amazon-echo-alexa-to-set-the-temperature-on-a-climate-thermostat-device-via-the-emulated-hue-component/7924/10) to handle thermostat with emulated_hue (i.e. Alexa, Set AC to 68)

### Living Room Entertainment Center Setup:

I have the Living Room setup wrapped together via the media_player.custom component. This combines the Pioneer receiver and the Chromecast together into a single component (Living Room TV).

* Monster Cable HDP 850G Green Power Surge Protector - Automatically controls Switched outlets based on Master Controlled Outlet status
* Pioneer SC-1522k AVR - Controlled via the media_player.pioneer component & Connected to Master Control Outlet on Surge Protector
* LG Non-Smart TV - Plugged into Switched Outlet; Automatically turns on when AVR is powered up and turns off when the AVR is powered down.
* Chromecast (2nd Generation) - Living Room Chromecast

### Automations:

#### Lighting Automation
* Evening Outside Lights On - Turn on all outdoor lights when sun elevation is below 1.5 
* Midnight Balcony Lights Off - Turn off outdoor balcony lights at midnight 
* Sunrise Outside Lights Off - Turn off all outdoor lights when sun rises 
* Morning Lights Off - Turn off all lighting / devices at 10:30AM
* Morning Guest Bedroom Lights Off - Turns off all Guest Bedroom lighting at 10:30AM (seperated for guest convenience)

### Energy Automation:
* Living Room TV Auto Off - Turn off Living Room Entertainment Center when idle for >30 mins (Chromecast Idle & Pioneer AVR On).

### Minimote Integration Automation
* Setup Minimote to control Guest Bedroom Lighting

### Z-Wave Devices:

* Monster IWD 600S (Leviton RZI06-1LX) - 2 Wire Dimmers - 9600 bps - Instant Status Capable
* Monster IWS 1000S (Leviton RZS15-1LX)) - Relay Switch - 9600 bps - Instant Status Capable
* Leviton VRS15-1LZ - Relay Switch - 40000 bps - Instant Status Capable
* GE/Jasco 45606 - 2 Wire Dimmers - 40000 bps
* GE/Jasco 45613 - 3 Way Dimmer Switches - 40000 bps
* GE/Jasco 45603 - Plug In Appliace Modules - 40000 bps
* Aeotec DSC26103 - Micro Switches (Gen2) - 40000 bps - Instant Status Capable
* Cooper RF9505-TR - Receptacles - 40000 bps - Instant Status Capable
* Schlage FE599 - Door Locks - 40000 bps
* Schlage BE369 - Deadbolt Locks - 40000 bps
* Trane TZEMT400AB32MAA - Thermostat - 40000 bps
* First Alert ZCOMBO-G - Smoke & CO Detector - 40000 bps
* Aeotec DSA03202 - Minimote - 40000 bps
