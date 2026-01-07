h1>Secure Network Implementation with DMZ, Firewall, and Trusted Zones: A Practical Implementation</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>

<br>SecureNetworkLab is a virtualized network infrastructure project designed to help organizations expand their IT capabilities within limited space and budget constraints. This lab demonstrates how to deploy scalable, secure systems using virtualization and open-source tools.

Key features of the implementation include:

Virtual Machine Deployments to minimize hardware costs and physical space usage

Scalable Infrastructure that supports seamless upgrades and expansion

Secure Network Segmentation to isolate trusted users from untrusted actors

The completed virtual environment includes:

🌐 Web Server

🔥 Router-Firewall (pfSense)

🖥️ CEO Workstation and Trusted User PC

📡 DNS Server

🛡️ Demilitarized Zone (DMZ)

This repository serves as a practical showcase of secure network design, virtualization strategy, and access control implementation—ideal for IT professionals, students, and cybersecurity enthusiasts.
<br />


<h2>Environments Used </h2>

- <b>Windows 11 (Host OS)</b> (21H2)
- <b>Virtual Box VM</b>
- <b>Router-Firewall (pfsense)</b>
- <b>CEO Workstation (pfsense)</b>
- <b>Web Server (pfsense)</b>
- <b>DNS Server (pfsense)</b>
- <b>Demilitarized Zone (DMZ) (pfsense)</b>


<h2>Project walk-through:</h2>

<p align="center">
Network Diagram: <br/>
<img src="https://imgur.com/U7HG1gy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
IP Structure for the Network:  <br/>
<img src="https://imgur.com/QDXrGOn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Deploying the VMs:  <br/>
<img src="https://imgur.com/TQKiIUP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setting up the CEO PC IP address:  <br/>
<img src="https://imgur.com/QKiOMSe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connectivity Test on The Network using ping utility:  <br/>
<img src="https://imgur.com/FWBBJkF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Performing Scanning Using NMAP Against DNS-Server:  <br/>
<img src="https://imgur.com/1dkUkND.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Running an Active Scan Using NMAP RESULTS FOR WEB SERVER:  <br/>
<img src="https://imgur.com/NdEC0Xk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Running a Connectivity Test from a Trusted Network to Untrusted Network:  <br/>
<img src="https://imgur.com/SBWfKHC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Running a Connectivity Test from a Untrusted Network to Trusted Network:  <br/>
<img src="https://imgur.com/yGawPpd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Capturing Packets Using WireShark:  <br/>
<img src="https://imgur.com/WBTZCnj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<h2>Conclusion</h2>

<br>This project marks a significant milestone in advancing the company's IT capabilities while adhering to strict space and budget limitations. By leveraging virtualization technologies, I successfully transformed a constrained environment into a secure, scalable, and efficient network infrastructure. The deployment of key components including a Web Server, Router-Firewall, DNS Server, DMZ, and dedicated workstations ensures robust performance, enhanced security, and future-proof flexibility.
The implementation not only meets current operational demands but also lays a solid foundation for seamless expansion and integration of future technologies. Through strategic planning and execution, this project demonstrates how innovative thinking and technical expertise can overcome resource limitations and deliver enterprise-grade solutions.
As one of my key projects, it reflects my commitment to practical problem-solving, secure system design, and scalable architecture core principles that I will continue to apply in future IT initiatives.
<br />
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
