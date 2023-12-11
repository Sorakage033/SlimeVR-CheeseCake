![Intro-GIF](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-GIF.gif) 

# SlimeVR-CheeseCake
Very delicious Cheesecake. Designed by Sorakage

# OverView
"CheeseCake" is a Lighter, portable and better looking full body tracking device.   
Based on SlimeVR   
With 8-port charging dock, eliminating wiring troubles.   
# CAUTION：   
**When you place an order in JLCPCB, remember change the PCB thickness to 1mm!**    
    
**Before flashing the firmware, the board must be connected to the battery.**    
This design removes the protection diode (to prevent Li-po battery overcharged while uploading firmware), and USB-5V is supplied to the battery via the on-board charging chip TP4057.    
**The on-board charger will not output voltage without connected to the battery.**        
## Extra Info:      
Any kind of modification are welcome!         
It can be even better if you can credit me on the modified PCB with [\[This LOGO\]](999-PictureFiles/SK-LOGO.png)     


## Index
- [Components](#Components)
- [Versions](#Versions)
- [Printing](#Printing)
- [Assembly](#Assembly)
- [Support Link](#Support)

## Components 
For the CheeseCake you will need the following components:   
- PCB produced by JLC PCBA   
- 3D Print Parts   
- 38 or 40mm straps   
-   Li-po Battery (_803035 800/900mAh or 903035 1000/1200mAh is what the docs suggest_)
    -   **Ensure the battery is no larger than 9mm in depth, 30mm in width, and 35mm in height to fit the case.**
    -   **Verify the battery dimensions with the seller before purchase. Some sellers list 803035 batteries with dimensions exceed, which will not fit in the 3D printed case.**
- Pogo Pins (Optional for specific supported PCBs) [\[More Info\]](001-‘’Cheese‘’/POGOPIN%20purchase%20Link.txt)
- Soldering Iron/Station 

## Versions
There are 3 Versions of PCB included in this Project:   
### BMI160-「Cheese」
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-3D_160.png?raw=true" width="30%">   

### BNO085-「Choco」SpecialRemake
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-3D_Special%20remake.png?raw=true" width="30%">    

### BNO085-「Choco」SpecialRemake(With AUX port)
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-3D_Special%20remake_AUX.png?raw=true" width="30%">    

### BNO085-「Choco」SpecialRemake(With AUX port and DC-DC Buck power supply)    
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-3D_Special%20remake_DCDC.png?raw=true" width="30%">      

This might be the best CheeseCake ever. To extend the battery life, it have some magic in it:    
DC-DC Buck Power Supply, which can save up to 18% of power consumption (in 4.2V,LDO need 90mA, but DC-DC only need 74mA).    
And in order to improve signal quality over long distances, leave some Keep-out area at ESP-12F's antenna.    
While using this version, the code in ``define.h`` must be change to:      
```
    #elif BOARD == BOARD_NODEMCU || BOARD == BOARD_WEMOSD1MINI
      #define PIN_IMU_SDA D2
      #define PIN_IMU_SCL D1
      #define PIN_IMU_INT D5
      #define PIN_IMU_INT_2 D6
      #define PIN_BATTERY_LEVEL A0
      #ifndef BATTERY_SHIELD_RESISTANCE
        #define BATTERY_SHIELD_RESISTANCE 0
      #endif
      #ifndef BATTERY_SHIELD_R1 
        #define BATTERY_SHIELD_R1 10
      #endif
      #ifndef BATTERY_SHIELD_R2
        #define BATTERY_SHIELD_R2 47
      #endif    
```      

### LSM6DSV16XTR-「Blueberry」(With AUX port and DC-DC Buck power supply)      
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro-3D_LSM6DSV%20‘’Blueberry‘’.png?raw=true" width="30%">      

It exists, therefore I designed.       

### ICM-42688-「RareCheese」(With external oscillator , AUX port and DC-DC Buck power supply)        
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro_3D_ICM42688“RareCheese”.png?raw=true" width="30%">          

All Japanese love Rare CheeseCake a lot, I love it too.      
And I hope you can also like it.    

### AUX MODULE - SK-MOD       

<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro_3D_SK-BMI270.png" width="30%"><img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro_3D_LSMMOD.png" width="30%"><img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro_3D_ICMMOD.png" width="30%">      
Including 3 different MOD: BMI series, LSM6DSV series and ICM-42688(with External Clock)

```
In SK-BMI MOD, the default IMU on BMI MOD is BMI270, but you can change it to BMI160/BMI323 or other IMUs at PCBA page.
```
It can be solodered on 「Choco」SpecialRemake directly or connect to the AUX port through ``JST 1.25mm 5pin`` like pic below:      
Note: the two connectors are MIRROR      
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro_CONN_sample.png?raw=true" width="100%">       
- **Notice:If you want to use it both solder it on Choco-SpecialRemake and use as AUX, I recommend order JST connector separately and soldering them on by yourself.**       
- **With AUX connector it too thick to fix acrylic top lid, or you need to carve a groove in the corresponding position of the 3D print top lid.**    

And the DEG of this module is fixed to ``DEG_0`` when installed on 「Choco」SpecialRemake or Y axis towards up.        

Also, if you want to upgrade your SlimeVR but not using 「Choco」SpecialRemake, it has a smaller version of SK-BMI270:     
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro_3D_SK-BMI270_Smol.png?raw=true" width="25%">
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro_3D_LSMMOD_Smol.png?raw=true" width="25%">
<img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro_3D_ICMMOD_Smol.png?raw=true" width="25%">      
Though it has a smaller size, if it was soldered on 「Choco」SpecialRemake, it looks a little bit unbalance.      

## 3D Printing for SlimeVR-CheeseCake

This repository contains various 3D printed components required to assemble the SlimeVR-CheeseCake. Below are the necessary files and instructions.

### CheeseCake Case
- **Main Case**: [CheeseCake Case with AUX](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/001.2-Chocolate-Case-With-AUX.stl) - Recommended design compatible with any 3D filament.
- **Alternative Designs**:
  - [Case with USB Port Only](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/001.3-Chocolate-Case_TypeC-Only.stl)
  - [Case with Pogo Pins Cutout](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/001.1-Chocolate-Case.stl)    
- If you want a larger battery, you can use the [803040-case](https://github.com/Sorakage033/SlimeVR-CheeseCake/tree/main/004-3D%20Print%20Model/000.1-Blue-Compact-Case-For-803040-Bat) modified by Blu3u.

### Top Lid
- **3D Printed Option**: [3D Printed Top Lid](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/002-Cake-Top.stl)
- **Acrylic Option**: For a 4mm transparent acrylic lid, use the dimensions provided in [this file](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/AcrylicTop-CutSize-Thickness4mm.png).

### Essential Component
- **Switch Component**: [Switch for Case](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/003-SW.stl) - This part is crucial for the assembly.
- Note: If it's hard to assemble, you can try narrowing the switch by scaling down the Z-axis.

### Holders (Recommended to Print in PETG Filament)
- [Clamp Holder](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/004-''CLAMP''Holder.stl)
- [GoPro Chest Harness Compatible Clamp Holder](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/004-1-''CLAMP''GoPro_Holder.stl) - For GoPro chest harness compatibility.
- [Slide Holder](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/005-''SLIDE''Holder.stl)

### Charging Dock (Recommended to Build the Type-C ChargeDock)
- **8-Tracker Type-C ChargeDock**     
  <img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro_Type-c%20Charging%20Dock.png?raw=true" width="40%">
  - [Top Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-8port-Typec-Top.stl)
  - [Bottom Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-8port-Typec-Bottom.stl)
- **8-Tracker ChargeDock**:
  - [Top Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-8port-Top-Optimized.stl)
  - [Bottom Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-8port-Bottom-Optimized.stl)
- **6-Tracker ChargeDock**:
  - [Top Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-6port-Top.stl)
  - [Bottom Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-6port-Bottom.stl)

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
      
## Support
If this project can help you I would be very happy!      
And also, if you want to give me some support, you can support me on [BOOTH](https://sorakage033.booth.pm/items/4859476)!
