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
* Also running [Pizzaface/Alexa-Chromecast-Skill2.0](https://github.com/Pizzaface/Alexa-Chromecast-Skill-2.0)

### Living Room Entertainment Center Setup:

I have the Living Room setup wrapped together via the media_player.custom component. This combines the Pioneer receiver and the 
Chromecast together into a single component (with the Pioneer over-riding the volume controls).

* Pioneer SC-1522k AVR - Controlled via the media_player.pioneer component
* Monster Cable Green Power Surge Protector - Receiver is plugged into Master Control Outlet
* LG Non-Smart TV - Plugged into Controlled Outlet; Automatically turns on when AVR is powered up and turns off when the AVR is powered down.
* Chromecast (2nd Generation) - Living Room Chromecast

Since the Chromecast is always on, the Pioneer does not automatically power-down. Automation has been added to automatically power down the Receiver (and TV by association) when idle for >30 minutes.

### Z-Wave:

* Monster IWD 600S (Leviton RZI06-1LX) - 2 Wire Dimmers - 9600 bps - Instant Status Capable
* Monster IWS 1000S (Leviton RZS15-1LX)) - Relay Switch - 9600 bps - Instant Status Capable
* Leviton VRS15-1LZ - Relay Switch - 40000 bps - Instant Status Capable
* GE/Jasco 45606 - 2 Wire Dimmers - 40000 bps
* GE/Jasco 45613 - 3 Way Dimmer Switches - 40000 bps
* Aeotec DSC26103 - Micro Switches (Gen2) - 40000 bps - Instant Status Capable
* Cooper RF9505-TR - Receptacles - 40000 bps - Instant Status Capable
* Schlage FE599 - Door Locks - 40000 bps
* Schlage BE369 - Deadbolt Locks - 40000 bps
* Trane TZEMT400AB32MAA - Thermostat - 40000 bps
* First Alert ZCOMBO-G - Smoke & CO Detector - 40000 bps
* Aeotec DSA03202 - Minimote - 40000 bps
