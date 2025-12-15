# Windows Event Log Brute Force Analysis (Lab Project)

A hands-on lab project simulating a brute-force login attempt and analyzing Windows Security Event Logs to identify failed and successful logon patterns
(similar to SOC workflows).

## Overview
This project focuses on:
- Understanding how Windows records authentication activity in Security logs
- Identifying brute-force patterns using Event Viewer
- Documenting findings in a structured security report

## Target Environment
- Platform: Windows (Virtual Lab)
- Log Source: Windows Security Event Log
- Tools: Event Viewer (Windows), Documentation/Reporting

## Methodology
1. Generate multiple failed login attempts against a local user account (lab-only simulation)
2. Open **Event Viewer** → Windows Logs → **Security**
3. Filter and analyze key Event IDs:
   - **4625**: Failed logon attempts
   - **4624**: Successful logon
4. Correlate attempts by:
   - Username
   - Time window
   - Logon type (e.g., Interactive)
5. Summarize findings and recommendations

## Key Findings (Example)
- Multiple consecutive **4625** events within a short time window indicate a brute-force pattern
- A subsequent **4624** event may indicate successful credential guessing
- Logon Type and Failure Reason provide useful investigation context

## Screenshots
See the `Screenshots/` folder for annotated evidence (filters, Event IDs, and highlights).

## Report
The full write-up is available in:
- `Report/Windows_Event_Log_Brute_Force_Report.pdf`

## Disclaimer
This project was performed in a controlled lab environment for educational purposes only.
No real systems or unauthorized targets were involved.
