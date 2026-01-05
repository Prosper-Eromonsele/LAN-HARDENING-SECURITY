# LAN Hardening: Layer 2 Security Implementation
## Project Overview
This project demonstrates the implementation of essential Layer 2 security features on a Cisco-based network. The goal is to mitigate common network attacks such as MAC Address Flooding, DHCP Spoofing, and ARP Poisoning (Man-in-the-Middle).

The environment was built and simulated using **Cisco Packet Tracer**.

---

## 🛠 Features Implemented
* **Port Security:** Restricted access to switch ports by locking them to specific MAC addresses and setting violation actions.
* **DHCP Snooping:** Created a "trusted" zone to prevent rogue DHCP servers from handing out malicious IP configurations.
* **Dynamic ARP Inspection (DAI):** Used the DHCP snooping binding database to validate ARP packets, preventing ARP spoofing.
* **VLAN Segmentation:** Organized the network into functional segments to reduce the broadcast domain.

---

## 🗺 Network Topology
The topology follows a redundant design with an Edge layer (Internet) and an Access/Distribution layer.



* **Routers A & B:** Act as the gateway to the Internet.
* **Routers C & D:** Act as the core/distribution switches where security policies are enforced for the end-user PCs.

---

## 🚀 Configuration Highlights

### 1. Port Security (Interface Level)
Prevents an attacker from connecting an unauthorized device to an open wall jack.
```bash
interface FastEthernet0/1
 switchport mode access
 switchport port-security
 switchport port-security maximum 1
 switchport port-security mac-address sticky
 switchport port-security violation shutdown
2. DHCP Snooping
Ensures only the legitimate server can provide IP addresses.

Bash

ip dhcp snooping
ip dhcp snooping vlan 10
! Set the uplink port to the router as trusted
interface GigabitEthernet0/1
 ip dhcp snooping trust
3. Dynamic ARP Inspection (DAI)
Prevents Man-in-the-Middle attacks.

Bash

ip arp inspection vlan 10
! Trust the interface connected to other network devices
interface GigabitEthernet0/1
 ip arp inspection trust
🧪 Verification & Results
To verify the hardening, the following tests were performed:

MAC Attack: Attempted to connect a new laptop to a secured port; the port immediately entered err-disabled state.

Rogue DHCP: A laptop configured as a DHCP server attempted to offer IPs; packets were dropped by the switch.

ARP Spoofing: Attempted to send a fake ARP response; the switch logged an invalid ARP packet and dropped it.

📁 Repository Contents
/Topology: Contains the .pkt file for Cisco Packet Tracer.

/Scripts: Text files with the full CLI configurations for Routers A, B, C, and D.

/Screenshots: Evidence of successful security triggers and "Show" commands.
