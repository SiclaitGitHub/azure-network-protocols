<img width="910" alt="Screen Shot 2023-07-13 at 8 45 49 AM" src="https://github.com/SiclaitGitHub/azure-network-protocols/assets/139138443/d6877251-7c35-492f-88d5-41b4c6ccfc66">


A Network Security Group (NSG) is a networking feature provided by cloud service providers, such as Microsoft Azure and Amazon Web Services (AWS), to enforce network security policies and control the flow of network traffic in a virtual network (VNet) or a subnet.

An NSG acts as a virtual firewall, allowing you to define inbound and outbound traffic rules to permit or deny specific types of network communication. These rules can be based on various criteria, including source and destination IP addresses, ports, protocols, and direction of traffic.


- ### [YouTube: Nessus Vulnerability Scanner Installation & Deployment](https://www.youtube.com/watch?v=x87gbgQD4eg)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
-WireShark

<h2> Operating System Used</h2>
- Windows 10 (21H2)


<h2>High-Level Steps</h2>

- Create Vurtual machin in Azure
- Install Nessus Application
- Run Vulnerability Scanner
- Address Vulverabilities
- Report Finsings
  
<h2>Actions and Observations</h2>

<img width="908" alt="Screen Shot 2023-07-10 at 1 30 29 PM" src="https://github.com/SiclaitGitHub/osticket-prereqs/assets/139138443/4f97a83e-1c37-4210-9dc1-8530cb7f91bf">


1. Set up your Azure Virtual Machine -OS:  Windows 10 (VM1)

Azure is a cloud computing platform and service offered by Microsoft. It provides a wide range of cloud services that enable organizations to build, deploy, and manage applications and services through Microsoft-managed data centers.

A virtual machine (VM) on Microsoft Azure is a computing resource that uses software instead of a physical computer to run programs and deploy apps. Each VM instance can run its own operating system (OS), which means multiple VMs can run different operating systems on the same physical machine.

Create a new Azure resource group, virtual network, subnet and virtual machine running Windows 10. Choose a VM size according to your needs. Once the VM1 is set up, you will need to connect to it using Remote Desktop. For this, you'll need the public IP address of the VM and the credentials you provided during the VM setup.
</p>
<br />

<img width="800" alt="Screen Shot 2023-07-12 at 10 37 45 PM" src="https://github.com/SiclaitGitHub/azure-network-protocols/assets/139138443/e91c239b-b41c-4282-ae21-a0b5f33643f2">


2. Set up 2nd Azure Virtual Machine - OS: Ubuntu Server 20.04 LTS - x64 Gen2 aka Linux (VM2)

Create a new Azure resource group, virtual network, subnet and virtual machine running Ubuntu Server 20.04 LTS - x64 Gen2 also known as Linux . Choose a VM size according to your needs. Once the VM2 is set up, you will need to connect to it using Remote Desktop. For this, you'll need the public IP address of the VM and the credentials you provided during the VM setup.
</p>
<br />

<p>
<img width="1197" alt="Screen Shot 2023-07-13 at 8 39 41 AM" src="https://github.com/SiclaitGitHub/azure-network-protocols/assets/139138443/ca3b2b6d-853c-4fc7-9a25-f7e055aa92d0">
</p>
<p>
3. Install WireShark on VM1

Wireshark is an open-source network protocol analyzer and packet capture tool. It is used for monitoring and analyzing network traffic in real-time. With Wireshark, you can capture and examine the packets flowing across a network and gain insight into the communication between different devices and protocols.

Wireshark allows you to capture packets from various network interfaces, including Ethernet, Wi-Fi, and Bluetooth. It supports a wide range of protocols, including TCP/IP, HTTP, DNS, FTP, SSH, and many others. You can use Wireshark to analyze both wired and wireless network traffic.

- Install latest version of "WireShark"off so the website. Select "Wndows Installer" then open and install file once dowloaded. 

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
