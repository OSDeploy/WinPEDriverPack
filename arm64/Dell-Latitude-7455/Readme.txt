####################################################################

Latitude 7455 DRIVER PACK A00 Driver 71MMN

####################################################################

Description:

With the Dell Command | Deploy Driver Pack, an Information
Technology Administrator can perform the following tasks: 

- Use Microsoft(R) Windows(R) operating system-based PnP enumeration
  capabilities to install drivers for applicable devices 

- Create a system-level optimized deployment sequence

- Setup an appropriate boot control sequence 

- Optimize the deployment of targeted system-specific driver packages  

Contents:

This file contains the following sections: 

* Criticality

* Minimum Requirements

* Release Highlights

* Installation

* User Notes

####################################################################
CRITICALITY
####################################################################

Optional - Dell recommends the customer review specifics about the
update to determine if it applies to your system. The update contains
changes that impact only certain configurations, or provides new
features that may/may not apply to your environment.

####################################################################
MINIMUM REQUIREMENTS
####################################################################

Compatibility / Minimum Requirements:

Latitude 7455 System

Windows Hardware Quality Lab (WHQL) Certification:  Not Applicable

####################################################################
RELEASE HIGHLIGHTS
####################################################################

Supported Systems, Operating Systems and Architecture

Latitude
--------
7455	win11 arm64
 
####################################################################
INSTALLATION
####################################################################

Windows Explorer supports native viewing of CAB contents. Users can 
also use WinZip to examine the contents of the cab. Optionally 
Microsoft provides a couple of tools via the Windows XP Service Pack 2 
Support Tools to examine the cabinet files. Extraction tools (CabArc 
and Extract) are available from Microsoft at the following location:

http://www.microsoft.com/downloads/details.aspx?
FamilyId=49AE8576-9BB9-4126-9761-BA8011FABF38&displaylang=en.  

- CAB Management Tool from Microsoft 
  Using CabArc to extract the driver contents and maintain directory 
  structure:
  CabArc.exe -p x <cab file path> *.* <output path>
  (e.g. C:\CabArc.exe -p x C:\<cab-file-name> *.* C:\drivers\)

- Extract Utility from Microsoft
  Once you are in the directory where you want to extract, enter the 
  following command: extract /Y /E <cab-file-name>

- To extract .EXE based Driver Packs run the command DriverPack.exe /s /e=<path> 
  

####################################################################
USER NOTES
####################################################################

Visit the Dell Tech Center at:
https://www.dell.com/support/kbdoc/en-us/000124139/dell-command-deploy-driver-packs-for-enterprise-client-os-deployment for additional help on 
using these Driver Packs for Operating System Deployment.

####################################################################

Information in this document is subject to change without notice.
(C) 2024 Dell Inc. All rights reserved.

Reproduction of these materials in any manner whatsoever without 
the written permission of Dell Inc. is strictly forbidden.

Trademarks used in this text: Dell, the DELL logo, OpenManage, 
Latitude, OptiPlex, Venue and Dell Precision are trademarks of Dell Inc.;
Intel is a trademark of Intel Corporation in the U.S. and other
countries; Altiris is a registered trademark of Altiris Inc.; 
Microsoft, Windows, and Internet Explorer are either
trademarks or registered trademarks of Microsoft Corporation in the
United States and/or other countries; Bluetooth is a registered
trademark owned by Bluetooth SIG, Inc. and is used by Dell Inc.
under license.

Other trademarks and trade names may be used in this document to 
refer to either the entities claiming the marks and names or their 
products. Dell Inc. disclaims any proprietary interest in trademarks 
and trade names other than its own.


June 2024
 