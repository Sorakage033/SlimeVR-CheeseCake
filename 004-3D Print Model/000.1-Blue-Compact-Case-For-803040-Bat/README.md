# Blue Compact Case for 803040 Bat

This is a slightly modified version of the original case to use a larger battery, and secondary IMU.

I've made several minor improvements to the 3D models specifically for FDM printing, enhancing their durability.

## Why

- Made for larger 803040 Li-Po battery that appears to be easier to purchase in the EU.
- SlimeVR docs recommend 5cm-wide straps that were incompatible with CheeseCake.
- I did not use acrylic tops, and 4mm case top was problematic while using FDM.
- There were no CheeseCake case 3d models for secondary IMU.

## Features

### Chocolate Case

- Support for 803040 Li-Po that is larger: Now it's 1000mAh instead of 800mAh.
- Support for both original 4cm clamp/slide holders, and the 5cm versions from this directory.

### Chocolate Case for Secondary IMU

- Support for Secondary IMU case that is compatible with the CheeseCake design and holders.
- Low profile while retaining the compatibility with all existing CheeseCake holders.

### Clamp Holder

- Support for default SlimeVR recommended Amazon-sourced Trilancer straps: 5cm instead of 4cm width.
- Improved durability of the major weak spots in clamp holders.

## Assembly guide

Make sure that your filament is at least PETG, kept in a good condition, printed with optimal settings, and preferably with 100% infill modifier at weak spots - as shown in the screenshot. This slightly reduces the risk of breakage. Better safe than sorry!

- Print the cases: `USBC` regular, `USBC+AUX` regular, and `AUX low profile` for secondary IMU variants.
- Print the 3mm case top lids.
- Use the M2 screws. I intentionally kept the single screw hole near USBC port. It prevents the board from shifting.
- (optional) Use gorilla tape on the secondary IMU. In my case it wasn't necessary but I kept the cuboid intended for the tape in the final print.
- (optional) Print the holders for 5cm straps. Remember to measure your straps before printing.

I'm happy with the result. I hope the models will be useful.
