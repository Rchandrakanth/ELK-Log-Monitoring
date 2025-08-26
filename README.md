# ELK Log Monitoring Platform

[![ELK](https://img.shields.io/badge/ELK-Stack-orange)]()
[![OSSEC](https://img.shields.io/badge/OSSEC-HIDS-blue)]()
[![Suricata](https://img.shields.io/badge/Suricata-IDS/IPS-red)]()
[![Nagios](https://img.shields.io/badge/Nagios-Monitoring-green)]()

---
📌 Project Overview

This project demonstrates the implementation of a SOC-like monitoring environment using the ELK Stack (Elasticsearch, Logstash, Kibana) integrated with Filebeat to collect, parse, and visualize logs from:

Nagios – Infrastructure & Service Monitoring

OSSEC HIDS – Host-based Intrusion Detection

Suricata IDS/IPS – Network Intrusion Detection & Prevention

The goal is to enable centralized log monitoring, real-time visualization, and alert correlation for security and infrastructure events.

⚙️ Architecture

Nagios: Monitors system health (CPU, memory, services, load, etc.) and sends alerts.

OSSEC HIDS: Monitors host activities, logs, and file integrity with agent-server communication.

Suricata IDS/IPS: Detects & logs suspicious/malicious network traffic (e.g., ICMP flood, port scans).

Filebeat: Forwards logs from each tool into Logstash → Elasticsearch → Kibana Dashboard.

🔹 Tools Used

Nagios Core: Service & Host Monitoring

OSSEC HIDS v3.7.0: Host-based Intrusion Detection

Suricata IDS/IPS: Network Threat Detection

ELK Stack (Elasticsearch, Logstash, Kibana): Centralized log storage & visualization

Filebeat: Log shipping

📊 Sample Dashboards & Logs
1️⃣ Nagios Integration

Collected Nagios alerts (service failures, high load, HTTP/SSH monitoring).

Visualized Nagios logs in Kibana.

2️⃣ OSSEC HIDS Integration

OSSEC server-agent setup with log forwarding.

Detects suspicious login attempts, server restarts, and file integrity violations.

Alerts sent to ELK for centralized monitoring.




3️⃣ Suricata IDS/IPS Integration

Suricata configured to log suspicious traffic (ICMP floods, scans).

Logs parsed and visualized in Kibana.






🚀 How It Works

Nagios, OSSEC, and Suricata generate logs locally.

Filebeat collects these logs and forwards them to Logstash.

Logstash parses and normalizes the logs.

Elasticsearch indexes the logs.

Kibana provides real-time dashboards and visualization.
