# SOC Analyst Home Lab: Splunk + Apache Detection Pipeline

A practical, beginner-to-intermediate Security Operations Center (SOC) home lab built on a single Kali Linux machine. This project demonstrates a complete attack detection and alerting workflow.

## Project Goal

To simulate a real-world SOC detection pipeline:
**Web Attack → Log Ingestion → SIEM Detection → Automated Alerting**

## Tools & Technologies

- **OS**: Kali Linux
- **Web Server**: Apache2
- **SIEM**: Splunk Enterprise (Free 60-day trial)
- **SOAR**: Shuffle (self-hosted, open source)
- **Ticketing**: Jira (planned)

## What Was Achieved

### Phase 1: Infrastructure Setup
- Installed and configured Apache2 web server on Kali Linux
- Enabled proper logging (`/var/log/apache2/access.log`)
- Configured Splunk to monitor Apache access logs in real-time
- Added necessary permissions for the `splunk` user

### Phase 2: Attack Simulation & Detection
- Generated realistic malicious web traffic (directory traversal, common admin panel scanning, SQLi-like attempts)
- Created a working Splunk detection alert for suspicious web requests
- Alert successfully triggers on patterns such as:
  - Directory traversal attempts (`../../../etc/passwd`)
  - Reconnaissance on common paths (`phpmyadmin`, `.env`, `admin`)

### Phase 3: Alert Automation
- Configured Splunk Webhook alert action
- Successfully forwarded alerts to Shuffle SOAR via webhook
- Confirmed webhook delivery through execution tracking in Shuffle

## Repository Structure
