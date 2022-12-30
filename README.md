<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


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

- Create 2 Virtual Machines within Microsoft Azure. Using a Windows 10 Pro Operating System and Linux.
- Connect to Virtual Machine 1 using Remote Connection, then download & install "WireShark" software.
- Step 3
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/oQI4sfL.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
- The first virtual machine being created in Azure is VM1, The operating system being used is Windows 10 pro
</p>
<br />

<p>
<img src="https://i.imgur.com/PMenivn.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Notice in the "Networking" tab that the VM created its own subnet and IP address. This is important because although each Virtual Machine will have its own IP address and subnet, Both virtual machines (VM1 & VM2) will have the same Virtual Network.
</p>
<br />

<p>
<img src="https://i.imgur.com/kEG8YZv.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
- The 2nd virtual machine being created in Azure is VM2. The operating system being used is Linux (Ubuntu 20.04)
</p>
<br />

<p>
<img src="https://i.imgur.com/6JDj8tq.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
- These are the current resources we now have setup inside of Azure.  2 Virtual Machines, 2 Virtual NIC's, 2 Network Security Groups, 2 public IP addresses, and 1 Virtual Network connecting both VM's.
</p>
<br />

<p>
<img src="https://i.imgur.com/dMj9wKX.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Once you've connected into VM1's Remote desktop, Connect to the internet to Download the "WireShark" software then install it unto VM1.
</p>
<br />

<p>
<img src="https://i.imgur.com/LQoeyv9.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Open the "WireShark" application once it finish installing. Double Click on the "Ethernet adapter" Option to start seeing the live data traffic that's happening on the virtual machine. The Blue icon in the top left corner should turn red when traffic is passing through.
</p>
<br />


<p>
<img src="https://i.imgur.com/1nMJJh3.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
- As you can see ICMP traffic shows up on WireShark when you test the Connectivity of VM2. On the command line its continuing to send packets beccause VM2's network security group is allowing inbound IMCP traffic to come through.
</p>
<br />

<p>
<img src="https://i.imgur.com/WXXhWEq.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
- In the Azure Portal you can configure the Network security group settings to stop ICMP traffic from getting to VM2. By 
</p>
<br />
