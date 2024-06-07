# Project: Security Project

## Objective
The overall objective of this project is to apply the knowledge acquired in the computer security module. The specific objectives are:
- Analyze incoming and outgoing traffic in a network architecture via a firewall.
- Design, configure, and activate filtering rules.
- Implement an IDS/IPS.
- Configure an intrusion detection tool Snort.
- Establish a Virtual Private Network (VPN).
- Deploy OpenVPN.
- Test some vulnerabilities of web applications.
- Apply one or two attacks among the 10 OWASP attacks to verify the resilience of the security policy and the attack detection-prevention system in place.

## Description
A company wants to secure its network, which is described as follows:
- A LAN network: includes all employee machines (internal users).
- A DMZ network: includes various servers hosting the company's business applications.
- A WAN network: includes all machines external to the company's network.

To protect the above architecture, the network security administrator proposed to implement a firewall as the first step. The access rules are described as follows:
Security Policy:
1. Company employees are allowed to browse the web.
2. Clients always have access to the web server.
3. Company employees can exchange emails using a locally implemented mail server.
4. Company employees can work remotely (telecommuting) using a secure connection through a VPN.
5. The network administrator must access from the LAN machine to the DMZ zone using the SSH protocol.
6. Authentication between the SSH server and its client must be done with keys, not passwords.
7. Prohibit any other application access to the servers.

## Tasks Assigned
### A. Implementation of the Network Architecture
- Replicate the network architecture using virtual machines under Linux.
- Perform necessary configurations (addressing, routing, etc.) and test connectivity between the three zones (LAN, WAN, and DMZ).
- Visualize the network traffic using Wireshark.

### B. Attack Testing
As an ethical attacker (white hacker), conduct some attacks to analyze the security of the unprotected network architecture:
- Test an attack of your choice from Chapter 2: visualize and interpret the result.
- Test one or two attacks among the 10 OWASP (Web Application Security Project) attacks: visualize and interpret the result.
  - What solutions would you propose for each attack tested?

### C. Securing the Network Architecture
#### Part 1: Firewall Filtering/Remote Access
- Install and configure Pfsense as a firewall to secure access across the different zones.
- Establish the filtering policy to control access to the different zones.
- Test access to various services from different zones: web access from LAN, access to public servers from LAN and WAN.
- Test remote access through SSH from the LAN machine to the DMZ with public key authentication.

#### Part 2: Intrusion Detection
- Install and configure Snort software at the network level.
- Perform tests with Snort: simple sniffer, alerts, etc.

#### Part 3: Virtual Private Network
- Install and configure OpenVPN on both LAN and WAN machines.
- Test secure authentication of local OpenVPN users.
  - Test VPN tunnel establishment between the two LAN and WAN networks.
  - Visualize traffic exchanged between these two machines using Wireshark for VPN tunnel establishment.

#### Part 4: Enhanced Security Level Testing
The network administrator wishes to verify the enhanced security level:

- Attempt to repeat previously tested attacks.
- Interpret the results.
- In general, is security guaranteed 100% even in the presence of Firewall, IDS/IPS, and traffic exchanges via VPN or SSH?
