![Intro-GIF](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-GIF.gif) 

# SlimeVR-CheeseCake
Very delicious Cheesecake. Designed by Sorakage

# OverView
"CheeseCake" is a Lighter, portable and better looking full body tracking device.   
Based on SlimeVR   
With 8-port charging dock, eliminating wiring troubles.   
# CAUTION：   
**Before flashing the firmware, the board must be connected to the battery.**    
This design removes the protection diode, and USB5V is supplied to the battery via the on-board charging chip TP4057.    
The on-board charger will not output voltage without connected to the battery.    


## Index
- [Components](#Components)
- [Versions](#Versions)
- [Printing](#Printing)
- [Assembly](#Assembly)

## Components 
For the CheeseCake you will need the following components:   
●PCB produced by JLC PCBA   
●3D Print Parts   
●38 or 40mm straps   
●Li-po Battery(*803035 800/900mAhis what the docs suggest*) 
●Soldering Iron/Station  

## Versions
There are 3 Versions of PCB included in this Project:   
### BMI160-「Cheese」
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-3D_160.png?raw=true" width="30%">   

### BNO085-「Choco」SpecialRemake
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-3D_Special%20remake.png?raw=true" width="30%">    

### BNO085-「Choco」SpecialRemake(With AUX port)
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-3D_Special%20remake_AUX.png?raw=true" width="30%">    

### BNO085-「Choco」SpecialRemake(With AUX port and DC-DC Buck power supply)    
This might be the best CheeseCake ever. To extend the battery life, it have some magic in it:    
DC-DC Buck Power Supply, which can save up to 18% of power consumption (in 4.2V,LDO need 90mA, but DC-DC only need 74mA).    
And in order to improve signal quality over long distances, leave some Keep-out area at ESP-12F's antenna.    
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-3D_Special%20remake_DCDC.png?raw=true" width="30%">    

### Additional Charging Dock

## Printing
The printing files included in these parts:    
1."CheeseCake"'s Case    
2.Top of Case(In the case that cannot got custom acrylic )    
3.2 kinds of Holder    
4.Charging Dock's Case     

## Assembly    
    
1.  Apply about 2cm foam tape on the inner side of the case (with M2*7mm hexagonal spacers installed by a HAMMER or whatever)      
<img decoding="async" src="https://raw.githubusercontent.com/Sorakage033/SlimeVR-CheeseCake/main/999-PictureFiles/A-01.png" width="80%">     
2.  Place the switch part in position and affix the battery to the case.
<img decoding="async" src="https://raw.githubusercontent.com/Sorakage033/SlimeVR-CheeseCake/main/999-PictureFiles/A-02.png" width="80%">    
3.  Bend the battery wire to ensure it can be tucked into the reserved gap during installation.    
<img decoding="async" src="https://raw.githubusercontent.com/Sorakage033/SlimeVR-CheeseCake/main/999-PictureFiles/A-03.png" width="80%">    
4.  When installing the PCB, put the switch to the "UP" position, tilt it towards the side with the switch. Fit it into the reserved slot on the 3d printing part.    
<img decoding="async" src="https://raw.githubusercontent.com/Sorakage033/SlimeVR-CheeseCake/main/999-PictureFiles/A-04.png" width="80%">    
5.  Tilt the board slightly towards the USB-C side, push the PCB at the side away from the switch.    
<img decoding="async" src="https://raw.githubusercontent.com/Sorakage033/SlimeVR-CheeseCake/main/999-PictureFiles/A-05.png" width="80%">     
6.  Press the whole PCB at position, screw on M2*5mm screws.    
