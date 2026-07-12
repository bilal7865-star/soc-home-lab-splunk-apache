# SOC Analyst Home Lab: Splunk + Apache Detection Pipeline

<img width="1366" height="768" alt="Screenshot From 2026-07-11 17-54-56" src="https://github.com/user-attachments/assets/e7559b7d-4340-46fc-92e7-ea6e14a4a41f" />


A hands-on Security Operations Center (SOC) home lab built on Kali Linux. This project demonstrates a complete detection and response pipeline from attack simulation to alerting.

## 🎯 Project Objective

To build and showcase a functional SOC pipeline:
**Web Attack → Log Ingestion → SIEM Detection → Automated Webhook Alerting**

## 🛠️ Technology Stack

- **Operating System**: Kali Linux
- **Web Server**: Apache2
- **SIEM**: Splunk Enterprise (Free Trial)
- **SOAR**: Shuffle (Self-hosted)
- **Future**: Jira Integration (in progress)

## ✅ What Was Successfully Implemented

### Phase 1: Log Ingestion
- Deployed Apache2 web server on Kali Linux
- Configured real-time monitoring of `/var/log/apache2/access.log` in Splunk
- Resolved file permission issues for the `splunk` user

### Phase 2: Threat Detection
- Simulated real-world web attacks (directory traversal, reconnaissance, admin panel scanning)
- Built and tested Splunk detection alert for suspicious HTTP requests
- Alert successfully triggers on malicious patterns

### Phase 3: Alert Automation
- Configured Splunk Webhook action
- Successfully forwarded alerts to Shuffle SOAR
- Verified webhook delivery through execution tracking

## 📸 Screenshots

<img width="1366" height="768" alt="Screenshot From 2026-07-10 18-50-31" src="https://github.com/user-attachments/assets/d5655970-8def-4bec-af42-40f939cca230" />
<img width="1366" height="768" alt="Screenshot From 2026-07-10 18-50-38" src="https://github.com/user-attachments/assets/a21f79d6-dce3-4ac9-a11d-21ecd6fdce5f" />
<img width="1366" height="768" alt="Screenshot From 2026-07-11 17-57-22" src="https://github.com/user-attachments/assets/bf20d071-d895-443b-8429-266150ac1b00" />
<img width="1366" height="768" alt="Screenshot From 2026-07-11 17-55-22" src="https://github.com/user-attachments/assets/620b005a-6814-49b0-afa0-9f4888cb9d1e" />


## 📚 Documentation

- [Setup Commands](docs/setup-commands.md)
- [Detection Queries](docs/detection-queries.md)

## 🔄 Next Steps

- Fix Shuffle login issue to complete SOAR workflow
- Implement automatic Jira ticket creation
- Add Splunk dashboards and visualizations
- Expand detections (network, file integrity, etc.)

## 💡 Key Learnings

- Practical log management and ingestion in Splunk
- Writing effective detection rules
- Understanding SIEM-SOAR integration using webhooks
- Building and troubleshooting a home lab environment

---

**Built as part of my SOC Analyst learning journey.**

**Last Updated:** July 2026
