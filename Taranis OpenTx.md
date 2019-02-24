### This is a guide/status for the taranis x9d+ radio using openTx 2.2.3
-----------------------------------------------------------------------
There are many ways to connected up openlrs hardware, this guid focus on using openTx and a taranis x9d+ radio, much of the information can be used across different equipment. The current wiki has significant information but setup for this radio and openlrs has a lot of different information available. 

My primary setup is a taranis x9d+ and orangerx 1 watt tx module.

I would like to acomplish these goals with this wiki page, to compile the rcgroups forum (650+ pages 9000+ post) into a easier to use guide to setups that work. 

I would like to have 16 channels out and frskyX telemetry coming back from sensors and flight controllers)

1. list of features and limitations of each feature
1. Setup of each feature as it pertains to an x9d+



OrangeRx 1 Watt Jr Module

Feature | Working Functions | Not working | Notes
-------- | ------------------ | ---------------- | --------------
PPM      |                [x] |                  | Not sure how serial passthrough functions, assume this is good.
SBUS     |                [x] |                  | Taranis has an option to use non-inverted sbus (taranis ppm pin must be attached to module rx pin)
Multi    |                [x] |                  | opentx 2.2.3, no inveter required.
Serial Passthrough |      [x] |                  | Adrupilot telemetry link or other serial, amount of data is limited by openlrs serial air baudrate

On two way links there are limitations, sometimes selecting a "type" of telemetry changes the baudrate on devices. i.e. normal frskyD telemetry is 9600, Nomral sport FrskyX telemetry is 100,000 8E2
PPM --> TX  ---> Air ---> RX ---> Reciever PPM pin
9600 FrskyD <-- TX <--- AIR <--- RX <--- 9600 FrskyD to Receiver RX pin

SBUS --> TX  ---> Air ---> RX ---> Reciever PPM pin
100,000 8E2 FrskyD or FrskyX? <-- TX <--- AIR <--- RX <--- sport to Receiver RX pin

Multi --> TX  ---> Air ---> RX ---> Reciever PPM pin
100,000 8E2 FrskyD or FrskyX <-- TX <--- AIR <--- RX <--- 100,000 8E2 sport or FrskyD to Receiver RX pin



Hardware | Working Functions |In Progress | Not working
-------- | ------------------ | ---------------- | --------------
Orange 1watt Jr Module | PPM <Br/> Sbus <Br/> Multi <Br/> Serial Passthrough | Content from<Br/> cell 2  | Content from cell 2
OrangeRX receiver | PPM <Br/> PWM <Br/> Sbus <Br/> Serial Passthrough | Content in the second column| Content in the second column

#### Working functions
[x] PPM 
[x] Sbus
[x] Multi
[] sumd - untested


#### Broken items
Telemetry


### Limitations of serial protocols
Selecting a serial protocal locks the transmitter to the speed of the serial protocal i.e. SBUS is 100000, 8E2
The output becomes set at this.

Multi protocal is setup to receive telemetry at the same rate as output, 
[ ] (others like sbus are expecting telemetry at a different rate?)



### Taranis settings
External module set to:
PPM   - set number of channels
Sbus  - option inverted output
Sbus  - option non- inverted output
Multi - option OpenLRS

### OpenLrsng Configurator Setttings
Tx page

Rx page
-Nothing yet, using pwm to test
-might need some more telemetry items to work



# Just for referenece when writing md file.

## xxxxx2
### xxxxx3
### xxxxxxx3
Click on `xxx` > `xxxxxx`
* xxx
![](./images/vscode_view_command_palette.png)

xx `xx`

![](./images/vscode_install_extensions.png)
## Usage
### 1. Open the OpenLRSng folder
xx `xx` > `xx`

 <nowiki>SDA-SDA
 SCL-SCL
 GND-GND
 VCC-VCC or 5V-5V</nowiki>   //grey area
 
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

~~CrossedOut~~

*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_
# This is an <h1> tag
## This is an <h2> tag
###### This is an <h6> tag

xxxxxxxxxxxxxxxxxxxxxxxxx
=========================
xxxx
xxxx

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
------------------------------------------------

