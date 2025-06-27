# 5V_and_3.3V-Power_Supply
A power supply has wall power as its input and outputs a steady 5V or 3.3V. Power MB V2 is used i.e. AMS1117-5V and AMS1117-3.3V fixed linear regulars are used. A 120V to 24V stepdown transformer is used to initially reduce the voltage. A  12V Zener diode is used to drop down the voltage further so it can be connected to the power MB V2 board. 

Components used:
Resideo AT72D 1683 - Multi-Mount Control Circuit Transformer (can get at most hardware stores) 
4 1N4007 - rectifier diode 
4 100 uF 50V - Polarized Capacitor 
300 Ohm resistor needs to handle 3.3 W but can use 5 100 ohm 1/2 W resistors (that's what I did since I have them already). Only problem with doing this is it slows down ramp up of the 5V and 3.3V since the 12V takes more time to ramp up. This outcome can be desirable depending on application 
1 BZX84C12L - 12V Zener diode 
5 10 uF 50V - Polarized Capacitor 
1 Elegoo Power MB V2 

Currently only part that is missing for full assembly is the 12V Zener Diode as 6/27/2025
