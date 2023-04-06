# Factory Beat Sensors and Wiring with Speeduino

# Inputs:

## Trigger Wheels:
The Beat has 3 trigger wheels that could be used. A CKP, TDC, and CYP.
- 24 tooth for CKP on the distributor (requires a VR conditioner)
- 3 tooth for TDC on distributor (will not be used)
- 1 tooth CYP inside cam pulley (requires JDM VR conditioner)

CKP (Crank Angle):
- CKPP to PIN 25 (v0.4.x) Crank Input / VR1+
- CKPM to PIN 27 (v0.4.x) VR1-

CYP (Cam):
- CYPP to PIN 24 (v0.4.x) Cam Input / VR2+
- CYPM to PIN 26 (v0.4.x) VR2-

The 24 tooth wheel will be used for crank reference on a factory distributor setup. The 1 tooth trigger on the cam 
will be used for cam reference. A dual wheel setup is required if no teeth are ground off of the 24 tooth wheel in 
the distributor. A DSC VR conditioner or a Mini Max A2 VR conditioner could be used instead of the JDM VR conditioner 
if you are willing to grind one tooth off of the 24 tooth wheel in the distributor. We are trying to avoid this. 

## TPS:
The Beat has a 3 wire TPS sensor from factory. It has 1 ground wire, 1 VRef, and one signal wire.
- Ground wire to ground
- Signal wire to PIN 22 (v0.4.x) TPS Input
- VRef to PIN 13 or 28 (v0.4.x)

## MAP (external, note: not using factory MAP sensor in our tests):
**NOTE: THIS IS NOT TESTED, TEST THE MAP SENSOR FIRST**
The Beat has a 3 wire MAP sensor from factory. Initial tests will not use this and use the internal MAP sensor on the Speeduino. 
It has 1 ground wire, 1 VRef, and one signal wire.
- Ground wire to ground
- Signal wire to PIN 11 (v0.4.x) 0v-5v MAP Sensor input
- Vref to PIN 13 or 28 (v0.4.x)

## Temperature Sensors:
There are two temperature sensors that will be used. A TA (IAT) and TW (Coolant Temp). 
Both sensors have 1 ground wire and 1 signal wire.\
TA(IAT):
- Ground wire to ground (preferably from ECU)
- Signal wire to PIN 20 (v0.4.x) Inlet Air Temp

TW(Coolant Temp):
- Ground wire to ground (preferably from ECU)
- Signal wire to PIN 19 (v0.4.x) Coolant

## Factory 02 Sensor:
Will not be used. Using Bosch or Denso LSU 4.9 wideband with Spartan 2 controller.

## Wideband:
Using Bosch or Denso LSU 4.9 wideband with Spartan 2 controller.
- Signal wire to PIN 21 (v0.4.x) 02 Sensor

## EACV (IAC - Intake Air Control Valve):
The Beat has a 2 wire EACV from factory. Unsure of wiring to speeduino for now. 

## VSS:
The Beat has a 3 wire VSS from factor. Wiring to come later.

# Outputs:

## Injectors:
Injector #1:
- Wire to PIN 1 (v0.4.x) Injector 1 - PIN 1/2
Injector #2:
- Wire to PIN 2 (v0.4.x) Injector 2 - PIN 1/2
Injector #3:
- Wire to PIN 3 (v0.4.x) Injector 3 - PIN 1/2

## Coil / Ignitor:
- Wire to PIN 7 (v0.4.x) Ignition 1

