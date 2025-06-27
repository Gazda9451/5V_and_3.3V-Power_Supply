# 5V_and_3.3V-Power_Supply
A power supply has wall power as its input and outputs a steady 5V or 3.3V. Power MB V2 is used i.e. AMS1117-5V and AMS1117-3.3V fixed linear regulars are used. A 120V to 24V stepdown transformer is used to initially reduce the voltage. A  12V Zener diode is used to drop down the voltage further so it can be connected to the power MB V2 board. This project was simulated in LTspice. 

Components used:
- Resideo AT72D 1683 - Multi-Mount Control Circuit Transformer (can get at most hardware stores) 
- 4 1N4007 - rectifier diode 
- 4 100 uF 50V - Polarized Capacitor 
- 300 Ohm resistor needs to handle 3.3 W but can use 5 100 ohm 1/2 W resistors, 500 ohms maxes out at 2 W (that's what I did since I have them already). Only problem with doing this is it slows down ramp up of the 5V and 3.3V since the 12V takes more time to ramp up. This outcome can be desirable depending on application 
- 1 BZX84C12L - 12V Zener diode 
- 5 10 uF 50V - Polarized Capacitor 
- 1 Elegoo Power MB V2 

Libraries added to LTspice (I did not create these models so will include the files I got them from) 
- M7 - .model M7 D (Is={5u/40} Bv={1000*1.05} Ibv={5u} Vpk={1000} N={.8*1.1/25m/(ln(1)-ln(5u/40))} Rs={0.05} Eg={1} Xti={3} Iave={1} Cjo={12p*2} M=.33 Tt={1500n} Vp=.5 mfg=Diotec type=Rectifier)
- 1N4007 - .MODEL 1N4007 D  ( IS=76.9p RS=42.0m BV=1.00k IBV=5.00u CJO=26.5p  M=0.333 N=1.45 TT=4.32u mfg= Vishay type= rectifier)

Currently the only part that is missing for full assembly is the 12V Zener Diode as of 6/27/2025. 

