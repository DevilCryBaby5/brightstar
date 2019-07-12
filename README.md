# BrightStar™ Engine Management & Control System

### Table of Contents
 * [BrightStar™ Control System & Associated Component Description](https://github.com/TitusStudiosMediaGroup/brightstar/blob/master/README.md#brightstar-control-system--associated-component-description)
 * [Installation](https://github.com/TitusStudiosMediaGroup/brightstar/blob/master/README.md#installation)

## BrightStar™ Control System & Associated Component Description
The BrightStar™ Microprocessor wheelslip control system controls many of the functions of the Locomotive. It's key function is to control the amount of wheelslip and enable maximum tractive effort to be applied. With the introduction of this microprocessor based system, a 25% increase in tractive effort was achieved over the older "E & CHEC" control systems.

The system looks at individual traction motor current and voltage through current shunts on each traction motor circuit. It is able to determine from these readings is a wheel set is turning faster (slipping) or slower than another. Depending on the current / voltage differential and time it took to get there, the system will employ four levels of wheelslip control. This is done to stop the Locomotive from going into a synchronous slip (all wheels spinning) and prevent the train from stalling.

Secondary to this function is the engine / dynamic brake protection management that it carries out. Below this is a description of the hardwere employed to carry out these functions.



### Engine Lube Oil & Water Temperatures (LOT & EWT):
Temperatures are monitored by sensors placed in the main water and oil outlet pipes. Radiator shutters and fan speeds are controlled by the processor at predetermined temperature ranges. If BrightStar™ detects that oil or water temps are getting to high (110 deg C) it will start to decrease the horsepower output of the engine in an attempt to cool the engine down. It will progressively de-rate the horsepower to a point (114 deg C) where the Locomotive will not produce any HP. It will still allow engine RPM to help with cooling of the water and oil.


### Diesel Engine Speed (DSS):
A sensor is placed in the cam gear cover housing, and the system monitors the speed of the engine. It has a predetermined engine speeds loaded for each throttle notch position.


### Engine Crankcase Pressure (COP):
A pressure transducer is placed in the COP / MAP box and is fed via a flexible hose connected to the cam gear cover housing above the DSS. This transducer detects if there is a "Positive" pressure developing in the engine crankcase.


### Manifold Air Pressure (MAP):
A pressure transducer is placed in the COP / MAP box and is fed via a flexible hose connected to the engine air inlet manifold. This transducer reads the turbocharger output pressure (If equipped)


### Dynamic Brake Fan Speed (BSS):
A sensor is placed in the DB fan and the system monitors the speed of the fan. Again there are predetermined fan speeds loaded, and the system will take action if an incorrect speed is detected.


### Main Reservoir Air Pressure (MR1):
A pressure transducer is placed in the main reservoir line, the system controls the cut-in and cut-out of the air compressor at predetermined pressures.


### Barometric Pressure (BPT):
A pressure transducer is placed in the CDC; this is only used to display barometric pressure as we never run at a high enough altitudes in New Zealand to require high altitude deration.


### Ambient Air Temperature (AT):
A temperature sensor is located in the CDC; it monitors the ambient air temperature.


### Driver / Locomotive Interface (DID):
The Diagnostic Information Display is the interface between the locomotive engineer and the locomotive control system. The DID will display locomotive faults if an abnormal operating condition is detected, the computer will initiate the ALARM mode.
In the ALARM mode, the computer uses the DID panel to alert the operator to the fault by displaying a description of the fault and in some cases, ringing an alarm bell. Depending on the severity of the defect, the control system will take action. The action can vary from an error message displayed on the DID panel, restrictions being imposed on the locomotive to the engine shutting down and not being able to be restarted.

Some faults will have an automatic reset function, others will be a manual reset carried out by the operator through the DID.


### Traction Motor Thermal Protection:
The BrightStar™ Control System has preset limits built into the control software and will limit the main alternator output if it reaches the prescribed limits. This function is employed to look after the traction motors and stop them from overheated, causing serious damage.

# Start Up Procedures

Once the BKS & Computer (BC) circuit breaker is closed the BrightStar™ will power up. The full boot up time is around 90 sec's during which time it carries out software integrity self-test. If it detects an issue it will log the fault and a "Reset" will be displayed on the screen above the F4 key. This should be reset before starting the engine.

1. Observe the DID panel, wait until it displays "Engine Not Running"
2. Ensure the EC switch is in the "Start" position.
3. Check the forward / reverse selector (Reverser) handle is in the "neutral" position.
4. Check the throttle handle is in the "Idle" position.


You may now proceed with normal engine starting procedures.


**NOTE:** It is preferable to use the remote start button on the engine so the fuel layshaft can be opened at the same time. This enables faster starting of the engine and is not such a drain on the locomotive starting batteries.

Once the engine is started release the start button, BrightStar™ will automatically drop the cranking contactors out if the engine is running or if the cranking time exceeds 30 seconds and the engine has not been started.

1. Check the DID panel and ensure that the auxiliary generator is running and that the batteries are now charging.
2. When ready to move the locomotive, turn the EC switch to the "Run" position.


## Engine Running

Display panel top line shows "I =" shows the battery is charging, will normally show under "I = 10A". After engine has been running for some time.

V = 74V Auxiliary Generator Voltage.
Tw = Water Temperature
To = Engine Oil Temperature

Reset any stored fault messages.
This is indicated by "Reset?"

Press soft key underneath message (F4), to see what the message is.
Pree button again to Reset. It may be necessary to enter level 2 to reset some faults.

The DID should now show that there are no newer or older faults
The locomotive is now ready for operation.


## Faults

Any fault that is displayed on the DID panel is also stored in the "Fault Log", the operator may view all the logged faults by placing the DID into level 2 and entering the "History" (Soft Key F4). When the "History" you may scroll back through all faults logged. It will always display the newest / active faults logged first.

### Level of Faults 

The faults that the BrightStar™ will detect have a programmed "Priority" list, depending on the fault logged will determine the following:

1. Reset of the fault - Automatic or Manual
2. Level of Access for the reset - Three levels of access
3. Restrictions Imposed

If a manual reset is being carried out, and the level of the reset is greater than the DID panel is in the message "Unable to Reset Fault at this Level" will be displayed on the DID.

### Automatic Resets

The BrightStar™ will automatically reset some faults for the operator; generally these automatic resets are limited to 3 resets within 60 minutes. This fault would then become a manual reset. The fault will only auto reset if the condition disappears.

### Manual Resets

Manual resets are carried out through the DID except for "Low Oil & Low Water Pressure" shutdowns.
Both the LOP & LWP governor shut downs are reset by manually resetting the button on the governor. Once the governor button are reset the BrightStar™ will then automatically reset the DID and the engine can be restarted.

**NOTE:** If the seriousness of the fault is detected is to- great the system will not allow the operator to reset the fault. The locomotive must be returned to the nearest maintenance depot for investigation.

## Alarm Bell

The alarm bell will not always ring when the system detects a fault, some faults will be displayed and logged without the operators knowledge.

In the event of a fault that does activate the alarm bell it may be "Silenced" by pressed the soft key (F3).

The alarm bell can so be silenced by moving the EC switch back to the "Start" position.

## Resetting Serious Faults

### Low Oil & Low Water Pressure

Logging of these conditions take 30 - 40 seconds for the DID panel to display the fault. During this time the diesel engine will shut down.

Before carrying out the resetm, investigate the possible cause of the failure. Both faults need to be reset at the engine governor, the system will reset automatically once the governor button/s are reset.

### Ground Relay

Message Displayed - **"E045 Won't Load: Power Circuit Ground"**
Alarm Bell - Will ring for 30 seconds
Reset - Automatic if throttle is returned to the idle position (Limited to 3 within 60 minutes)

**NOTE:** The system does not know where in the electrical circuit the ground fault has occurred. Traction Motor cutout is fitted to the locomotive so individual traction motors can be cut out if the ground fault persists.




# Installation

1. Click the "Clone or Download" button on the righthand side of the screen and select "Download Zip."
2. Open the Zip file using a program like WinZip or WinRar, if it didn't open automatically.
3. Navigate __INTO__ the "brightstar-master" Folder. You should see two items: a folder named "brightstar_control_system", and readme.md.
4. Extract the two folders directly into: `<Your active steam directory>\SteamApps\common\Garry's Mod\garrysmod\data\expression2\`.
The file path should then look like `expression2\brightstar_control_system\...`.
5. If you see the folder "brightstar-master" inside the "expression2" folder, __YOU INSTALLED IT WRONG__ and the E2 will not work!

You will also need Magnums Train Models and Titus's Locomotive Sound Expansion Pack's Sound packs for it to work correctly. There are eight:

Titus's Locomotive Sound Expansion Pack(s):

 * https://steamcommunity.com/sharedfiles/filedetails/?id=1572612341
 * https://steamcommunity.com/sharedfiles/filedetails/?id=1572613783
 * https://steamcommunity.com/sharedfiles/filedetails/?id=1572616038
 * https://steamcommunity.com/sharedfiles/filedetails/?id=1572620031
 * *There is a fifth addon but it is not required for this to work*
 
Magnum's Train Model Pack
 * https://steamcommunity.com/sharedfiles/filedetails/?id=260954002
 
Grovesteetgman Train Sounds
 * https://steamcommunity.com/sharedfiles/filedetails/?id=240020348
 * https://steamcommunity.com/sharedfiles/filedetails/?id=1254010890
 * https://steamcommunity.com/sharedfiles/filedetails/?id=1254014222

If you're currently in-game in Garry's Mod, open the E2 Editor, and click the "Update" button under the list of E2s on the lefthand side of the window.


## Thank You!
Thank you for installing Titus's GE BrightStar™ Engine Management & Control System E2. 
Find my other work around the internet:
 * [Website](https://titusstudiosmediagroup.github.io/) * https://titusstudiosmediagroup.github.io/
 * [Twitter](https://twitter.com/TitusStudiosMG) * https://twitter.com/TitusStudiosMG
 * [Twitch](https://www.twitch.tv/titusstudios) * https://www.twitch.tv/titusstudios
 
 _Disclaimer: This E2 is no way, shape or form is trying to "steal" the copyrighted works of General Electric or any other business, This E2 and its code is copyrighted under Titus Studios Media, Contact for more information._
_**Extra Note:** The information relating to the **BrightStar™ Engine Management & Control System** is genuine and accurate, and can be applied to real life systems, I do **NOT** take any responsibility for anything users do with this information._

Copyright © 2019 Titus Studios Media. All rights reserved. Contact Titus Studios Media, for more information or licencing.
