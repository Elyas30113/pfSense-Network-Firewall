# pfSense Network Firewall

## Project Overview

The **pfSense Network Firewall** is a cybersecurity mini project designed to demonstrate how a firewall can monitor, control, and secure network traffic using predefined firewall rules.

The project was implemented using **Oracle VirtualBox**, **pfSense Community Edition (CE)**, and **Kali Linux**. pfSense acts as the firewall, while Kali Linux acts as the client machine used to generate and test network traffic.

The main objective of this project is to demonstrate practical firewall configuration, packet filtering, access control, network monitoring, and traffic analysis.

---

## Project Objectives

- Configure pfSense as a network firewall.
- Create firewall rules to allow and block specific network services.
- Control network traffic using port-based filtering.
- Test firewall rules using Kali Linux.
- Capture and analyze network packets using Wireshark.
- Verify firewall activity using pfSense logs.
- Understand practical network security concepts.

---

## Technologies and Tools Used

- **Oracle VirtualBox** – Virtualization platform
- **pfSense Community Edition (CE)** – Network firewall
- **Kali Linux** – Client machine for testing
- **Wireshark** – Network packet analysis
- **Firefox** – Accessing the pfSense WebGUI

---

## Project Architecture

```text
+-------------------+
|    Kali Linux     |
|   Client Machine  |
+---------+---------+
          |
          | Network Traffic
          v
+-------------------+
|      pfSense      |
|  Network Firewall |
|                   |
|  Firewall Rules   |
|  Packet Filtering |
|  Logging          |
+---------+---------+
          |
          v
+-------------------+
|  External Network |
|    / Internet     |
+-------------------+
---

## Firewall Rules

### Allowed Traffic

- **DNS – Port 53:** Allows DNS traffic for domain name resolution.
- **HTTP – Port 80:** Allows standard web traffic.
- **HTTPS – Port 443:** Allows secure web traffic.

### Blocked Traffic

- **Telnet – Port 23:** Blocks insecure remote access.
- **SSH – Port 22:** Blocks SSH connections according to the configured security policy.
- **FTP – Port 21:** Blocks FTP traffic.
- **NTP – Port 123:** Blocks NTP traffic.
- **RDP – Port 3389:** Blocks Remote Desktop Protocol traffic.
- **SMTP – Port 25:** Blocks SMTP traffic.
- **ICMP:** Blocks ICMP/ping traffic.

---

## Testing

The configured firewall rules were tested using network traffic generated from Kali Linux.

The testing process included:

1. Generating network traffic from Kali Linux.
2. Checking whether the connection was allowed or blocked.
3. Capturing packets using Wireshark.
4. Analyzing the captured packets.
5. Checking pfSense firewall logs.
6. Comparing the results with the expected firewall rule behavior.

---

## Packet Analysis

Wireshark was used to capture and analyze network packets during firewall testing.

Example filters used:

```text
tcp.port == 23
tcp.port == 22
tcp.port == 21
tcp.port == 80
tcp.port == 443
udp.port == 123
tcp.port == 3389
tcp.port == 25
icmp
dns
```
### Figure 1 - pfSense VM

![Figure 1 - pfSense VM](./Figure%201%20-%20Pf%20Sense%20vm.png)

### Figure 2 - pfSense Network Firewall Dashboard

![Figure 2 - pfSense Network Firewall Dashboard](./Figure%202%20-%20Pf%20Sense%20Network%20Firewall%20Dashboard.png)

### Figure 3 - Implementing Rule

![Figure 3 - Implementing Rule](./Figure%203%20-%20Implementing%20Rule.png)

### Figure 4 - Rules Implemented

![Figure 4 - Rules Implemented](./Figure%204%20-%20Rules%20Implemented.png)

### Figure 5 - Creating Traffic

![Figure 5 - Creating Traffic](./Figure%205%20-%20Creating%20Traffic.png)

### Figure 6 - Opening Wireshark

![Figure 6 - Opening Wireshark](./Figure%206%20-%20Opening%20Wireshark.png)

### Figure 7 - Packet Captured

![Figure 7 - Packet Captured](./Figure%207%20-%20Packet%20Captured.png)

### Figure 8 - Firewall Log Entry

![Figure 8 - Firewall Log Entry](./Figure%208%20-%20Firewall%20Log%20Entry%28Allowing%20and%20Blocking%20the%20predefined%20networks%29.png)

---
## Conclusion

This project demonstrates the practical implementation of a network firewall using pfSense in a virtualized environment. Firewall rules were configured to allow and block selected network traffic. The rules were tested using Kali Linux, while Wireshark was used to capture and analyze network packets. pfSense firewall logs were also examined to verify the expected traffic behavior.

The project provided practical experience with firewall configuration, packet filtering, network monitoring, logging, and basic network security concepts.
