# Google AIY Voice Kit and openHAB 2
This script is an adaptation of the ones that come with the 
[Google AIY Voice Kit](https://aiyprojects.withgoogle.com/voice/), including custom commands
that can be sent to openHAB 2, so you can manage your smart home directly from your Voice Kit.

This example is made over a system with a Philips Hue color bulb and makes use of the openHAB
REST API. Adding more Hue lights is as easy as specifying their Items at the Configuration part
of the script. If you would like to add more devices, it is possible by adding new rules,
following the structure of the current script.

## How it works
The assistant can direct your commands to Google Assistant or to openHAB. To direct a command to
openHAB, say the hotword first (by default, *home*) and then your command. For example:
- This command will be directed to the Google Assistant:
> OK Google, what's the weather like today in Granada?
- And this command, to openHAB:
> OK Google, home, turn on all the lights.

This script **can trigger the assistant by saying *OK Google* or by pressing the button of the
Voice Kit**.

## Installation
Clone this repo into your Voice Kit, configure it (take a look at `CONFIGURATION` inside the code)
and execute this script with Python 3. You will be ready to speak to the assistant.

## Languages
The assistant only recognizes English. However, it is possible to make it answer in other languages.
Change the language code in `aiy.i18n.set_language_code('en-GB')` to the one you prefer and also 
please remember to change the answers to that language!

*This work is part of my BSc End Project (TFG) about the creation of a voice-driven controller
for home automation on Raspberry Pi*
