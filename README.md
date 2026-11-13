# HBFS Robotics Start Stop System Remote

This is a premium remake of the original 
[p1rse](https://github.com/p1rse/robot-sumo-start-module) remote which 
is yet to be designed in KiCAD. 

This project improves upon the original in some few key areas:

- High quality Cherry MX ULP switches with RGB LEDs
- Removes pointing of the remote towards the robot
- High power OSRAM infrared LEDs
- STM32 microcontroller
- Power options ranging from Supercapacitors, Lithium cells and AAA batteries
- Charging via USB-C
- Zero switches, touch to power on, auto power off
- Lighweight and sleek design
- Lanyard compatible

In the style of the original remote, the BOM uses a carefully curated 
list of components that were singlehandedly selected for supply chain 
availability across the world, with one exception. Keycaps. Those remain 
challenging to source.

## Power Sourcing

As shipping batteries is difficult due to airline regulations, this remote 
uses an iPod nano 7th generation replacement battery P/Ns **616-0639** 
or **616-0640** as the preffered power source. At only 1.9mm thick, this 
Li-Ion battery is available in most places for around 20USD, while 
quantity purchases from places closer to manufacturing origins lower the 
cost of each cell down to around 5USD. As you can imagine, the total BOM 
cost of this remote sits way past its original partlist of 11USD with free 
PCBs.

Alternative power sources include Supercapacitors, AAA Batteries, and LiPo 
battery cells with JST PH connectors. These are available from the 
following suppliers:
- Supercapacitor [**ADCM-S05R5SA106RB**](https://octopart.com/part/abracon/ADCM-S05R5SA106RB)
- Adafruit LiPo P/Ns [**1578**](https://www.adafruit.com/product/1578), [**4236**](https://www.adafruit.com/product/4236), [**258**](https://www.adafruit.com/product/258)
- SparkFun LiPo P/Ns [**PRT-13854**](https://www.sparkfun.com/lithium-ion-battery-850mah.html), [**PRT-13851**](https://www.sparkfun.com/lithium-ion-battery-400mah.html)
- Akyga LiPo Cells such as the [**AKY0185**](https://www.tme.eu/en/details/aky-lp503040/rechargeable-batteries/akyga-battery/aky0185/) with wires soldered directly onto pads
- Triple AAA battery holder from Keystone [**2479**](https://www.digikey.com/en/products/detail/keystone-electronics/2479/303824)

The original design used two AA batteries. Since two standard AA batteries 
only sum up to 3V when brand new, there were not enough volts to push the 
infrared emitters very high. There were not enough amps as well, and the 
design used an electrolytic cap to overcome the high internal battery 
resistance limitations.

## Part Numbers

The following part numbers have been designated to each of the constructive 
variants. Contributions are welcome, and if someone finds a better way to 
power this remote, all 3D models are made available in the repo.

| P/N                            | Power Source          | Thickness | Charging | Unit Cost (10-pack) |
|--------------------------------|-----------------------|-----------|----------|---------------------|
| HBFS-STARTSTOP-REMOTE-THIN     | iPod Battery 616-0640 | 4MM       | USB-C    | TBD                 |
| HBFS-STARTSTOP-REMOTE-SUPERCAP | 5.5V Supercapacitor   | 15MM      | USB-C    | TBD                 |
| HBFS-STARTSTOP-REMOTE-JST      | JST PH LiPo Cell      | 8MM-15MM  | USB-C    | TBD                 |
| HBFS-STARTSTOP-REMOTE-LIPO     | Wired LiPo Cell       | 6MM       | USB-C    | TBD                 |
| HBFS-STARTSTOP-REMOTE-AAA      | AAA Batteries or NiMH | 14MM      | Cell     | TBD                 |


## Charging

The charging chip used is the TI's **BQ25170DSGR** featuring low quiescent 
current and up to 800mA of charging current. The current settings have to 
be sized for the appropriate cell used. 


## Contributions

HBFS Robotics contributes in the robotics space by dedicating its work to 
the **public domain**. We find ways.
