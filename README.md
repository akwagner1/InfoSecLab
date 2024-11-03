# InfoSecLab
VMware ESXI lab designed to learn and demonstrate competency in information security, networking, and active directory.
## Purpose
The primary purpose of this lab is to create an environment to develop practical skills and gain hands-on experience in different areas of information security, but also showcases basic networking and active directory. The lab includes:
* Setting up and managing virtual machines (VMs) within a commonly used enterprise hypervisor, VMware ESXI
* Implementing network security controls
* Configuring and monitoring intrusion detection and prevention systems (IDS/IPS)
* Deploying and integrating Security Information and Event Management (SIEM) solutions
* Exploring security automation and orchestration (SOAR) tools for incident response
* Testing and evaluating new network security products and features
* And more...
## Lab Components
This lab consists of the following key components:
* **Hardware Setup:** Utilize a Dell PowerEdge server as the hardware for our virtualization platform.
* **Virtualization:** Install VMware ESXI as the hypervisor on the PowerEdge server to create virtual machines (VMs) for various security tools and computer systems.
* **Networking:** Configure a firewall (e.g., pfSense) as a gateway between the network and the internet, providing security and VPN capabilities.
* **Domain Controller:** Set up a Windows Server as a domain controller to manage user accounts and provide centralized authentication services.
* **Client Machines:** Create multiple VMs (Windows and Linux) to simulate different network endpoints, servers, and clients for testing and demonstration purposes.
* **Security Tools:** Configure Wazuh as a security information and event manager, and Security Onion as our intrusion detection and prevention system. We will also utilize various other tools as may be native to an information security team.
* **Automation:** Utilize Ansible to streamline the deployment and configuration of various components within the lab.
* **Documentation:** Maintain comprehensive documentation, including setup instructions, configuration guides, and troubleshooting steps to help navigate and understand the lav environment effectively.

* ***Future***
* **VoIP:** Establish a secure VoIP network using Fanvil X5U phones, a dedicated VoIP server VM, and separate VLAN on a managed switch, for secure calling in a simulated office environment.
## Getting Started
To get started with the lab, please refer to the documentation provided [here](https://github.com/akwagner1/InfoSecLab/tree/main/GettingStarted). It will guide you through the initial setup process, including hardware requirements, software installation, and configuration steps using VMware ESXI.
## Contributions
## Disclaimer
Please note that the lab is intended for educational and learning purposes. Be mindful of legal and ethical considerations when conducting offensive or defensive security operations and adhere to the terms and conditions of the software and tools used. The creators of this repository are not responsible for any misuse or unauthorized activities performed using the provided information and resources.
