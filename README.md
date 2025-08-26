# ELK Log Monitoring Platform

[![ELK](https://img.shields.io/badge/ELK-Stack-orange)]()
[![OSSEC](https://img.shields.io/badge/OSSEC-HIDS-blue)]()
[![Suricata](https://img.shields.io/badge/Suricata-IDS/IPS-red)]()
[![Nagios](https://img.shields.io/badge/Nagios-Monitoring-green)]()

---

## Project Overview
A SOC-style centralized monitoring platform using the ELK Stack to aggregate and visualize logs from critical security and infrastructure tools:
- **Nagios** — Monitors system/services health  
- **OSSEC HIDS** — Tracks host-based anomalies & integrity  
- **Suricata IDS/IPS** — Detects network threats

Provides unified visibility, rapid detection, and threat correlation in real time.

---

## Tech Stack

| Tool         | Purpose                             |
|--------------|-------------------------------------|
| Nagios       | Infrastructure & service health     |
| OSSEC HIDS   | Host-level intrusion detection      |
| Suricata     | Network-based anomaly detection     |
| Filebeat     | Log forwarding                      |
| Logstash     | Log parsing & normalization         |
| Elasticsearch| Central log indexing                |
| Kibana       | Data visualization & dashboards     |

---

## Architecture Diagram

*Optional: Add an architecture image illustrating data flow from agents (Nagios, OSSEC, Suricata) → Filebeat → Logstash → Elasticsearch → Kibana.*

---

## Setup & Deployment

```bash
# Clone repository
git clone https://github.com/Rchandrakanth/ELK-Log-Monitoring.git
cd ELK-Log-Monitoring

# Install & configure Nagios, OSSEC, Suricata (see individual setup files)
# Example: Launch Filebeat
filebeat -e -c filebeat.yml

# Start Logstash:
logstash -f logstash_pipeline.conf

# Launch Elasticsearch & Kibana (Docker-compose / local)
docker-compose up -d

# Access Dashboard
# Kibana: http://localhost:5601
```

Highlights & Capabilities

Scalable Monitoring: Collect logs across tools and centralize insights.

Structured Alerts: Detects issues like intrusion attempts, service failures, and malicious traffic.

Real-Time Dashboards: Visualize logs instantly using Kibana.

Modular Design: Easily add new log sources or visualization features.

