# Linux Static IP & Subnet Segmentation Lab

## 📌 Overview

This lab demonstrates manual IP configuration, subnet segmentation using CIDR notation, and validation of subnet boundaries within a Linux virtual machine environment.

The objective was to simulate multiple hosts within a smaller subnet (/28) inside a larger /24 network and verify routing behavior, broadcast boundaries, and scoped network scanning.

---

## 🖥 Environment

- OS: Ubuntu Linux (VM)
- Interface: `enp0s1`
- Base Network: `192.168.64.0/24`
- Tools Used:
  - `ip` (IP configuration)
  - `ping` (connectivity testing)
  - `nmap` (network scanning)
  - `ip route` (routing table analysis)

---

## 🎯 Objectives

- Manually assign static IP addresses
- Create a `/28` subnet inside an existing `/24`
- Identify network and broadcast addresses
- Validate subnet boundaries
- Perform subnet-scoped host discovery
- Analyze longest prefix match behavior

---

## 🔧 Step 1 — Assign Static IP Addresses

Three simulated hosts were created within a `/28` subnet:

```bash
sudo ip addr add 192.168.64.18/28 dev enp0s1
sudo ip addr add 192.168.64.19/28 dev enp0s1
sudo ip addr add 192.168.64.20/28 dev enp0s1
---

## 📸 Screenshots
![broadcast-test](broadcast-test.png)
![sudo-tcpdump-enp0s1](sudo-tcpdump_enp0s1.png)
![Routing Table](screenshots/routing-table.png)


![dns-resolution-verification.png](dns-resolution-verification.png)

