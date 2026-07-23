# Akram Khoulid

> **Building infrastructure from first principles.**

I build secure infrastructure by combining Linux, networking, cloud technologies, and security practices into complete, production-inspired environments.

Currently pursuing a degree in **Networks & Telecommunications Engineering at ENSA Safi**, I focus on understanding systems from the ground up—how they're built, how they communicate, how they fail, and how to secure them.

Rather than treating projects as isolated exercises, I use them to explore real engineering concepts, document every important decision, and create resources that I can continuously refine as my knowledge grows.

## Engineering Philosophy

I believe good infrastructure is built on understanding rather than memorization.

Instead of learning technologies in isolation, I prefer to understand the principles behind them by building complete environments, troubleshooting real problems, and documenting every decision along the way.

My projects follow a consistent approach:

- Build from first principles rather than relying on abstraction.
- Understand how every component interacts with the rest of the system.
- Design security into the architecture instead of adding it later.
- Document the implementation as thoroughly as the implementation itself.
- Continuously improve existing projects as my knowledge grows.

I don't collect technologies.

I build complete systems, understand how they work, and document the lessons learned so they can be reproduced and improved.

## 📁 Engineering Portfolio

> Every project in this portfolio was built to explore real infrastructure concepts through hands-on implementation. Rather than treating projects as isolated exercises, I design complete environments, troubleshoot real-world problems, and document the entire engineering process.

---

<details>
<summary>

### 🛡️ Zero Trust SSH Bastion
*OpenSSH • ProxyJump • nftables • Zero Trust • Ubuntu Server*

</summary>

<br>

> **A production-inspired SSH gateway that secures access to internal infrastructure using Zero Trust principles.**

<p align="center">
  <img src="images/bastion-architecture.png" alt="Zero Trust SSH Bastion Architecture" width="850">
</p>

### Overview

This project implements a production-inspired SSH architecture where administrative access to internal systems is performed through a hardened Bastion Host instead of exposing servers directly to the network.

The environment was designed to explore SSH beyond basic remote access by implementing public key authentication, ProxyJump, firewall policies with **nftables**, and network segmentation following Zero Trust principles.

### Architecture

> *(Architecture diagram placeholder)*

### Engineering Highlights

| Category | Implementation |
|-----------|----------------|
| Authentication | SSH Public Key Authentication |
| Secure Access | SSH ProxyJump |
| Firewall | nftables |
| Security Model | Zero Trust Architecture |
| Operating System | Ubuntu Server |
| Internal Host | Kali Linux |

### Key Takeaways

- Designed a secure SSH architecture inspired by production environments.
- Hardened OpenSSH using public key authentication.
- Built stateful firewall rules with nftables.
- Applied Zero Trust principles to Linux infrastructure.
- Troubleshot authentication, firewall, routing, and forwarding issues.
- Produced detailed technical documentation covering the entire deployment.

### Repository

- 📂 **Repository:** https://github.com/yourusername/your-repository
- 📖 **Documentation:** https://github.com/yourusername/your-repository/tree/main/docs

</details>

---

<details>
<summary>

### 🔍 Wazuh SIEM Security Monitoring Lab
*Wazuh • Ubuntu • Kali Linux • Detection • Monitoring*

</summary>

<br>

> **A complete SIEM laboratory built to monitor Linux infrastructure, centralize logs, and improve security visibility.**

<p align="center">
  <img src="images/wazuh-architecture.png" alt="Wazuh SIEM Architecture" width="850">
</p>

### Overview

This project focuses on defensive security by deploying a complete Wazuh SIEM environment capable of collecting logs, monitoring Linux systems, and detecting suspicious activity across multiple hosts.

The objective was to understand how security monitoring works in practice by building a centralized platform for visibility, analysis, and incident detection.

### Architecture

> *(Architecture diagram placeholder)*

### Engineering Highlights

| Category | Implementation |
|-----------|----------------|
| SIEM Platform | Wazuh |
| Infrastructure | Ubuntu Server |
| Monitored Endpoint | Kali Linux |
| Monitoring | Agent-Based |
| Security | Log Collection & Event Analysis |
| Deployment | Linux Environment |

### Key Takeaways

- Deployed and configured a complete Wazuh SIEM environment.
- Connected Linux agents for centralized monitoring.
- Learned how security events are collected and analyzed.
- Improved visibility into infrastructure activity.
- Built practical experience with defensive security operations.

### Repository

- 📂 **Repository:** https://github.com/yourusername/your-repository
- 📖 **Documentation:** https://github.com/yourusername/your-repository/tree/main/docs

</details>

---

<details>
<summary>

### 🌐 Linux Router & Network Infrastructure
*Linux Routing • nftables • DHCP • DNS • Open vSwitch*

</summary>

<br>

> **A Linux server transformed into a complete network router to understand networking from first principles.**

<p align="center">
  <img src="images/router-architecture.png" alt="Linux Router Architecture" width="850">
</p>

### Overview

This project transforms a Linux machine into a fully functional router responsible for forwarding traffic between isolated networks while providing essential infrastructure services.

Instead of relying on dedicated networking appliances, the project explores how Linux performs routing, firewalling, packet forwarding, DHCP, DNS, NAT, and VLAN segmentation internally.

### Architecture

> *(Architecture diagram placeholder)*

### Engineering Highlights

| Category | Implementation |
|-----------|----------------|
| Routing | Linux IP Forwarding |
| Firewall | nftables |
| DHCP | ISC DHCP Server |
| DNS | Bind9 |
| VLANs | Open vSwitch |
| Operating System | Ubuntu Server |

### Key Takeaways

- Understood how Linux makes routing decisions.
- Configured packet forwarding between isolated networks.
- Built firewall policies using nftables.
- Deployed DHCP and DNS services.
- Designed segmented network architectures using VLANs.
- Troubleshot routing, NAT, firewall, and connectivity issues.

### Repository

- 📂 **Repository:** https://github.com/yourusername/your-repository
- 📖 **Documentation:** https://github.com/yourusername/your-repository/tree/main/docs

</details>

---

## ⚙️ Engineering Experience

### 🐧 Linux Systems

Ubuntu Server • Kali Linux • Users & Groups • Permissions • systemd • Package Management • Storage • Networking

---

### 🌐 Networking

TCP/IP • IPv4 Addressing • Routing • DHCP • DNS (Bind9) • NAT • VLANs • Open vSwitch

---

### 🔐 Infrastructure Security

OpenSSH • Public Key Authentication • ProxyJump • Bastion Hosts • nftables • Zero Trust

---

### 🛡️ Security Monitoring

Wazuh SIEM • Linux Agents • Log Collection • Event Analysis

---

### 📦 Containers

Docker • Docker Compose

---

### 📚 Documentation

Architecture Diagrams • Technical Reports • Deployment Guides • Troubleshooting Documentation

---

## 🎯 Current Learning Journey

I believe engineering is a continuous process of learning, experimenting, and refining. My roadmap reflects the areas I am currently exploring through practical projects and technical documentation.

### ✅ Foundations

- Linux Administration
- Networking Fundamentals
- SSH & Infrastructure Security
- Docker
- Terraform
- Wazuh SIEM

### 🚧 Currently Exploring

- Linux Privilege Escalation
- Linux Security
- Cloud Security
- Infrastructure Hardening

### 🎯 Next Objectives

- Kubernetes
- Ansible
- DevSecOps
- Detection Engineering
- AWS Professional Certifications

---

## 📂 Repository Guide

If you're interested in exploring my work, I recommend starting with these repositories:

| Repository | Description |
|------------|-------------|
| 🛡️ Zero Trust SSH Bastion | Secure SSH architecture built around Zero Trust principles. |
| 🔍 Wazuh SIEM Lab | Centralized security monitoring and defensive security laboratory. |
| 🌐 Linux Router & Network Infrastructure | Linux router providing routing, DHCP, DNS, VLANs, and firewalling. |
| 🧪 Infrastructure Labs | A growing collection of focused experiments covering Linux, networking, and security concepts. |

---

## 🤝 Connect

- 💼 LinkedIn: *(Add your LinkedIn URL)*
- 📧 Email: *(your.email@example.com)*

---

> *"Building infrastructure from first principles."*
