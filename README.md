# 🔍 Sysmon Event Log Analysis using Windows Event Viewer

## 📌 Project Overview

This project demonstrates the installation and analysis of **Sysmon (System Monitor)** logs using **Windows Event Viewer** in a VirtualBox Windows environment.

Sysmon is a Microsoft Sysinternals tool that provides detailed system activity monitoring. It helps SOC analysts investigate endpoint activities, detect suspicious behavior, and perform security analysis.

---

## 🎯 Objectives

- Install Sysmon on Windows
- Explore Sysmon Event Logs
- Understand important Event IDs
- Analyze endpoint activities
- Learn SOC-level log investigation
- Monitor Windows system behavior

---

## 🖥️ Lab Environment

| Component | Details |
|---|---|
| Operating System | Windows 10 / Windows 11 |
| Monitoring Tool | Sysmon |
| Log Viewer | Windows Event Viewer |
| Shell | PowerShell |
| Log Location | Sysmon Operational Log |

---

## ⚙️ Sysmon Installation

Sysmon was installed using Administrator PowerShell.

Command used:

```powershell
.\Sysmon64.exe -accepteula -i
```

After installation, Sysmon service was verified successfully.

---

## 📂 Sysmon Log Location

Open:

```
Event Viewer

↓

Applications and Services Logs

↓

Microsoft

↓

Windows

↓

Sysmon

↓

Operational
```

---

# 💻 PowerShell Testing

PowerShell was used to generate system activities and create Sysmon logs.

## Process Creation Testing

Open applications:

```powershell
notepad
```

```powershell
cmd
```

```powershell
powershell
```

These activities generated Sysmon process creation logs.

---

# 🔎 Event IDs Analyzed

| Event ID | Description |
|---|---|
| 1 | Process Creation |
| 2 | File Creation Time Changed |
| 3 | Network Connection |
| 5 | Process Terminated |
| 6 | Driver Loaded |
| 7 | Image Loaded |
| 8 | Create Remote Thread |
| 10 | Process Access |
| 11 | File Created |
| 12 | Registry Object Created/Deleted |
| 13 | Registry Value Set |
| 15 | File Stream Created |
| 22 | DNS Query |

---

# 🧪 Event Investigation

## Event ID 1 - Process Creation

Observed:

- Process Name
- Process ID
- Parent Process
- Command Line
- User Account
- File Path
- Hash Information

Purpose:

Used to identify suspicious program execution.

---

## Event ID 3 - Network Connection

Observed:

- Source IP
- Destination IP
- Port Number
- Process Name
- User

Purpose:

Used for network activity monitoring and threat detection.

---

## Event ID 11 - File Creation

Observed:

- File Name
- File Path
- User
- Timestamp

Purpose:

Used to detect suspicious file creation.

---

## Event ID 13 - Registry Modification

Observed:

- Registry Key
- Registry Value
- Process Name

Purpose:

Used to identify persistence techniques.

---

## Event ID 22 - DNS Query

Observed:

- Query Name
- Process
- User

Purpose:

Used to monitor domain requests.

---

# 📸 Screenshots

Add screenshots:

```
Screenshots/

├── sysmon-installation.png
├── sysmon-service.png
├── operational-log.png
├── event-id-1.png
├── event-id-3.png
├── event-id-11.png
├── event-id-13.png
└── event-id-22.png
```

---

# 🛡️ SOC Use Cases

- Endpoint Monitoring
- Threat Hunting
- Malware Analysis
- Incident Response
- Process Investigation
- Network Monitoring
- Windows Forensics

---

# 🧠 Skills Learned

- Sysmon Installation
- Windows Event Viewer
- Log Analysis
- PowerShell Usage
- Endpoint Detection
- Security Monitoring
- SOC Investigation

---

# 🚀 Future Improvements

- Sysmon Configuration Rules
- Wazuh Integration
- Splunk Dashboard
- Sigma Rule Detection
- MITRE ATT&CK Mapping
- Automated Alert Creation

---

# 📁 Project Structure

```
Sysmon-Event-Analysis/

│── README.md
│── REPORT.md
│── Screenshots/
│     ├── installation.png
│     ├── logs.png
│     └── event-analysis.png
```

---
