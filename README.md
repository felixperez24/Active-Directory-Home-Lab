<h1>Active Directory Home Lab</h1>



<h2>Description</h2>
Built a Windows Active Directory home lab in a virtualized environment to simulate a corporate domain. Configured Organizational Units (OUs), users, security groups, and department-based access controls. Implemented Group Policy Objects (GPOs) to enforce password policies, restrict Control Panel access, and manage domain security settings. Demonstrates hands-on experience with Active Directory administration, Group Policy, and Windows Server management.
<br />

<h3>Tools & Technologies</h3>

Windows Server 2019

Active Directory Domain Services (AD DS)

Group Policy Management (GPMC)

Active Directory Users and Computers (ADUC)

DNS

Windows 10 (Client VM)

Oracle VirtualBox 

PowerShell 

Windows Administration Tools

<h2>Environments Used </h2>

Host OS: Windows 10

Virtualization: Oracle VirtualBox 

Server: Windows Server 2019

Client: Windows 10 pro

Directory Services: Active Directory Domain Services (AD DS)

Domain Services: DNS

<h2>Management Tools</h2>

Active Directory Users and Computers (ADUC)

Group Policy Management Console (GPMC)

Server Manager

Network: VirtualBox Internal Network / NAT 

<h2>Walk-through:</h2>
<br />

To Start my Home Lab Active Directory I downloaded a ISO of windows 10 and windows server 2019. I used VirtualBox for this environment, after downloading the images i created my Domain Controller first which would be my server. For my network setting for my Domain Controller, adapter 1 is set to NAT and adapter 2 is set to internal network. ( Important later on when connecting CLIENT1 Virtual machine to the Domain controller Virtual machine. <br/>
<img src="AD Lab/Screenshot 2026-07-06 134440.png">
<img src="AD Lab/Screenshot 2026-07-06 134503.png">
<img src="AD Lab/Screenshot 2026-07-06 134528.png">
<br />
<br />

After setting up my DC and succesfully installing Windows Server 2019, I Renamed the two networks. One network is for the Internal network and the other is for External. Once my Network was configured I downloaded Active Directory Domain Services. <br/>
<img src="AD Lab/Screenshot 2026-07-04 201249.png"/>
<img src="AD Lab/Screenshot 2026-07-04 201515.png"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
