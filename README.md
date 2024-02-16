<h1>Active Directory Home Lab</h1>


<h2>Description</h2>
 Project consists of building a network environment and setting up a virtual machine using Oracle virtual Box. In this Lab we are building our knowledge on how windows and active directory works. We will also be configuring and run PowerShell. Within the Virtual Windows 10 machine it will have many users in the environment, emulating a work setup/environment.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle VM</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Windows 10, 2019 version</b> 

<h2>Program walk-through:</h2>

<p align="center">
Lab overview : <br/>
<img src="https://i.imgur.com/q8jZyQ9.png" height="80%" width="80%" alt="Lab overview"/>
<br />
<br />
Set up network on DC VM:  <br/>
<img src="https://i.imgur.com/jONdI0U.png" height="80%" width="80%" alt="Set up network on DC VM"/>
<br />
<br />
DHCP IPv4 network set up: <br/>
<img src="https://i.imgur.com/GaqgJ43.png" height="80%" width="80%" alt="DHCP IPv4 network set up"/>
<br />
<br />
list names for "employees" for the enviornment:  <br/>
<img src="https://i.imgur.com/MpgZf5p.png" height="80%" width="80%" alt="list names for "employees" for the enviornment"/>
<br />
<br />
enter the powershell on DC VM:  <br/>
<img src="https://i.imgur.com/BSS5AJE.png" height="80%" width="80%" alt="enter the powershell on DC VM"/>
<br />
<br />
In powershell use this script to set up password for users that are going to be in the work enviornment:  <br/>
<img src="https://i.imgur.com/UcOJkD8.png" height="80%" width="80%" <br/>
<img src="https://i.imgur.com/5sSM6w9.png" height="80%" width="80%" alt="In powershell use this script to set up password for users that are going to be in the work enviornment"/>
<br />
<br />
go to "Active Directory Users and Computers", you can see the users in the DC VM:  <br/>
<img src="https://i.imgur.com/2Y2U3Dl.png" height="80%" width="80%" alt="go to "Active Directory Users and Computers", you can see the users in the DC VM"/>
<br />
<br />
Go to Oracle VM and make new operating machine, call it "client 1" to emulate a employee's computer:  <br/>
<img src="https://i.imgur.com/bcc0u2R.png" height="80%" width="80%" alt="Go to Oracle VM and make new operating machine, call it "client 1" to emulate a employee's computer"/>
<br />
<br />
in (client 1) VM open command prompt and check insert "ipconfig" to check if the "employee" computer is connected to the control domain network:  <br/>
<img src="https://i.imgur.com/r0yxEvy.png" height="80%" width="80%" alt="in (client 1) VM open command prompt and check insert "ipconfig" to check if the "employee" computer is connected to the control domain network:"/>
<br />
<br />
Check if network is opperating correctly,in my example I pinged google:  <br/>
<img src="https://i.imgur.com/wPeocRh.png" height="80%" width="80%" alt="Check if network is opperating correctly,in my example I pinged google"/>
<br />
<br />
 Still in (client 1) VM go to system properties and change the domain to "mydomain.com" and rename the PC:  <br/>
<img src="https://i.imgur.com/URD48uB.png" height="80%" width="80%" <br/>
<img src="https://i.imgur.com/4AmMWXq.png" height="80%" width="80%" alt="Still in (client 1) VM go to system properties and change the domain to "mydomain.com" and rename the PC"/>
<br />
<br />
 Go back to the DC VM and head to DHCP and in the IPv4 enviornment network, you can see that the "client 1" is on the network:  <br/>
<img src="https://i.imgur.com/HziYHiq.png" height="80%" width="80%" alt="Go back to the DC VM and head to DHCP and in the IPv4 enviornment network, you can see that the "client 1" is on the network"/>
<br />
<br />
In the "computers" section, you can see that the user/"employee" computer is apart of the work envionment/domain:  <br/>
<img src="https://i.imgur.com/IXpUyzt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

 That is the end of my project, thank you for checking this out! :)
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
