# Server Hardware Setup Guide
## Introduction
Welcome to the Server Hardware Setup Guide. This document provides a step-by-step walkthrough for setting up the server to create the InfoSec lab. For the purposes of this lab, we are using a Dell Poweredge R620, but you can use whatever fits your needs.
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
At this point, we are ready to move on to the next step: Setup with the Lifecycle Controller.
