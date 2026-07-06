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

After setting up my DC and succesfully installing Windows Server 2019, I Renamed the two networks. One network is for the Internal network and the other is for External. Once my Network was configured I downloaded Active Directory Domain Services and created the domain(mydomain.com). <br/>
<img src="AD Lab/Screenshot 2026-07-04 201249.png"/>
<img src="AD Lab/Screenshot 2026-07-04 201515.png"/>
<br />
<br />
I created a admin account for the DC using Active Directory: <br/>
<img src="AD Lab/Screenshot 2026-07-04 205159.png"/>
<img src="AD Lab/Screenshot 2026-07-04 205636.png"/>
<img src="AD Lab/Screenshot 2026-07-04 205527.png"/>
<br />
<br />
Next I downloaded Remote access and configured it so that clients on the private network can access the internet through the domain controller.  <br/>
<img src="AD Lab/Screenshot 2026-07-04 205636.png"/>
<img src="AD Lab/Screenshot 2026-07-04 210006.png"/>
<br />
Up next was installing DHCP on the Domain Controller and configuring it.<br />
<img src="AD Lab/Screenshot 2026-07-04 211152.png"/>
<img src="AD Lab/Screenshot 2026-07-04 212116.png"/>
<img src="AD Lab/Screenshot 2026-07-04 212447.png">
<br />
<br />
After setting up my DHCP i created users using a Powershell Script:  <br/>
<img src="AD Lab/Screenshot 2026-07-04 221045.png"/>
<img src="AD Lab/Screenshot 2026-07-04 222906.png"/>
<img src="AD Lab/Screenshot 2026-07-04 223709.png"/>
<br />
<br />
Creating the CLIENT1 VM( Network setting adapter 1 should be set to internal network) Once the iso image of windows 10 is installed on CLIENT1 VM i test the connection to the Domain controller. Using Command prompt to pull up the ip configuration(Default gateway matches from my DC configuration)
I pinged google.com to make sure my connection to the internet was working, also pinging my server aswell mydoamin.com:  <br/>
<img src="AD Lab/Screenshot 2026-07-06 144218.png"/>
<img src="AD Lab/Screenshot 2026-07-06 122820.png"/>
<img src="AD Lab/Screenshot 2026-07-06 122922.png"/>
<br />
Next i went back to my Domain Controller to check that Client1 was indeed connected and showing up in my DHCP.   <br/>
<img src="AD Lab/Screenshot 2026-07-06 123254.png"/>
<img src="AD Lab/Screenshot 2026-07-06 123332.png"/>
<br />
<br />
The next part of my Lab I created Organizational Units simulating a company and different departments withing the corporation.Such as IT, HR, Finance, and sales. After this i added users to each group and created security groups for each one such as IT-staff.<br/>
<img src="AD Lab/Screenshot 2026-07-06 124456.png"/>
<img src="AD Lab/Screenshot 2026-07-06 125056.png"/>
<br />
<br />
After adding my users to groups I Implemented Group Policy(GPO) using Group policy managment tool. I kept it basic and Prohibited access to the control panel and pc settings for the HR-staff.(Done on DC VM)
<img src="AD Lab/Screenshot 2026-07-06 125633.png"/>
<br />
<br />
Lastly i configured the Password Policy for all users. ( Must be Done in Defualt Domain Policy) 
<img src="AD Lab/Screenshot 2026-07-06 132543.png"/>
</p>
<h2>What I Learned</h2>
One challenge I encountered was ensuring that Group Policy changes were applied correctly to the intended users and computers. After verifying that the GPOs were linked to the correct Organizational Units and confirming group membership, I used the `gpupdate /force` command and verified the applied policies to ensure the settings took effect. I also experienced connectivity issues while configuring remote administration, which I resolved by enabling Remote Desktop, confirming the appropriate Windows Firewall rules were enabled, and verifying network connectivity between the virtual machines. Working through these issues improved my troubleshooting skills and gave me a deeper understanding of how Active Directory and Group Policy function in a Windows domain environment.




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
