# IBM SOAR aka Resilient Uses Cases for Demo & POC under Cloud Pak For Security or Stand Alone SOAR

## Instructions for 1 step full package installation:
PowerPoint: https://ibm.box.com/v/21Demo21DemoThreatEnrichement 
Direct Link to the full Package to install directly on:
* __v17: [export-CP4S_Demo_Cases.resz](https://github.com/brostagni/SOAR-Threat-Management-Use-Cases/blob/main/export-CP4S_Demo_Cases.resz)__
  * CP4S SOAR 1.7+
  * IBM Security SOAR v40.1+ (Resilient Stand Alone) 
  * See additional manual steps to install Components App & Uses Case #16
  * for older versions, please use the old version from April 2021
* Full use cases instructions & download, playbook by playbook: http://ibm.biz/CP4SusecaseTHREAT __*link to change here*__
* Versions
  * __v17 : New SIM mode, new integration WHOIS/RDAP + Custom integration eXtreMe IP in Components__
  * v16 : include internal IPs validation and sub-workflows (pack to be generated)
  * v15 : just remove some tracking notes from Threat Analysis
  * v14 : new URL SCanIO post-process with many improvements !!! & Threat Analysis improvements
  * v12 : Correct bug on TI (TLP & Threat Analysis) Script and rule "TLP from TI" need to be deleted before importing if exist
  * _v11 : DO NOT USE  package downloaded from June 14 - July 2 - BUG on Threat Intell_
_Script and rule "TLP from TI" need to be deleted from old version before importing_

## install the full package within minutes
* download the full package from [export-CP4S_Demo_Cases.resz](https://github.com/brostagni/SOAR-Threat-Management-Use-Cases/blob/main/export-CP4S_Demo_Cases.resz)
* go to you SOAR > Administration > Organisation > Import
* Import the package __export-CP4S_Demo_Cases.resz__
  * if you get a time-out, just import again, it is a BIG package
* __Use it directly with no other configuration (Threat Intelligence, App Host deployed):__
  * Congiguration > Rule > update rule zero : RULE #0: Housekeeping #0 rule: Task note = Yes Change the Boolean Value inside If you do not have an App Host installed and configured, Set value to Task Automation =  NO & Simulation = YES
* __Use it with Threat Intelligence and App Host__
  * Configure the Threat Intelligence in SOAR OR TII with XForce, VirusTotal, and others
  * Create an App Host
  * Deploy the Apps on the App Host and verify the app.config file for sepecific needs of Api Keys expected by the Integration.

## Package installed:
1. [House Keeping](https://github.com/brostagni/SOAR-Threat-Management-Use-Cases/tree/main/House_Keeping)
2. Traffic Light Protocol
3. Automatic incident type setup
4. Severity Color Coding
5. Tracking Users
6. Validation Step by Manager
7. Dynamic Out Of The Box Playbooks
8. Groups & Assign Incident & Task for CP4S & SOAR
9. Analyze Automation for Threat Intel
10. Relation (TO BE ADDED only in v41 import in AppHost)
