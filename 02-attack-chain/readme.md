
# Attack Chain Preparation - Kali Attacker Node

## Objective

Deploy a dedicated attacker machine to simulate brute force and credential-based attacks against the domain environment.

## Kali Linux Configuration

- Hostname: KALI
- IP address: 192.168.100.50
- Network: SOC-LAB-NET
- DNS server: 192.168.100.10

The attacker machine is fully isolated within the lab network and will be used to generate authentication events for detection engineering.

## Evidence

### Kali VM Created

![kali vm created](screenshots/01-kali-vm-created.PNG)

### Kali Static IP Configuration

![kali static ip](screenshots/02-kali-static-ip.PNG)

## RDP Exposure on WIN10

Remote Desktop Protocol (RDP) was enabled on WIN10 to simulate an exposed authentication service.

This will be used to generate failed and successful authentication events from the attacker node.

### Evidence

![win10 rdp enabled](screenshots/03-win10-rdp-enabled.PNG)
