Welcome to the GRC Automation Project: Sentinel

# SentinelGRC

> **An open-source Governance, Risk, and Compliance (GRC) automation platform designed to collect technical evidence, normalize compliance data, correlate vulnerabilities, and generate actionable reporting across multiple cybersecurity frameworks.**

---

## Overview

SentinelGRC is a vendor-neutral GRC platform built to demonstrate how compliance programs can be implemented using open technologies instead of commercial governance platforms.

The project centralizes technical evidence from multiple sources into a normalized SQLite database, correlates findings across compliance frameworks, and produces technical and executive reporting suitable for governance, risk, and audit activities.

The objective is to separate **evidence collection** from **compliance mapping**, allowing a single technical assessment to satisfy multiple regulatory frameworks.

---

## Key Capabilities

* Asset Inventory Management
* Technical Compliance Validation
* Vulnerability Correlation
* Risk Register Support
* POA&M Generation
* Continuous Monitoring
* Historical Compliance Tracking
* Executive Reporting
* Power BI Integration
* SQLite Evidence Repository
* Multi-Framework Compliance Mapping

---

## Supported Compliance Frameworks

* CMMC 2.0
* NIST SP 800-53 Rev. 5
* NIST SP 800-171 Rev. 3
* NIST SP 800-172
* DISA STIG
* SCAP
* CIS Benchmarks

---

## Technology Stack

| Component               | Technology                      |
| ----------------------- | ------------------------------- |
| Primary Language        | PowerShell 7                    |
| Database                | SQLite                          |
| Reporting               | Microsoft Excel, HTML, Power BI |
| Configuration           | JSON                            |
| Documentation           | Markdown                        |
| Version Control         | Git / GitHub                    |
| Testing                 | Pester                          |
| Static Analysis         | PSScriptAnalyzer                |
| Development Environment | Visual Studio Code              |
| Data Formats            | XML, CSV, JSON, HTML            |

---

## Core Architecture

```text
Evidence Collection
        │
        ▼
Normalization Engine
        │
        ▼
SQLite Evidence Repository
        │
        ├── Compliance Mapping
        ├── Vulnerability Correlation
        ├── Risk Register
        ├── POA&M
        └── Historical Scan Data
                │
                ▼
Reporting Engine
        │
        ├── Excel
        ├── HTML
        ├── JSON
        └── Power BI
```

---

## Current Modules

* Asset Inventory
* Compliance Engine
* Framework Mapping
* Vulnerability Import
* STIG Processing
* SCAP Processing
* Risk Management
* Reporting
* Database Management
* Logging

---

## Repository Structure

```text
SentinelGRC/
├── Assets/
├── Checks/
├── Config/
├── Database/
├── Docs/
├── FrameworkMappings/
├── Logs/
├── Modules/
├── Reports/
├── SQL/
├── Tests/
└── Tools/
```

---

## Design Principles

* Collect evidence once and reuse it across multiple compliance frameworks.
* Normalize all technical findings into a common data model.
* Separate technical implementation from governance logic.
* Maintain a modular, plugin-based architecture.
* Favor open, portable technologies over proprietary platforms.
* Produce repeatable, auditable, and evidence-based reporting.

---

## Intended Audience

SentinelGRC is designed for:

* Governance, Risk, and Compliance (GRC) Teams
* Security Engineers
* Compliance Analysts
* Internal Audit
* DoD Contractors
* Managed Security Service Providers (MSSPs)
* Security Operations (SecOps)
* IT Administrators

---

## Project Status


The project is under active development and currently focuses on establishing the core platform architecture, evidence collection model, database design, compliance mappings, and reporting framework.

---

## Long-Term Vision

SentinelGRC aims to provide an extensible, open-source alternative to commercial GRC platforms by integrating technical evidence collection, vulnerability management, compliance assessment, risk management, and executive reporting into a single, vendor-neutral platform.
