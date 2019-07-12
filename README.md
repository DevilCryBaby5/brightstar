# BrightStar™ Engine Management & Control System


## BrightStar™ Control System & Associated Component Description
The BrightStar™ Microprocessor wheelslip control system controls many of the functions of the Locomotive. It's key function is to control the amount of wheelslip and enable maximum tractive effort to be applied. With the introduction of this microprocessor based system, a 25% increase in tractive effort was achieved over the older "E & CHEC" control systems.

The system looks at individual traction motor current and voltage through current shunts on each traction motor circuit. It is able to determine from these readings is a wheel set is turning faster (slipping) or slower than another. Depending on the current / voltage differential and time it took to get there, the system will employ four levels of wheelslip control. This is done to stop the Locomotive from going into a synchronous slip (all wheels spinning) and prevent the train from stalling.

Secondary to this function is the engine / dynamic brake protection management that it carries out. Below this is a description of the hardwere employed to carry out these functions.



## Engine Lube Oil & Water Temperatures (LOT & EWT):
Temperatures are monitored by sensors placed in the main water and oil outlet pipes. Radiator shutters and fan speeds are controlled by the processor at predetermined temperature ranges. If BrightStar™ detects that oil or water temps are getting to high (110 deg C) it will start to decrease the horsepower output of the engine in an attempt to cool the engine down. It will progressively de-rate the horsepower to a point (114 deg C) where the Locomotive will not produce any HP. It will still allow engine RPM to help with cooling of the water and oil.


## Diesel Engine Speed (DSS):
A sensor is placed in the cam gear cover housing, and the system monitors the speed of the engine. It has a predetermined engine speeds loaded for each throttle notch position.


## Engine Crankcase Pressure (COP):
A pressure transducer is placed in the COP / MAP box and is fed via a flexible hose connected to the cam gear cover housing above the DSS. This transducer detects if there is a "Positive" pressure developing in the engine crankcase.


## Manifold Air Pressure (MAP):
A pressure transducer is placed in the COP / MAP box and is fed via a flexible hose connected to the engine air inlet manifold. This transducer reads the turbocharger output pressure (If equipped)


## Dynamic Brake Fan Speed (BSS):
A sensor is placed in the DB fan and the system monitors the speed of the fan. Again there are predetermined fan speeds loaded, and the system will take action if an incorrect speed is detected.


## Main Reservoir Air Pressure (MR1):
A pressure transducer is placed in the main reservoir line, the system controls the cut-in and cut-out of the air compressor at predetermined pressures.


## Barometric Pressure (BPT):
A pressure transducer is placed in the CDC; this is only used to display barometric pressure as we never run at a high enough altitudes in New Zealand to require high altitude deration.


## Ambient Air Temperature (AT):
A temperature sensor is located in the CDC; it monitors the ambient air temperature.


## Driver / Locomotive Interface (DID):
The Diagnostic Information Display is the interface between the locomotive engineer and the locomotive control system. The DID will display locomotive faults if an abnormal operating condition is detected, the computer will initiate the ALARM mode.
In the ALARM mode, the computer uses the DID panel to alert the operator to the fault by displaying a description of the fault and in some cases, ringing an alarm bell. Depending on the severity of the defect, the control system will take action. The action can vary from an error message displayed on the DID panel, restrictions being imposed on the locomotive to the engine shutting down and not being able to be restarted.

Some faults will have an automatic reset function, others will be a manual reset carried out by the operator through the DID.


## Traction Motor Thermal Protection:
The BrightStar™ Control System has preset limits built into the control software and will limit the main alternator output if it reaches the prescribed limits. This function is employed to look after the traction motors and stop them from overheated, causing serious damage.
