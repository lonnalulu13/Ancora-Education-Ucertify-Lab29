# Ancora-Education-Ucertify-Lab29
# Configuring an Access Port

Access ports are used to connect end devices to the network. They are typically configured to accept incoming traffic from the end device as well as send outbound traffic to the end device. They can be configured to use different speeds, duplex settings, and VLANs, depending on the needs of the user.

> **Original Lab Source**
> 
> This lab was available through:
>
>[https://ancoraeducation.ucertify.com/app/?func=navigate_items&item_sequence=2]

## Instructions
The PuTTY SSH Client is used in this lab. It is a popular SSH and Telnet Client that provides a secure way to access remote systems.

**Topology** 

Topology refers to the arrangement or configuration of the virtual network connections within the virtual machine (VM) environment. It defines how the virtual network interfaces and components are interconnected and organized.
 ## Objective of the Lab
 This lab session demonstrates the steps involved in configuring an access port. Upon completion of this lab, you will be able to:

 * Understand the concept of an access port and its importance in network administration.
 *  Configure the port as either an access or trunk port.

## PART A: Establishing Telnet Connection
Access the PuTTY console with IP address as 192.168.116.128, Port as 5016, and Connection type as Other.
### STEP 1
From the left sidebar, open PuTTY SSH Client. The PuTTY Configuration dialog box will appear on the screen.
### STEP 2
Type Host Name (or IP address) as 192.168.116.128
### STEP 3
Type Port as 5016
### STEP 4
Select the Other radio button.
### STEP 5
Click Open to connect the IOU1 terminal window.
### STEP 6
If you don't get a command line prompt in the terminal window, then press Enter.
## PART B: Configuring the Access Port
Enter into configuration mode and execute the commands to configure the access port on VLAN 99 named as ucian for interface e0/3.
### STEP 1
Execute the following commands to enter into configuration mode and configure NetFlow. (Note: Execute one command at a time.):
```bash
configure terminal
```
```bash
vlan 99
```
```bash
name ucian
```
```bash
interface e0/3
```
```bash
switchport mode access
```
```bash
switchport access vlan 99
```
```bash
end
```
### NOTE
* The configure terminal command is used to enter global configuration mode on a Cisco router.
* The vlan 99 command is used to create a VLAN with ID 99.
* The name ucian command is used to configure a name for the VLAN.
* The interface e0/3 command is used to specify and enter interface configuration        mode for the Ethernet interface e0/3 interface.
* The switchport mode access command is used to configure the VLAN membership mode.
* The switchport access vlan 99 command is used to assign the port or range of ports     into access ports.
## PART C: Verifying the Access Port
Execute the commands to verify the configured access port.
### STEP 1
Execute the following commands to observe an access port configuration:
```bash
show vlan
```
### NOTE
The show vlan command is used to display the current VLANs and their assignments.
### STEP 2
Close all windows. At the PuTTY Exit Confirmation prompt, click Yes.
## LAB SUMMARY
This lab session provides you with a straightforward and practical understanding of access ports and how to configure them. Here's a summary of what you have learned:
* How to configure the access port with VLAN settings.
* How to configure the port as either an access or trunk port.

 Now, you are equipped with the knowledge and skills to configure an access port effectively, secure the port, and ensure proper end device connectivity.

## Disclaimer

This repository is for **educational and personal learning purposes only**.  

The original lab content belongs to **uCertify / Ancora Education** and remains their copyrighted material.  
This repository is not affiliated with, endorsed by, or sponsored by uCertify or Ancora Education.  

No copyright infringement is intended.  
Use of any tools or techniques mentioned here should only be performed in authorized, legal environments.
