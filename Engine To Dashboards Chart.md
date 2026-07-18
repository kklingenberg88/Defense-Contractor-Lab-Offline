Visual Aid for the information flow for Engines that forward information to Dashboards
                    ┌─────────────────────────────┐
                    │     Data Collection Engine  │
                    └──────────────┬──────────────┘
                                   │
        SCAP  STIG  Nessus  Assets  Patch Status  PowerShell
                                   │
                                   ▼
                    ┌─────────────────────────────┐
                    │   Data Processing Engine    │
                    │ Normalize / Clean / Merge   │
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                    Master Evidence Repository
                    (Single Source of Truth)
                                   │
          ┌──────────────┬──────────────┬──────────────┐
          ▼              ▼              ▼              ▼
  Compliance      Vulnerability     Asset         Risk Assessment
     Engine      Correlation Engine Management       Engine
          │              │              │              ▲
          │              └──────────────┴──────────────┘
          │                     (Shared Data)
          ▼
                 POA&M Management Engine
                          │
                          ▼
               Executive Reporting Layer
                          │
      ┌───────────┬───────────┬───────────┬───────────┐
      ▼           ▼           ▼           ▼           ▼
 Executive   Compliance  Vulnerability   Asset      Risk
 Dashboard    Dashboard    Dashboard   Dashboard Dashboard
                          │
                          ▼
                    POA&M Dashboard
