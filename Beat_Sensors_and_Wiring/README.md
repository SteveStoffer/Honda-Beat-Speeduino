# Factory Beat Sensors and Wiring with Speeduino

# Inputs:

## Trigger Wheels:
The Beat has 3 trigger wheels that could be used. A CKP, TDC, and CYP.
- 24 tooth for CKP on the distributor (requires a VR conditioner)
- 3 tooth for TDC on distributor (will not be used)
- 1 tooth CYP inside cam pulley (requires JDM VR conditioner)

CKP (Crank Angle):
- (ECU D9 Input) CKPP (Blue / Green) to PIN 25 (v0.4.x) Crank Input / VR1+
- (ECU D10 Signal) CKPM (Blue / Yellow) to PIN 27 (v0.4.x) VR1-

TDC (Not Used)
- (ECU D7 Input) TDCP (Orange / Blue)
- (ECU D8 Signal) TDCM (White / Blue)

CYP (Cam):
- (ECU D5 Input) CYPP (Orange) to PIN 24 (v0.4.x) Cam Input / VR2+
- (ECU D6 Signal) CYPM (White) to PIN 26 (v0.4.x) VR2-

The 24 tooth wheel will be used for crank reference on a factory distributor setup. The 1 tooth trigger on the cam 
will be used for cam reference. A dual wheel setup is required if no teeth are ground off of the 24 tooth wheel in 
the distributor. A DSC VR conditioner or a Mini Max A2 VR conditioner could be used instead of the JDM VR conditioner 
if you are willing to grind one tooth off of the 24 tooth wheel in the distributor. We are trying to avoid this. 

## TPS:
The Beat has a 3 wire TPS sensor from factory. It has 1 5V+ wire, 1 5V- wire, and one signal wire.
- (ECU D22 5v+) Yellow / Red PIN 13 (v0.4.x) 5v
- (ECU D11 Signal) Green to PIN 22 (v0.4.x) TPS Input
- (ECU D20 5v-) Brown / Black to PIN 12 (v0.4.x)

## MAP (external):
**NOTE: THIS IS NOT TESTED, TEST THE MAP SENSOR FIRST**\
The Beat has a 3 wire MAP sensor from factory. Initial tests will not use this and use the internal MAP sensor on the Speeduino. 
It has 1 ground wire, 1 VRef, and one signal wire.
- (ECU D13 Signal) White PIN 11 (v0.4.x) Map Sensor (0v - 5v)
- (ECU D19 5v- dedicated) Green / Blue PIN 10 (v0.4.x) 
- (ECU D21 5v+) Red / White PIN 13 (v0.4.x) 5v 

## Temperature Sensors:
There are two temperature sensors that will be used. A TA (IAT) and TW (Coolant Temp). 
Both sensors have 1 5v- wire and 1 signal wire.\
TA(IAT):
- (ECU D15 Signal) Red / Yellow to PIN 20 (v0.4.x) Inlet Air Temp
- (ECU D20 5v-) Brown / Black to PIN 23 (v0.4.x) 

TW(Coolant Temp):
- (ECU D17 Signal) Red / White to PIN 19 (v0.4.x) Coolant
- (ECU D20 5v-) Brown / Black PIN 23 (v0.4.x)

## Factory 02 Sensor:
Will not be used. Using Bosch or Denso LSU 4.9 wideband with Spartan 2 controller.

## Wideband:
Using Bosch or Denso LSU 4.9 wideband with Spartan 2 controller.
- Signal wire to PIN 21 (v0.4.x) 02 Sensor

## EACV (IAC - Intake Air Control Valve):
The Beat has a 2 wire EACV from factory. Unsure of wiring to speeduino for now. 
- (ECU A9) Light Blue (changes to) Black / Blue to PIN 37 (v0.4.x) PWM Idle
- (ECU A23 Spliced A25) Red / Black to PIN TBD (v0.4.x)

## VSS:
The Beat has a 3 wire VSS from factory.
- (ECU D3) Light Blue (changes to) Yellow / Red -------- Cluster ---- ECU (PIN TBD / Not Needed)
- Yellow / Black (changes to) Yellow -- 10A Key On.
- Black - Ground

# Outputs:

## Injectors:
Injector #1:
- (ECU A1) Red to PIN 1 (v0.4.x) Injector 1 - PIN 1/2
- (ECU A23 Spliced A25) Red / Black PIN TBD (v0.4.x) \

Injector #2:
- (ECU A23) Light Blue to PIN 2 (v0.4.x) Injector 2 - PIN 1/2
- (ECU A3 Spliced A25) Red / Black PIN TBD (v0.4.x) \

Injector #3:
- (ECU A5) Yellow to PIN 3 (v0.4.x) Injector 3 - PIN 1/2
- (ECU A23 Spliced A25) Red / Black PIN TBD (v0.4.x)

## Coil / Ignitor:
- (ECU A15 Spliced A16) White to PIN 7 (v0.4.x) Ignition 1

(ECU D1 12v+ 7.5A for ECU) Thin White / Blue

