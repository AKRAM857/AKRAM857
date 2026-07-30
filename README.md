# Akram Khoulid

> **Building infrastructure from first principles.**

I build secure infrastructure by combining Linux, networking, and security into production-inspired environments.

Currently pursuing a degree in **Networks & Telecommunications Engineering at ENSA Safi**, I focus on understanding systems from the ground up — how they're built, how they communicate, how they fail, and how to secure them.

Rather than treating projects as isolated exercises, I use them to explore real engineering concepts, solve practical problems, and document the knowledge I gain throughout the process.

---

## Engineering Philosophy

I believe good infrastructure is built on understanding rather than memorization.

Instead of learning technologies in isolation, I prefer building complete environments where every component has a purpose and every design decision can be explained.

My projects follow a simple philosophy:

- Build from first principles.
- Understand every layer of the system.
- Design security into the architecture.
- Document both implementation and reasoning.
- Continuously improve existing projects as my knowledge grows.

> *I don't collect technologies. I build systems, understand them, and document the lessons learned.*

---

## 📁 Featured Projects

> These projects represent my current engineering portfolio. Each repository contains architecture diagrams, technical documentation, implementation details, and lessons learned.

---

<details>
<summary><strong>🛡️ Secure-SSH-Bastion-Infrastructure </strong> — OpenSSH · ProxyJump · nftables · RBAC · fail2ban · Permissions · Groups · auditd</summary>

<br>

A production-inspired secure access infrastructure built from scratch in VirtualBox. Rather than exposing internal servers directly, all administrative access is centralized through a hardened Bastion Host that enforces authentication, network segmentation, and access control before any connection reaches internal systems.

Every architectural decision is documented with its security reasoning — not just what was configured, but why.

### What makes this different

- Dual-interface network architecture — public `enp0s3` and private `enp0s8` enforcing physical segment isolation between the exposed and internal networks
- SSH daemon hardened to keys-only authentication — passwords disabled entirely, root login disabled, access restricted to defined groups
- ProxyJump blind tunneling — the Bastion forwards connections to internal servers without ever holding credentials for them; the private key never leaves the administrator's machine
- nftables stateful ruleset with default-drop policy — port 22 only inbound, all other traffic silently dropped at the kernel level before any application sees it
- RBAC with three engineering teams — `devs`, `ops`, and `auditors` — each with precisely scoped filesystem permissions and sudo policies that enforce least privilege
- fail2ban integrated with nftables — automated IP banning after 5 failed authentication attempts within 60 seconds; banned IPs are rejected at the network layer before SSH processes them
- Accompanied by a 70+ page technical report documenting every architectural decision, security reasoning, configuration choice, and troubleshooting session

📂 **Repository:** https://github.com/AKRAM857/zero-trust-infrastructure

</details>

---

<details>
<summary><strong>🛡️ Infrastructure Security Automation Framework</strong> — Ansible · nftables · Jinja2 · Linux Hardening · Threat Modeling · Infrastructure as Code</summary>

<br>

An enterprise-focused security engineering framework that automates Linux server hardening and role-based firewall deployment using Ansible. Instead of applying generic security configurations, every policy is designed from a documented threat model, translated into security requirements, implemented through reusable Ansible roles, and validated using security assessment tools.

The framework provides a common hardening baseline alongside specialized security profiles for Web, Database, and Management servers, allowing the same automation to adapt to different infrastructure roles without modifying the core implementation.

### What makes this different

* Security-first engineering workflow — every firewall rule and hardening policy originates from a documented threat model before any automation is written
* Role-based security profiles — independent security policies for Web, Database, and Management servers, each minimizing its own attack surface
* Reusable Ansible architecture — modular roles, inventories, variables, handlers, and Jinja2 templates designed for scalable Infrastructure as Code deployments
* Dynamic nftables generation — a single Jinja2 template produces different firewall rulesets based on server role, interfaces, ports, and trusted management networks
* Enterprise Linux hardening baseline — SSH hardening, kernel security parameters, user and privilege management, and system-wide security configurations shared across every server
* Validation-driven implementation — every security profile is verified through idempotency testing, Nmap network scanning, and Lynis security auditing to demonstrate that the deployed policies behave exactly as intended
* Accompanied by a comprehensive technical report documenting the security methodology, threat models, firewall engineering decisions, Ansible architecture, implementation details, validation procedures, and lessons learned throughout the project

📂 **Repository:** https://github.com/AKRAM857/infrastructure-security-automation-framework

</details>

---

<details>
<summary><strong>🌐 Linux Router & Network Infrastructure</strong> — Routing · DHCP · DNS · VLANs · Open vSwitch</summary>

<br>

A Linux server configured as a complete software-defined network router. Built to understand routing, packet forwarding, and core network services from first principles rather than relying on preconfigured appliances.

### What makes this different

- Single Ubuntu VM acting as a full router — DHCP server, BIND9 authoritative DNS, NAT masquerading, and inter-VLAN routing simultaneously
- Open vSwitch VLAN trunking with tagged ports and internal bridge interfaces separating network segments
- Kali Linux and Alpine Linux clients assigned to separate VLANs with controlled inter-VLAN routing

📂 **Repository:** https://github.com/AKRAM857/Implementing-a-Linux-Router-with-DHCP-and-DNS-Services

</details>

---

## ⚙️ Technical Stack

| Domain | Technologies |
|---|---|
| Linux | Ubuntu Server · Kali Linux · systemd · users & groups · file permissions · auditd · rsyslog |
| Security | OpenSSH · nftables · fail2ban · Zero Trust · RBAC · sudo policy · least privilege |
| Networking | TCP/IP · NAT · VLAN · DHCP · DNS · Open vSwitch · Netfilter · stateful inspection |
| Monitoring | Wazuh XDR · SIEM · MITRE ATT&CK · log analysis · threat detection |
| Containers | Docker · Docker Compose |
| Documentation | 100+ page technical reports · architecture diagrams · troubleshooting logs |

---

## 🎯 Current Learning Journey

I believe engineering is a continuous process of learning through experimentation and practical implementation.

### Solid Foundations

- Linux Administration
- Networking Fundamentals
- SSH & Infrastructure Security
- Docker
- Wazuh SIEM

### Currently Exploring

- Linux Security & Privilege Escalation
- Infrastructure Hardening
- Web Servers — Apache & Nginx
- nftables & Firewall Design

### Next Milestone

**Enterprise Core Infrastructure** — a self-contained production-inspired environment built around the services every company depends on.

| Service | Purpose |
|---|---|
| DNS & DHCP | Internal name resolution and address management |
| LDAP | Centralized identity and authentication |
| PKI & CA | Internal certificate authority — HTTPS everywhere |
| Reverse Proxy | Single entry point for internal services |
| GitLab | Self-hosted source control and CI/CD |
| Monitoring | Infrastructure observability |
| Logging | Centralized log aggregation |
| Backups | Automated backup policy |
| Automation | Configuration management across all services |

Every service integrates with the others. LDAP authenticates GitLab. PKI signs certificates for HTTPS. The reverse proxy fronts everything. Monitoring watches it all.

The same methodology as the bastion project — built from first principles, every decision documented.

---

## 📚 Beyond Featured Projects

In addition to my main repositories, I maintain a growing collection of smaller laboratories and experiments focused on understanding individual concepts in greater depth.

Topics include:

- Linux Administration
- SSH
- nftables & Firewall Design
- Networking
- Docker
- Web Servers
- Privilege Escalation
- Security Experiments

These repositories serve as an engineering notebook where I explore technologies from first principles before integrating them into larger projects.

---

## 🤝 Connect

- 💼 LinkedIn: https://www.linkedin.com/in/akram-khoulid-08aa4435a/
- 📧 Email: akramkhoulid47@gmail.com

---

> **Building infrastructure from first principles.**
