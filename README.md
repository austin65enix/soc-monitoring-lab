# SOC Monitoring Lab

An architect-level SOC monitoring lab demonstrating how availability,
security visibility, network analysis, incident forensics, and long-term
maintainability can be integrated into a single operational model.

---

## Architecture Overview

<a href="images/architecture-overview.svg">
  <img src="images/architecture-overview-optimized.svg" width="900">
</a>

---

## Architecture Design

This lab is designed as a **three-layer integrated Monitoring + SIEM architecture**.

### 1) Detection & Monitoring Layer
Zabbix, Wazuh, and Zeek focus on detecting availability issues, host-level security events,
and network behavior anomalies from different perspectives.

### 2) Event & Forensics Layer
Graylog acts as the central event hub, aggregating logs and security events into a correlatable
timeline for incident investigation and root cause analysis.

### 3) Trends & Capacity Layer
Prometheus provides long-term metrics and trend visibility, supporting capacity planning and
distinguishing transient anomalies from systemic issues.

This layered design ensures clear responsibility separation, reduced alert fatigue,
and long-term maintainability.

---

## Core Components

- **Zabbix** – Availability and service monitoring
- **Wazuh** – Host-based security monitoring and auditing (HIDS)
- **Zeek** – Network traffic and behavior analysis
- **Graylog** – Centralized logging and incident forensics
- **Prometheus** – Performance trends and capacity planning
- **EDR** – Real-time endpoint detection and response

---

## Incident Workflow

<a href="images/incident-workflow.svg">
  <img src="images/incident-workflow.svg" width="900">
</a>

### Example Scenarios
1. Zabbix detects abnormal system or service behavior  
2. Wazuh / EDR identify suspicious host activity  
3. Zeek provides network-level evidence (DNS / connections)  
4. Graylog correlates events into a unified timeline  
5. Prometheus validates long-term trends vs. anomalies  

---

## Design Principles
- One tool, one responsibility
- Correlatable and traceable incidents
- Focus on long-term maintainability and handover readiness

---

## Maintenance SOP (High-Level)
- Daily: platform health checks (services / disk / resources)
- Weekly: alert quality review and noise reduction
- Monthly: retention & capacity review (rotation / storage)
- Quarterly: upgrades, backups, and restore drills

- ---

## Why SOC Implementations Often Fail

Many organizations invest heavily in SOC tools,
but still struggle with operational effectiveness.

### 1. Alert Fatigue
Too many isolated alerts without proper correlation.
Security teams spend time reviewing noise instead of real incidents.

### 2. No Clear Event Correlation
Logs are collected, but not structured into a meaningful timeline.
Root cause analysis becomes slow and reactive.

### 3. Tool-Centric, Not Architecture-Centric
Deploying multiple tools without defining:
- Ownership
- Data flow
- Responsibility boundaries
- Maintenance strategy

### 4. No Operational Sustainability
Without maintenance SOP, retention planning,
and alert tuning, SOC platforms degrade over time.

---

## How This Lab Addresses Those Problems

This SOC lab focuses on:

- Layered responsibility separation (Detection / Forensics / Trends)
- Event correlation through centralized logging
- Clear incident workflow design
- Long-term maintenance and handover readiness

The goal is not to replicate commercial SOC platforms,
but to demonstrate a sustainable SOC foundation architecture.

