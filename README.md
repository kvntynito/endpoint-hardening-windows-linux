# <Project Title>

This project demonstrates practical endpoint hardening on both Windows and Linux systems.
It includes security baselines, configuration changes, validation steps, and evidence showing how systems were strengthened against common attack vectors.

## 🎯 Objectives
- Windows baseline
- Linux baseline
- Hardening steps
- Validation commands
- Screenshots of hardened settings

## 🧪 What’s Inside
A simple virtualized environment was used to apply and validate system hardening:
- Hypervisor: Proxmox / VMware / VirtualBox
- Windows VM: Windows 10/11 or Server 2019
- Linux VM: Ubuntu 22.04 / Debian / CentOS
- Network:
  - Segmented via pfSense/OPNsense
  - Optional: AD Domain for GPO hardening
- Tools Used:
  - Sysinternals Suite
  - PowerShell 7
  - Lynis (Linux)
  - auditd (Linux)
  - Local Group Policy Editor (Windows)
  - Windows Security Baselines (Microsoft)

## 🏗️ Lab Setup (Quick Start)
- Host: Proxmox/VMWare/Hyper-V/Docker (choose one)
- VMs: Windows Server 2019, Ubuntu 22.04, Kali
- Network: pfSense with two VLANs (Home / Lab)
- Cloud (optional): Azure free tier (Sentinel, Key Vault, Defender for Cloud)

🔐**Hardening Focus Areas** -  **Windows**
- Local policies (LSA protection, RDP restrictions)
- Attack surface reduction
- PowerShell logging
- Credential Guard / Device Guard
- SMB signing
- Firewall configuration
- Secure user rights assignments
- Removing unnecessary roles/features

🔐**Hardening Focus Areas** - **Linux**
- SSH hardening
- Password & account lockout policies
- File permissions
- Firewall (UFW/ipTables)
- auditd rules
- Disable unused services
- Kernel parameter hardening (sysctl)
- Log retention policies

## ▶️ How to Run (Validation Steps)
**Windows Validation**

Run these PowerShell commands:

- Get-ProcessMitigation
- Get-MpComputerStatus
- secedit /export /cfg baseline.cfg
- gpresult /h report.html

Document the results in lab/.

## 📊 Deliverables
- Link to your key reports (incident, vuln assessment, detections)
- Screenshots or short gifs (if any)

## 🧠 What I Learned
- Bullet points of concepts/skills you gained - Write what you learned about permissions, policies, configs.

## ✅ Next Steps
- Planned improvements or stretch goals

## ⚖️ License
MIT – see `LICENSE`.
