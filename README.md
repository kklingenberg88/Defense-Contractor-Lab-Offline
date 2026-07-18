# Defense-Contractor-Lab-Offline
This is a Project outline that is scalable to a multilab offline environment.
The need to adhere to multiple compliance standards including NIST 800-53, 171, 172 and CMMC

Base Description and Outline: You will use scripts to run tools, generate security data and create spreadsheets.
Those spreadsheets will be fed into a network drive for backup, into sharepoint for a main repository and presented through Power BI


Automate creation of separate spreadsheets and the import process to a Master XLSM
Process from raw data in a standard template form, to a condensed XLSM book, to dashboards
1st Page will have condensed findings and actionable items pulled from others
	&nbsp;Overall Compliance, Risk Score, Critical findings, Patch Compliance, Open POAMs
2nd Page > References findings among all books with a vulnerability score and remediation steps
	&nbsp;This functions as the source of truth, and eliminates duplicate entries
3rd Page > Nessus findings that reference endpoint, CVSS and CVE
4th Page > STIG/SCAP findings reporting the same information for cross reference on book 3
5th Page > Windows Version/Patch Status for endpoints
**This will have 4 total spreadsheets feeding into it.

Executive Dashboard - Pulls information from the following:
	&nbsp;Pulls from Master spreadsheet, this should have all of the linked information
	&nbsp;Current top of priorities can be communicated in meetings, make it quick and easy.
	&nbsp;Compliance, Risk, Critical findings, Open POAMs and Patch Compliance
	&nbsp;Overall Score percentage - weighted in accordance to their desires
	&nbsp;Bonus if it's at a click, and you can dive through each Dashboard for additional details

Vulnerability Dashboard
	&nbsp;Pulls from Master spreadsheet, pages 1 and 2
	&nbsp;Severity of threats and Quantity
	&nbsp;Layered graph for tiered threats: 1, 2 and 3 to display threat surface based on departments
	&nbsp;Monthly trends, should be decreasing over time

Compliance Dashboard
	&nbsp;Family of controls - Automate control checks via Powershell script, complete with a scoring
	&nbsp;Controls missed listed per endpoint, separated by Control family and Percent scores
	&nbsp;Percent Compliant: This goes across NIST, CMMC, SOC 2 etc.
		&nbsp;&nbsp;Pull from the compliance scores, and have a workbook per compliance standard
		&nbsp;&nbsp;Bonus if this can generate artifacts
**This can have 1 to 5 spreadsheets, depending on your needs. Note: 900 controls is heavy.

Asset Dashboard - Categories, Trends month over month for Asset tracking
	&nbsp;Server Count (Windows and Linux)
	&nbsp;Workstations
	&nbsp;Switches
	&nbsp;Firewalls
	&nbsp;End of Support
	&nbsp;Unsupported
	&nbsp;Missing Patches
	&nbsp;Offline
	&nbsp;Retired
	&nbsp;Server Backup Status: Full, Differential, Incremental (Monthly, Weekly, Daily)
	&nbsp;Log Collection: Size per asset, Rsyslog drive status, forwarding to SOC
**This is one spreadsheet, this should be the simplest one

Risk Dashboard - Heat Map for visual aid
Used for tracking remediation and potential risk factors associated with high risk/high impact findings
Pull from the cross referenced and distilled findings. These vulnerabilities will be sorted based on the scoring of likelihood and probability of exploitation.
	&nbsp;Run formula on this to create scores
	&nbsp;Risk Calculus formula based on findings, huge bonus to have.

POAM Dashboard - Manual Feed 
	&nbsp;Used to track, update and communicate status to Executive Dashboard
	&nbsp;Tracks points of authority, points of responsibility and current status - Biweekly meeting
	&nbsp;Open, Completed, Overdue, within SLA %
**This will likely be it's own quarterly/annual spreadsheet


Automation Requirements:

Raw Data (4 Scripts)
	&nbsp;Check for tool definition updates and patches then install them at set times
	&nbsp;Tools ran by scheduled task with preset conditions (Including file name format)
	&nbsp;Run server hosted Powershell to collect endpoint data
	&nbsp;&nbsp;	Shared drive is stored on server for backups, and copied to a network drive & Sharepoint
	&nbsp;Run formatting Powershell to consolidate raw files into Spreadsheet (Formatting is key)
	
Compliance Automation (4-5 Possible)
	&nbsp;Create Control family checkers, different families should yield different scores
		&nbsp;&nbsp;This will be fed by multiple books if you have multiple compliance standards to meet
	&nbsp;&nbsp;If possible, link to remediation library (Possibly through CVE/CVSS)

Asset Automation (3 Scripts)
	&nbsp;Backup Creation and a query formula to check for incoming files.
	&nbsp;&nbsp;	I.E. March's sheet will query for March Week 1, 2, 3 and 4. The document is living.
	&nbsp;&nbsp;	Status: Full, Differential, Incremental (Monthly, Weekly, Daily)
	&nbsp;Log generation, collection, and forwarding. This is for SOC digestion.
	&nbsp;Patch retrieval, installation and verification
		This would be done on week 1 for the VM/Workstation, and week 2 for all endpoints

Risk Automation (1 Script)
	&nbsp;Create a presentable heat map based on findings, goal of finding lateral attack surface.
	&nbsp;	Findings cross referenced from page 2 of the master spreadsheet of distilled findings. 
	&nbsp;	Scored and sorted based on the scoring of likelihood and probability of exploitation.


Overview
All labs are all automated for security patching, vulnerability assessments and data collection.
Complete with action items and visibility on remediation.
	&nbsp;Tools and patches run with a scheduled task for each
	&nbsp;Vulnerability scanning - outcome of files ready for integration
	&nbsp;Log Collection either run from server or locally via Event viewer for Continuous monitoring
	&nbsp;Powershell run to collect all properly formatted data for consolidation with redundancy

Compliance and Control Integration
	&nbsp;Able to have live knowledge on current state of affairs for priority with evidence
	&nbsp;Able to check and track multiple compliance standards over time
	&nbsp;Action items for specific audits, establishing priority 

Asset Management made simple
	&nbsp;An updated asset list, their status, and action items
	&nbsp;Trends over time
	&nbsp;Endpoint security streamlined

Vulnerability and Risk
	&nbsp;Heat maps for visual aid and trends on company security posture
	&nbsp;CVE/ CVSS action items to address it via security policy, automation or manual fix


Engine that makes this work:
&nbsp;8-12 scripts to automate the information flow infrastructure
&nbsp;1 Source of truth from 8-10 Spreadsheets, generated and referenced 
&nbsp;6 Dashboards for specific inquiries across different teams
&nbsp;Transparency to upper management
&nbsp;Action items for the team
&nbsp;Streamlined deliverables for audits/POAMs
&nbsp;Emphasis cyber maturity and streamlined GRC
