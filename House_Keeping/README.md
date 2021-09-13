# To import All Below cases at once, use the following package:
## Current Demo case implemented: 1 to 8 and IOC enrichment 10+
* get the file: **[export-CP4S_Demo_Cases.resz](https://github.com/brostagni/SOAR-Threat-Management-Use-Cases/blob/main/export-CP4S_Demo_Cases.resz)**
* in **Admin > Organisation > Import**, select the file and import it.
* if you get a _timeout_ message during the import, just do it again, it should be good (even the first time on timeout, the package is imported but you just do not get the success message)

## Notes: 
* This package is much nicer with Live integrations: 
  * Install App Host 
  * Configure relevant Tokens and API Keys from the listed Apps
  * Deploy the Apps
  * Verify the Apps are connected corectly (download logs, Stomp should be connected)
* If you do not have an App Host and wish to run this package in _**SIM**ulation_ mode:
  * To be always in _**SIM**ulation_ mode, please update rule zero: **RULE #0: Housekeeping #0** rule: Task note = Yes Change the Boolean Value inside If you do not have an App Host installed and configured, Set value to Task Automation =  NO & Simulation = YES
  * To run only **ONE** incident in _**SIM**ulation_ mode, just create the incident and run the incident action: **Force Simulation to YES**

# Housekeeping project part:
* File Name: **config_HouseKeeping.res-export-20210706155258.res**
* Import Link: (https://github.com/brostagni/SOAR-Threat-Management-Use-Cases/blob/main/House_Keeping/config_HouseKeeping.res-export-20210706155258.res)
## Purpose of this package:
* Add quick import of IOCs with an Incident Action
* Force Simulation in when no AppHost & no Threat Intelligence are set
* Allow to show all fields on this package on a Debug Tab
## Manual activation: 
* Action Button : Add IOCs (4 lists)
* Action But Force Simulation to YES
* Create a Note with _Debug On_ or _Debug Off_ keywords will show or hide the debut tab(layout must be build or imported)
## Extract res file command:  
resilient-sdk extract \
--script "Add IOCs" \
--rule "Debug On" "Debug Off" "Housekeeping #0 rule: Task note = Yes" "Add IOCs" "Force Integration Simulation to NO" "Force Integration Simulation to YES" \
--field "debug" "custom_task_look_automation" "custom_task_force_simulation" \
-n config_HouseKeeping.res --zip

# to be merge with this other package:
* task automation
