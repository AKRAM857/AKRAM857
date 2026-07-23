<div align="center">

# Akram Khoulid

**Networks & Telecommunications Engineering Student**
École Nationale des Sciences Appliquées — Safi · Université Cadi Ayyad

*I build infrastructure from scratch, break it deliberately, and document everything I learn.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akram-khoulid-08aa4435a/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AKRAM857)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:akhoulid@gmail.com)

</div>

---

## About

I'm a third-year Networks & Telecom engineering student focused on the intersection of Linux systems administration, network security, and infrastructure hardening. My learning method is simple: build real systems, understand every layer, document the reasoning behind every decision.

I don't follow tutorials. I build things from first principles — then I break them and understand why they broke.

**Current focus:** Linux infrastructure security, stateful firewalling, SSH hardening, Zero-Trust access control, and intrusion detection.

**Career direction:** DevSecOps · Infrastructure Security · Cloud Security Engineering

---

## Core Competencies

### 🖥️ Linux Systems Administration
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Kali](https://img.shields.io/badge/Kali_Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![systemd](https://img.shields.io/badge/systemd-000000?style=flat-square&logo=linux&logoColor=white)

User & group management · RBAC · File permissions · SUID/SGID · umask policy · auditd · PAM · service hardening

### 🔐 Security & Access Control
![SSH](https://img.shields.io/badge/OpenSSH-000000?style=flat-square&logo=openssh&logoColor=white)
![nftables](https://img.shields.io/badge/nftables-CC0000?style=flat-square&logo=linux&logoColor=white)
![fail2ban](https://img.shields.io/badge/fail2ban-FF6600?style=flat-square&logo=linux&logoColor=white)

Zero-Trust architecture · SSH cryptographic hardening · ProxyJump · stateful packet inspection · nftables · fail2ban · sudo policy design · least privilege enforcement

### 🌐 Networking & Infrastructure
![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?style=flat-square&logo=virtualbox&logoColor=white)
![Open vSwitch](https://img.shields.io/badge/Open_vSwitch-CC0000?style=flat-square&logo=linux&logoColor=white)

Network segmentation · NAT · VLAN · DHCP · DNS · routing · dual-interface bastion design · Netfilter/nftables · tcpdump

### ☁️ Cloud & DevOps
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

AWS security architecture · IAM · Security Groups · Docker · CI/CD pipelines · container security

### 🔍 Monitoring & Detection
![Wazuh](https://img.shields.io/badge/Wazuh-3D8CFF?style=flat-square&logo=wazuh&logoColor=white)
![OpenSearch](https://img.shields.io/badge/OpenSearch-005EB8?style=flat-square&logo=opensearch&logoColor=white)

SIEM/XDR · threat detection · MITRE ATT&CK · log analysis · intrusion detection · brute force simulation

---

## Featured Projects

### 🏰 Zero-Trust SSH Bastion Host Infrastructure
> *The flagship project — a complete enterprise-grade secure access environment built from scratch*

A hardened multi-user SSH bastion host simulating an enterprise perimeter gateway. Built on VirtualBox with dual-interface network segmentation, this project implements every layer of a real Zero-Trust access model.

**What it covers:**
- Dual-interface network architecture — public `enp0s3` and private `enp0s8` with IP forwarding and NAT masquerade
- SSH daemon hardening — key-only auth, ProxyJump blind tunneling, AllowGroups enforcement
- Role-Based Access Control — three engineering teams (devs, ops, auditors) with precisely scoped filesystem permissions and sudo policies
- Stateful firewall with nftables — BastionRules table, input/forward/output chains, connection tracking
- Intrusion detection — fail2ban with SSH and Apache jail configuration
- Kernel audit telemetry — auditd recording all privileged commands
- 70+ page technical report documenting every architectural decision and its reasoning

**Stack:** Ubuntu 25.10 · Kali Linux · OpenSSH · nftables · fail2ban · auditd · Apache · VirtualBox

**Concepts:** Zero Trust · SSH cryptography · ProxyJump · RBAC · stateful packet inspection · least privilege · blast radius containment

---

### 🌐 Linux Router with DHCP, DNS & SDN
> *Full software-defined network built on a single Ubuntu VM*

Ubuntu VM configured as a complete network router handling DHCP address assignment, BIND9 DNS resolution, Open vSwitch VLAN segmentation, NAT masquerading, and inter-VLAN routing for Kali Linux and Alpine Linux clients.

**Stack:** Ubuntu · Open vSwitch · isc-dhcp-server · BIND9 · iptables · VirtualBox

**Concepts:** SDN · DHCP · DNS · NAT · VLAN · inter-VLAN routing · network troubleshooting

---

### 🔒 Wazuh SIEM Lab — Threat Detection & Incident Analysis
> *Complete XDR/SIEM deployment with real attack simulation and detection*

Full Wazuh v4.14.4 XDR/SIEM deployment on Ubuntu, monitoring a Kali Linux attack machine over a custom OVS/VLAN network. Simulated SSH brute force attack and detected **44,000+ alerts** in the dashboard. Analyzed events against MITRE ATT&CK framework.

**Stack:** Wazuh v4.14.4 · Filebeat OSS · OpenSearch 7.10.2 · Ubuntu · Kali Linux

**Concepts:** SIEM · XDR · threat detection · MITRE ATT&CK · log analysis · brute force simulation · incident response

---

## Knowledge Base

I maintain a structured personal knowledge base across all domains I study. Every concept is documented after being understood and tested — not before.

| Document | Status | Covers |
|---|---|---|
| Linux Systems Administration | Active · 33+ pages | Filesystem · users · groups · permissions · services · systemd |
| SSH — Protocol & Theory | Active | Cryptography · key exchange · ProxyJump · hardening |
| Firewall & Network Security | Active | Netfilter · nftables · stateful inspection · fail2ban |
| Bastion Host Project Report | Active · 70+ pages | Full implementation documentation with architecture diagrams |

---

## Learning Philosophy

> *"The best way to learn is to break things, understand why they broke, and document everything."*

I don't separate learning from doing. Every project produces:
- A working system I can demonstrate
- A technical report documenting the reasoning behind every decision
- A knowledge base entry explaining the theory behind what was implemented

The goal is not to know commands. The goal is to understand systems deeply enough to design, secure, and troubleshoot them under pressure.

---

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=AKRAM857&show_icons=true&theme=dark&hide_border=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=AKRAM857&layout=compact&theme=dark&hide_border=true)

</div>
