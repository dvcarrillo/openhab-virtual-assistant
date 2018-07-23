# Google AIY Voice Kit applied to openHAB 2
This script is an adaptation of the ones that come with the 
[Google AIY Voice Kit](https://aiyprojects.withgoogle.com/voice/), including custom commands
that can be sent to openHAB 2, so you can manage your smart home directly from your Voice Kit.

This example is **made over a system with a Philips Hue color bulb** and makes use of the openHAB
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

## Commands
Apart from the actions that Google Assistant can perform, the script can send the following actions
to openHAB. Please see in the code the words that can trigger each command. 

- For all the lights (through a group item):
  - Turn on and off
- For each light:
  - Turn on and off
  - Change the light color
  - Change the light color temperature
  - Increase and decrease its brightness
- For the system (Raspberry Pi):
  - Turn off
  - Reboot

## Languages
The assistant only recognizes English. However, it is possible to make it answer in other languages.
Change the language code in `aiy.i18n.set_language_code('en-GB')` to the one you prefer and also 
please remember to change the answers to that language!

## Installation
Please note that this script is **only supported in Raspberry Pi 2 and 3**.

Clone this repo into your Voice Kit, configure it (take a look at `CONFIGURATION` inside the code)
and execute this script with Python 3. Follow the instructions on screen and enjoy!

## 
*This work is part of my BSc End Project (TFG) about the creation of a voice-driven controller
for home automation on Raspberry Pi.*
