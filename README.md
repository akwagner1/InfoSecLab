# InfoSecLab

Welcome to this **InfoSecLab** – a VMware ESXi-based lab environment designed to help you learn and demonstrate competency in **information security**, **networking**, and **active directory**. This lab provides hands-on experience in various areas of security and allows you to explore a range of security tools and practices.

---

## Purpose

The **primary purpose** of this lab is to create an environment where you can develop practical skills and gain hands-on experience in the following areas:

- Setting up and managing **virtual machines (VMs)** within VMware ESXi, a commonly used enterprise hypervisor.
- Implementing **network security controls** to protect systems and data.
- Configuring and monitoring **intrusion detection and prevention systems (IDS/IPS)**.
- Deploying and integrating **Security Information and Event Management (SIEM)** solutions.
- Exploring **security automation and orchestration (SOAR)** tools for effective incident response.
- Testing and evaluating new **network security** products and features.
- And much more...

---

## Lab Components

This lab is built using several key components, each serving a specific function in creating a secure and operational environment:

- **Hardware Setup:**  
   A **Dell PowerEdge** server as the hardware for the virtualization platform.

- **Virtualization:**  
   **VMware ESXi** installed as the hypervisor on the PowerEdge server, enabling the creation of multiple VMs for various security tools and systems.

- **Networking:**  
   A **firewall** (e.g., **pfSense**) configured as the gateway between the lab network and the internet, providing essential security and VPN capabilities.

- **Domain Controller:**  
   A **Windows Server** set up as a domain controller to manage user accounts and provide centralized authentication services.

- **Client Machines:**  
   Multiple VMs (both **Windows** and **Linux**) simulate different network endpoints, servers, and clients for testing and demonstration purposes.

- **Security Tools:**  
   Key security tools are configured, including **Wazuh** (SIEM) and **Security Onion** (IDS/IPS). Additional tools native to an information security environment will also be incorporated.

- **Automation:**  
   **Ansible** used to streamline the deployment and configuration of various components within the lab, reducing manual intervention.

- **Documentation:**  
   Comprehensive documentation maintained, including setup instructions, configuration guides, and troubleshooting steps to help users understand the lab environment effectively.

---

### **Future Goals**

- **VoIP Security:**  
   Implement a secure **VoIP** network with **Fanvil X5U** phones, a dedicated VoIP server VM, and a separate VLAN on a managed switch for secure calling in a simulated office environment.

---

## Getting Started

To get started with setting up the InfoSecLab, please refer to the [Getting Started Documentation](https://github.com/akwagner1/InfoSecLab/tree/main/GettingStarted). It will guide you through the initial setup process, including:

1. Hardware requirements
2. Software installation
3. VMware ESXi configuration

---

## Contributions

Contributions to the InfoSecLab project are always welcome! If you have suggestions, improvements, or new components to add, please feel free to fork the repository, make changes, and submit a pull request.

---

## Disclaimer

This lab is intended for **educational and learning purposes only**. Please be mindful of legal and ethical considerations when conducting offensive or defensive security operations. Adhere to the terms and conditions of the software and tools used. The creators of this repository are not responsible for any misuse or unauthorized activities performed using the provided information and resources.

---

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.
