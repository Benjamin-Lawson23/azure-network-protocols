<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this turtorial, we will observe network traffic to and from Azure Virtual Machines with Wireshark and also experiment with Network Security Groups.
The main aim of this turtorial is to get a better understanding of firewalls and to solidify our understanding of network protocols. 
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1: Create our Resources
- Step 2: Observe ICMP Traffic
- Step 3: Observe SSH Traffic
- Step 4: Observe DHCP Traffic
- Step 5: Observe DNS Traffic
- Step 6: Observe RDP Traffic

<h2>Actions and Observations</h2>

<p>
<h2>Step 1: Create our Resources</h2>

1. Create a Resource Group in Azure
2. Create a Windows 10 virtual machine 
3. For the new Windows 10 virtual machine, select the Resource Group that we created previously
4. Azure will create a new Virtual Network (Vnet) and Subnet
5. Now, in Azure, create a Linux (Ubuntu) virtual machine
6. For the new Linux virtual machine, select the previously created Resource Group and Vnet
7. You can observe the virtual network by selecting Network Watcher
</p>
<br />

<p>
<img src="https://i.imgur.com/Rk9EF8n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/dfcWSdh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Step 2: Observe ICMP Traffic</h2>

1. Use Remote Desktop to connect to your Windows 10 Virtual Machine (If you are using a Mac, you can download the Microsoft Remote Desktop app from the App Store) 
2. Within your Windows 10 Virtual Machine, open a browser and download and install Wireshark
3. Open Wireshark and type ICMP in the bar at the top to filter for ICMP traffic only
4. Find the private IP address of the Ubuntu virtual machine on Azure and then ping it from within the Windows 10 virtual machine
5. Observe ping requests and replies within WireShark
6. From The Windows 10 virtual machine, open command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in WireShark
7. We will now use VM2's firewall to block ICMP. First, initiate a perpetual ping (-t) from your Windows 10 virtual machine to your Ubuntu virtual machine
8. In Azure, open the Network Security Group for your Ubuntu virtual machine and disable incoming (inbound) ICMP traffic
9. Back in the Windows 10 virtual machine, note the ICMP traffic in WireShark and the command line Ping activity
10. Re-enable ICMP traffic for the Network Security Group for your Ubuntu virtual machine 
11. Back in the Windows 10 virtual machine, observe the ICMP traffic in WireShark and the command line Ping activity (it should start receiving replies again)
12. Stop the ping activity (ctrl + c) 
</p>
<br />

<p>
<img src="https://i.imgur.com/02EVq2V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/sZ00n0t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/nQDRnwI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/7EzT9VK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />





