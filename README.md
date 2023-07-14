<img width="910" alt="Screen Shot 2023-07-13 at 8 45 49 AM" src="https://github.com/SiclaitGitHub/azure-network-protocols/assets/139138443/d6877251-7c35-492f-88d5-41b4c6ccfc66">


A Network Security Group (NSG) is a networking feature provided by cloud service providers, such as Microsoft Azure and Amazon Web Services (AWS), to enforce network security policies and control the flow of network traffic in a virtual network (VNet) or a subnet.

An NSG acts as a virtual firewall, allowing you to define inbound and outbound traffic rules to permit or deny specific types of network communication. These rules can be based on various criteria, including source and destination IP addresses, ports, protocols, and direction of traffic.


- ### [YouTube: Nessus Vulnerability Scanner Installation & Deployment](https://www.youtube.com/watch?v=x87gbgQD4eg)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
-WireShark

<h2> Operating System Used</h2>
- Windows 10 (21H2)


<h2>High-Level Steps</h2>

- Create Vurtual machine in Azure
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
<img width="815" alt="Screen Shot 2023-07-13 at 7 47 02 PM" src="https://github.com/SiclaitGitHub/azure-network-protocols/assets/139138443/f69c50bc-f1f7-4562-8b05-876f6c7bceda">

</p>
<p>
4. Configure WrieShark 

- Search "WrireShark" in the Start menu to locate and launch the WireShark application
- Select "Ethernet" the click teh blue icon in the top left corner to begin monitoring traffic.
  

<img width="871" alt="Screen Shot 2023-07-13 at 7 47 24 PM" src="https://github.com/SiclaitGitHub/azure-network-protocols/assets/139138443/367c9d36-4c2d-4454-af3e-e59cc5e0065c">

5. Observe traffic on the WireShark interfcae
- Once the application begins to run you will see traffic consisting on arious protocols. (Ex: ICMP, HTTP, TCP)



<img width="882" alt="Screen Shot 2023-07-13 at 8 01 35 PM" src="https://github.com/SiclaitGitHub/azure-network-protocols/assets/139138443/3a9cc7a0-92fc-4e57-b53c-8997f14e57f0">

6. Filter traffric from ICMP traffic only

ICMP stands for Internet Control Message Protocol. It is an integral part of the Internet Protocol Suite (TCP/IP) and is used for network diagnostic and error-reporting purposes. ICMP allows network devices, such as routers, to send control messages to other devices in the network.

The primary function of ICMP is to report errors and provide feedback regarding the communication status between network devices. It operates at the network layer (Layer 3) of the TCP/IP model. ICMP messages are encapsulated within IP packets and are typically generated by network devices in response to specific conditions or events. This is also the protocol that "ping" uses

The "ping" function refers to the act of sending ICMP Echo Request messages from one device to another device in order to test network connectivity and measure the round-trip time (RTT) between them. It is a commonly used utility in networking and is available on most operating systems.

- Type "ICMP" in the search bat at the top of the WireSahrk window the press "Enter"
- You will notice that no ICMP traffic is visible. This is eauce the Network Security Group of VM@ is blocking th eflow of this type of traffic between VM! and VM2.


<img width="1427" alt="Screen Shot 2023-07-13 at 11 08 28 PM" src="https://github.com/SiclaitGitHub/azure-network-protocols/assets/139138443/b35829d2-4365-4dba-a381-603b75546b90">

7. Establish SSH Remote Access of VM2 (Linux) from MV1(Windows 10)
</p>
<br />
