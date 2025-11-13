## Endpoint Hardening

This project demonstrates practical endpoint hardening on both Windows and Linux systems.
It includes security baselines, configuration changes, validation steps, and evidence showing how systems were strengthened against common attack vectors.

## 🎯 Objectives

- Build Windows & Linux hardening baselines
- Apply secure configuration changes
- Validate results using system and security tools
- Capture before/after evidence
- Strengthen systems against misconfigurations commonly exploited by attackers

## 📁 What’s Inside
- docs/ - Baselines, checklists, templates
- lab/ - Validation outputs, screenshots, before/after comparisons
- scripts/ - Optional auditing and configuration scripts
- .github/ - Issue/PR templates

## 🧪 Lab Setup (Quick Start)

**Host:**
- Proxmox
- VMware
- VirtualBox
- Hyper-V

**Operating Systems:**
- Windows: Windows 10/11 or Server 2019
- Linux: Ubuntu 22.04 / Debian / CentOS

**Network:**
- Segmented VLANs using pfSense/OPNsense
- Optional: AD Domain for GPO-based Windows hardening

**Tools Used:**

- Windows
  - Sysinternals Suite
  - PowerShell 7
  - Microsoft Security Baselines
  - Local Group Policy Editor (gpedit.msc)
  - secedit / gpresult

- Linux
  - Lynis
  - auditd
  - UFW / ipTables
  - sysctl

Some validation steps integrate with Repo 1 Sentinel logs when cloud ingestion is enabled.

## 🔐**Hardening Focus Areas** -  **Windows**
- Local policies (LSA protection, RDP restrictions)
- Attack surface reduction
- PowerShell logging
- Credential Guard / Device Guard
- SMB signing
- Firewall configuration
- Secure user rights assignments
- Removing unnecessary roles/features

## 🔐**Hardening Focus Areas** - **Linux**
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
- Capture:
  - before/after screenshots
  - policy reports
  - mitigation status results

**Linux Validation**

Run:

- sudo lynis audit system
- sudo ufw status
- cat /etc/ssh/sshd_config
- sudo sysctl -a

Upload outputs/screenshots into lab/.
- include:
  - Lynis audit results
  - SSH configuration changes
  - sysctl kernel hardening
  - firewall rule status

## 📊 Deliverables
✅ Windows Hardening Baseline

✅ Linux Hardening Baseline

✅ Before/after screenshots

✅ Validation reports (PowerShell, Lynis, auditd)

✅ Architecture diagram (optional)

✅ Scripts (Windows auditing / Linux auditing)

## 🧠 What I Learned
- Bullet points of concepts/skills you gained - Write what you learned about permissions, policies, configs.
- How attackers abuse weak configurations
- How to apply secure baselines without breaking functionality
- How Windows policies map to enterprise standards
- How Linux security differs from Windows
- How to validate hardening and measure improvement
- Understanding the principle of least privilege (PoLP)
- How to document system changes clearly and professionally

## ✅ Next Steps
- Add Active Directory GPO hardening
- Apply Microsoft’s official security baselines
- Add CIS Level 1 / Level 2 benchmark comparisons
- Automate validation checks with PowerShell/Bash
- Add scripts to automatically export baseline configs
- Extend to macOS hardening (optional)

## ⚖️ License
MIT – see `LICENSE`.
