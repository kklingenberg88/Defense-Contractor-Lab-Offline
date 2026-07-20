This Project outline is for an automated offline Governance, Risk, and Compliance platform that consolidates vulnerability data, compliance assessments, asset inventories, and remediation activities into a centralized evidence repository. Through scheduled automation, the platform normalizes data from multiple security tools, correlates duplicate findings, maps vulnerabilities to compliance frameworks, calculates organizational risk, generates POA&Ms, and presents executive dashboards for continuous monitoring and audit readiness.

# Offline GRC Automation Platform

## Overview

The Offline GRC Automation Platform is a centralized Governance, Risk and Compliance solution designed for isolated and air-gapped environments.
Its purpose is to automate the collection, normalization, correlation and presentation of security data across multiple compliance frameworks while maintaining a single source of truth. 

You will use scripts to run tools, generate security data and create spreadsheets.
Those spreadsheets will be fed into a network drive as a single source of truth. The sharepoint that uses these documents in this repository are presented through Power BI. Those will create 6 dashboards that technicians, engineers and executives can use to strategize company objectives and the CISO's security vision.

## Objectives

- Automate vulnerability collection
- Correlate duplicate findings
- Track patch compliance
- Generate executive dashboards
- Produce audit evidence
- Simplify POA&M management

```
             Scheduled Tasks

  				    │

        ┌───────────┴───────────┐

        │                       │

  Security Tools          Asset Collection

        │                       │

        └───────────┬───────────┘

		            │

             Data Normalization

                    │

           Master Evidence Store

                    │

      ┌─────────────┴─────────────┐

      │             │             │

 Compliance     Risk Engine   Asset Engine

      │             │             │

      └─────────────┬─────────────┘

                    │

          Executive Dashboards

```


Our project's core principle is "Single source of truth". We accomplish this with a Master spreadsheet.
What is functioning behind the scenes is a lot of automation to compiling information.
Create templates through powershell script parser, extracting highly useful information to a condensed XLSM book, assembling information across multiple spreadsheets in the archieve, and finally integrating them with Power BI to create dashboards.

Once an internal soft architecture has been created, we streamline the process for Data collection and Processing.
Below is a quick explaination of what the master spreadsheet will be:

1st Page will have condensed findings and actionable items pulled from others
Overall Compliance, Risk Score, Critical findings, Patch Compliance, Open POAMs

2nd Page > References findings among all books with a vulnerability score and remediation steps
This functions as the source of truth, and has cross referenced findings with evidence

3rd Page > Nessus findings that reference endpoint, CVSS and CVE

4th Page > STIG/SCAP findings reporting the same information for cross reference on book 3

5th Page > Windows Version/Patch Status for endpoints

**This will have 4 total spreadsheets feeding into it.
   
