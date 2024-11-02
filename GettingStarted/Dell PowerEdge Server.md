# Server Setup Guide
## Introduction
Welcome to the Server Setup Guide. This document provides a step-by-step walkthrough for setting up the server to create the InfoSec lab. For the purposes of this lab, we are using a Dell Poweredge R620, but you can use whatever fits your needs.
The servers will serve (no pun intended) as the foundation for the lab, allowing the simulation of real-world information technology and security scenarios.
## Prerequisites
Before proceding, ensure posession of the following:
1. Dell PowerEdge R620 Server
2. Included power cables (two for the R620), network cables, mouse, keyboard, and a monitor with a VGA port
3. At least three RAID-compatible hard drives for configuring RAID 5 (striping with parity)
4. VMWare ESXi ISO image for installation
5. Two USB drives: one for the ESXi ISO, and one that we will add the latest iDRAC firmware to
6. A computer or laptop with network connectivity to verify remote management configuration
### Hardware List
[Amazon Shopping List](https://www.amazon.com/hz/wishlist/ls/FFAQ4AJTO8Y9?ref_=wl_share)
## Hardware Setup
This hardware setup is pretty straight forward.
1. Make sure the server is properly connected to a power source, either directly to your wall outlet or a UPS if you already have one setup. For the R620, you will need two available outlets, as there are two power supplies in this server.
2. Connect your monitor to the VGA port on the rear of the server. You will also need to go ahead and connect a keyboard and mouse. The USB ports will also be found in the rear of the server.
3. Connect your drives to the slots at the front and ensure they are properly seated.
4. Connect your network cable to an ethernet port in the rear. For simplicity throughout this process, we will use NIC 1.
5. Press the power button found on the front of the server, to the left of the drive bays.
Once it powers on, you should see it POST on your monitor screen. If you have any errors, refer to Google for troubleshooting.

At this point, we are ready to move on to the next step: System Setup.

## System Setup
Now we will configure the initial setup of the server with System Setup and the Lifecycle Controller. We will need to configure a static IP address, choose our default gateway and DNS servers, and configure RAID.
### Enter Setup Menu
1. Once the server powers on and goes through the POST process, it will automatically load into the Lifecycle Controller. We will eventually go there, but first, we need to press F2 and enter the System Setup.
2. Select your desired language and keyboard options.
3. On the network options to choose a NIC, we will use NIC 1. There are a total of four, but since we plugged our network cable into the first port on the rear of the server, this corresponds with NIC 1.
4. Set a static IP. Be sure that what you choose is not already taken by another device. Generally, there will be 254 addresses available on your subnet. For my lab, I am choosing addresses between 100-200, while my home network devices automatically get an address starting from 1 with DHCP.
5. Input a subnet. Generally this will be 255.255.255.0.
6. Input a default gateway and DNS servers. I am using the IP address of my home router for both.
7. For now, we will leave VLAN off. We will configure this option in a later section.
### RAID Configuration
To start our RAID configuration, we will give the server a reboot and then enter the Lifecycle Controller using F10. Again, for the purposes of this lab, we will setup RAID 5. This RAID type will give us a balance of redundancy, capacity, and performance. As we are only using three drives, it is less likely we will have to deal with a failure. If one does fails, we can use the third drive that contains our parity data to reconstruct the lossed data. If, for some reason, more than one drive fails, our data is lost, as RAID 5 cannot tolerate more than one drive failure. Which RAID configuration you use will depend on your needs; it is best practice to research the different types before you make a decision. Remember, RAID is not a substitute for backups, and since this will be a security-focused lab, we should also consider the possibilities that lie with attackers who wish to render our data unavailable, or any potential disaster that may result in this.
1. Once rebooted and entered into the Lifecycle Controller, select Configure RAID, which is on the Home page.
2. Your controller should be automatically selected. Click next.
3. Select your desired RAID level, then click next.
4. Select all physical disks you wish to include in the RAID setup, and click next.
5. Give the virtual disk a name with no spaces. I just inputted my RAID level here, RAID5. Leave the other options as they are and click next.
6. Verify the information on this screen matches what you inputted in the previous steps, then click Finish.

It will take some time to configure the setup, so grab some coffee and a snack. Once it is finished, it will be time to install [VMware ESXi]().
