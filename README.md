# Blue Team Lab — Network Documentation

## 1. Overview

Blue Team Lab is a virtualized environment for conducting application security testing in an isolated setting. All virtual machines are run using Oracle VirtualBox.

## 2. Network Configuration

| Configuration | Value |
|---|---|
| Network Name | BLUE-TEAM-LAB |
| Network Type | NAT Network |
| IPv4 Prefix | 10.10.2.0/24 |
| DHCP | Enabled |

## 3. Virtual Machine Inventory

| VM | Operating System | IP Address | Function |
|---|---|---|---|
| VM 1 | Kali Purple | 10.2.0.10 | Analyst Workstation |
| VM 2 | Ubuntu Server LTS | 10.2.0.9 | Target Linux Server |

## 4. Application Configuration

| Component | Configuration |
|---|---|
| Container Runtime | Docker |
| Container Name | juice-shop |
| Application | OWASP Juice Shop |
| Application Port | 3000 |
| Protocol | HTTP |

## 5. Network Communication

- Kali Purple communicates with Ubuntu Server through the lab network.
- SSH uses TCP port 22 when the SSH service is enabled.
- Kali Purple accesses OWASP Juice Shop through HTTP on TCP port 3000.
- OWASP Juice Shop runs as a Docker container inside Ubuntu Server.

## 6. Security Considerations

- All security testing is restricted to the personal lab.
- Both VMs use the dedicated BLUE-TEAM-LAB NAT Network.
- Shared folders and shared clipboard are disabled.
- No unauthorized testing is performed against external systems.

## 7. Backup and Recovery

Both virtual machines have a `clean-baseline` snapshot for recovery.

## 8. Diagram

See `docs/network-diagram.png` for the complete network topology.
