# Introduction
This document provides a step-by-step walkthrough for installing Ubuntu Server, configuring a static IP, DNS servers, and gateway with Netplan, joining the server to the domain, adding domain admins to the sudoers group, and installing and configuring Wazuh for security monitoring in your lab environment.
## Installing Ubuntu Server
1. Insert the Ubuntu Server installation media ISO from the ESXi storage pool and boot the server from it.
2. Select Install Ubuntu Server and press Enter.
3. Choose to configure the network manually for a static IP configuration.
4. Select your preferred storage method and complete the disk setup.
5. Select the desired software packages or opt for a minimal installation.
6. Create a user account and set a password.
7. After installation, reboot the server and log in.
## Configuring a Static IP
We will need to configure a static IP address so that when we deploy our Wazuh agents later on, they will always refer to this Ubuntu server as the Wazuh manager. To edit our network configuration, we will use Netplan.
1. Find your NIC name with ifconfig. Mine is ens160.
2. sudo vim /etc/netplan/50-cloud-init.yaml
3. Configure the file to show as follows:
   network:
     ethernets:
       ens160: #This is the name of my NIC as designated by Ubuntu, yours may be different
         dhcp4: false #Disables DHCP so that we can manually an IP address
         addresses: [192.168.1.xx/24] #Select the IP address you want for this server. We will use it again when deploying the Wazuh agents
         nameservers:
           addresses: [192.168.1.xx, 8.8.8.8] #Use the address of our domain controller, which has DNS functionality. Also included Google's nameserver when connecting to the internet
         routes:
           - to: default
             via: 192.168.1.x #Using the router address
4. Apply changes with sudo netplan apply.
5. Verify the IP address is correct with ifconfig.
6. In order to communicate directly to your home router, and ultimately the internet, you may need to manually add a route to the routing table in Ubuntu. Do this with sudo ip route add default via IPADDRESS dev ens160. Replace ens160 with the interface name you determined earlier.
7. Verify connectivity with the domain controller with ping -c 3 IPADDRESS. Ensure to replace IPADDRESS with the address of your domain controller.
8. Verify connectivity to the internet with ping -c 3 8.8.8.8

If there is proper conenctivity, we can move on to adding this server to our domain.
## Joining the Domain
