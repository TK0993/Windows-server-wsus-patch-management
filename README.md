# Windows Server 202centralized Patch Management (WSUS) Lab

This repository documents the deployment, infrastructure provisioning, and architectural alignment of **Windows Server Update Services (WSUS)** on **Windows Server 2022**. 

Governing vulnerabilities, regulating update approval cycles, and staging software updates centralizes domain compliance control. This architecture establishes the foundation for enterprise endpoint configuration tools like MECM (SCCM), serving as a core responsibility during out-of-hours infrastructure operations.

---

## 🛠️ Infrastructure Core Components
* **Operating System:** Windows Server 2022 Datacenter Edition
* **Management Console:** Update Services Console (`wsus.msc`)
* **Automation Framework:** Windows PowerShell 5.1
* **Strategy Target:** Centralized Patch Caching & Metadata Synchronization

---

## 🏗️ Technical Execution & Framework Walkthrough

### 1. Automation-Driven Core Engine Provisioning
To streamline infrastructure staging, the WSUS update engine and its associated graphical administrative snap-ins were compiled programmatically via PowerShell, bypassing the multi-step Server Manager manual installation layout.
```powershell
# Command used to deploy the update ecosystem binaries
Install-WindowsFeature -Name UpdateServices -IncludeManagementTools
