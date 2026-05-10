# Azure-Geo-Analytic-Workbooks

Azure Workbooks focused on geographic visualization, authentication analytics, and threat monitoring across Microsoft Azure, Microsoft Sentinel, and Entra ID.

## Overview

This repository contains custom Azure Workbooks designed to provide security teams with visual analytics and geographic intelligence for authentication events, malicious traffic, and VM access activity.

The workbooks help identify:

- Suspicious authentication attempts
- Geographic attack patterns
- Brute-force activity
- Malicious inbound traffic
- High-risk sign-in behavior
- VM authentication anomalies

---

# Workbooks

## 1. Malicious Traffic Entering the Network

<img width="1550" height="586" alt="Malicious Traffic Entering the Network" src="https://github.com/user-attachments/assets/62a141a0-43bf-4cf4-988c-2c6eafc8c201" />


### Description
Visualizes malicious inbound traffic attempting to access the environment using geo-mapping and threat analytics.

### Features
- Interactive world map of attacker IP locations
- Threat severity breakdown
- Protocol analytics
- Top malicious source countries
- Traffic trend timeline
- Blocked vs allowed traffic comparison

### Data Sources
- Microsoft Sentinel
- Azure Firewall Logs
- Defender for Cloud
- NSG Flow Logs

### Example Metrics
| Metric | Description |
|---|---|
| Source IP | Originating attacker IP |
| Country | Geo-location of source |
| Threat Type | Malware, brute force, scans |
| Severity | Low to Critical |
| Protocol | TCP / UDP |
| Action Taken | Allowed / Blocked |

---

## 2. Entra ID Authentication Failures

<img width="1605" height="571" alt="Entra ID Authentication Failures" src="https://github.com/user-attachments/assets/85ea9237-38c0-4008-966e-1d8e2748e66d" />


### Description
Tracks failed Entra ID sign-in attempts with geographic visualization and identity analytics.

### Features
- Failed sign-in heatmap
- MFA failure tracking
- Conditional access failures
- Risk-level visualization
- Top targeted accounts
- Authentication trend analysis

### Data Sources
- Microsoft Entra ID Sign-In Logs
- Microsoft Sentinel
- Identity Protection

### Example Metrics
| Metric | Description |
|---|---|
| User Principal Name | Targeted user |
| Failure Reason | Invalid password, MFA denied |
| Country | Source location |
| Application | Targeted application |
| Risk Level | Low / Medium / High |

---

## 3. VM Authentication Failures

<img width="1136" height="566" alt="VM Authentication Failures" src="https://github.com/user-attachments/assets/8a37783f-4bfc-4d04-81d6-d3ead18f7a63" />


### Description
Monitors failed authentication attempts against Azure virtual machines.

### Features
- SSH and RDP attack tracking
- Brute-force detection
- Source IP mapping
- Failed login timelines
- Critical VM targeting analysis
- Authentication method analytics

### Data Sources
- Azure Monitor
- Syslog
- Windows Security Events
- Microsoft Sentinel

### Example Metrics
| Metric | Description |
|---|---|
| VM Name | Targeted virtual machine |
| Username | Attempted username |
| Source IP | Originating IP |
| Auth Method | SSH / RDP |
| Failure Reason | Invalid credentials, expired password |
| Attempts | Number of failed attempts |

---

# Deployment

1. Open Azure Portal
2. Navigate to Azure Monitor or Microsoft Sentinel
3. Open Workbooks
4. Select Import
5. Upload workbook JSON file

---

# Requirements

- Microsoft Sentinel
- Azure Monitor Logs
- Microsoft Entra ID P1/P2
- Appropriate Log Analytics permissions

---

# Future Enhancements

- Threat intelligence integration
- Live attack feeds
- Geo-risk scoring
- User behavior analytics
- Dark mode optimized dashboards
- Cross-workspace support

---
Security Analytics & Azure Monitoring Project
