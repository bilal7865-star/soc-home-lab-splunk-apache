# SOC Analyst Home Lab: Splunk + Apache Detection Pipeline

A practical Security Operations Center (SOC) home lab built on Kali Linux. This project demonstrates a functional detection pipeline from web attack simulation to automated alerting.

## Project Overview

**Pipeline**: Web Attack → Apache Logs → Splunk Detection → Webhook Alert (Shuffle SOAR)

This lab was built to strengthen my skills in log ingestion, detection engineering, and SIEM-SOAR integration.

## Tools Used

- **Kali Linux** (host OS)
- **Apache2** (web server + log source)
- **Splunk Enterprise** (SIEM)
- **Shuffle SOAR** (Automation - partially configured)
- **Jira** (planned)

## Achievements

### Completed
- ✅ Apache2 web server setup with proper logging
- ✅ Real-time log ingestion into Splunk (`apache:access` sourcetype)
- ✅ Custom Splunk alert for suspicious web activity (directory traversal, reconnaissance)
- ✅ Webhook integration from Splunk to Shuffle SOAR
- ✅ Successful alert triggering and webhook delivery

### In Progress
- Full SOAR workflow automation
- Automatic Jira ticket creation

## Screenshots

See the [`Screenshots/`](Screenshots/) folder for visual documentation.

## Documentation

- [Setup Commands](docs/setup-commands.md)
- [Detection Queries & Alert Configuration](docs/detection-queries.md)

## Key Learnings

- Handling file permissions for log monitoring
- Writing effective Splunk SPL queries
- Understanding webhook-based SIEM to SOAR integration
- Troubleshooting services in a home lab environment

## Future Enhancements

- Complete Shuffle SOAR workflow
- Add Jira ticket creation action
- Build Splunk dashboards
- Expand to more log sources (auth.log, Suricata, etc.)

---

**Last Updated:** July 2026  
Built as part of my SOC Analyst self-learning journey.
