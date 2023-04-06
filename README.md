# Honda Beat Speeduino Project
## Why?
Since the Beat has known ECU issues, a stand-alone ECU is desireable. A factory ECU can possibly be repaired, but for future proofing the car 
a stand-alone ECU might be needed. This will be a cheap DIY solution for the car. You can do this as cheap as possible or spend as much as 
you want for other upgrades to come in the future. 

## Goals:
The goal of this project is to have a Honda Beat PP1 run off of a "Speeduino" ECU. Currently (April, 2023) there is only one readily available 
stand-alone ECU for the Beat using an EMU Black. The first phase of this project is to get the Beat running without modifying anything under 
the hood. The only changes to the car will be a wideband and the Speedunio. No modifications will be done to the factory wiring harness. A 
jumper harness will be used so the factory ECU plugs on the car will not be modified. The goal is to be as close to plug and play as possible. 

### After Phase 1:
After the car is running, the goal will be to have the car run with flex fuel. This will use the factory distributor still. A flex fuel sensor 
will need to be added as well as other supporting fuel system upgrades. Once all hardware upgrades are complete on the car, a new tune will 
be created to get the car to run.

### After Phase 2:
After the car sucessfully runs on the Speeduino with flex fuel, the goal will be to run the car with a coil on plug conversion. First, we can 
get the car to run with the distributor still on the car but not using it for spark. It will be used for crank reference. After the car 
sucessfully runs with a coil on plug conversion, using the distributor as a crank reference, a distributor delete will be worked on. This will 
require a seperate trigger wheel and sensor to be installed on the crank pulley. This is needed since the Speeduino needs a crank reference and 
a cam reference. Since we will be loosing the crank reference from the distributor, the custom trigger wheel on the crank is required. A new 
tune will also be needed. Four seperate tunes will be created. One for COP with distributor, one for COP with distributor and flex fuel, one 
for COP and distributor delete, and finally one for COP and distributor delete with flex fuel. 

## Hardware Requirements (for factory setup):
- Arduino MEGA 2560 (USB cable required for loading firmware and tune)
- Speeduino v0.4.x or Speeduino v0.3.x (using v0.4.x for this)
- Standard Speeduino Component Kit.
- MAYBE Onboard MAP Sensor.
- 40 Pin IDC Connector (if using v0.4.x)
- Some VR Conditioner (using JDM VR conditioner from PnPduino)
- Wideband Sensor (using Bosch or Denso LSU 4.9)
- Wideband Controller (using Spartan 2)
- Honda OBD1 ECU Female Connector Housing (for PnP using A and D connectors)

### Hardware Links (US):
- [Arduino MEGA 2560](https://wtmtronics.com/product/arduino-mega-2560/)
- [Speeduino v0.4.x + Components + Map Sensor](https://wtmtronics.com/product/speeduino-v0-4-x-pcb/)
- [LSU 4.9 Wideband + Spartan 2 Controller](https://wtmtronics.com/product/spartan-2-wideband-o2-controller/)
- [40 Pin IDC Connector](https://wtmtronics.com/product/speeduino-0-4-x-connector/)
- [JDM VR Conditioner](https://pnpduino.com/product/jdm-vr/)
- [Honda OBD1 ECU Female Connector Housing](https://www.hamotorsports.com/products/obd1femaleconn)

## Software Needed:
- Tunerstudio
- SpeedyLoader
- A Tune

# Other Helpful Links:
- [Speeduino Wiki](https://wiki.speeduino.com/en/home)
- [Speeduino Repository](https://github.com/noisymime/speeduino)

