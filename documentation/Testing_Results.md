

\# Wazuh Security Monitoring Lab – Testing Results



\## 1. Overview



This document records the monitoring and testing activities performed in the Wazuh Security Monitoring Lab.



The tests were conducted to verify endpoint connectivity, file integrity monitoring, security configuration assessment, vulnerability detection, and security event monitoring.



\## 2. File Integrity Monitoring (FIM)



\*\*Objective:\*\* Verify whether Wazuh detects changes to monitored files.



\*\*Test procedure:\*\*



1\. Created a test file named `fim\_test.txt` in `C:\\Users\\Public`.

2\. Modified the file.

3\. Reviewed the resulting security event in the Wazuh Dashboard.



\*\*Observed result:\*\*



\- Wazuh generated a file integrity modification alert.

\- Event description: Integrity checksum changed.

\- Rule ID: 550

\- Severity level: 7

\- Detection mode: Real-time.

\- File: `C:\\Users\\Public\\fim\_test.txt`



Wazuh recorded changes to file attributes, including MD5, SHA-1, and SHA-256 checksums.



\*\*Result:\*\* Successful. The file modification was detected and an alert was generated.



\## 3. Security Configuration Assessment (SCA)



\*\*Objective:\*\* Review endpoint security configuration against the selected security policy.



\*\*Test procedure:\*\*



1\. Opened Configuration Assessment in the Wazuh Dashboard.

2\. Selected the Windows endpoint.

3\. Reviewed the assessment results.



\*\*Observed result:\*\*



The dashboard displayed the following assessment results:



\- Passed checks: 123

\- Failed checks: 350

\- Total checks: 473



Failed checks indicate security policy checks that did not pass at the time of assessment. They do not automatically represent confirmed vulnerabilities. Each failed check requires individual review.



\*\*Result:\*\* Successfully reviewed the SCA assessment results.



\## 4. Vulnerability Detection



\*\*Objective:\*\* Review vulnerabilities identified on the monitored Windows endpoint.



\*\*Test procedure:\*\*



1\. Opened Vulnerability Detection.

2\. Accessed the Inventory section.

3\. Reviewed the detected CVE records.

4\. Inspected individual vulnerability details.



\*\*Observed result:\*\*



\- Vulnerability inventory records were visible.

\- CVE identifiers and associated vulnerability details were reviewed.

\- Individual CVE information was inspected in the dashboard.



\*\*Result:\*\* Successfully reviewed vulnerability records and CVE details. No vulnerability remediation was performed as part of this test.



\## 5. Security Event Monitoring



\*\*Objective:\*\* Examine security events collected by Wazuh.



\*\*Test procedure:\*\*



1\. Opened Threat Hunting → Events.

2\. Cleared restrictive search filters.

3\. Selected a broader time range.

4\. Reviewed the available security events.



\*\*Observed result:\*\*



Security event records became visible after clearing restrictive filters and expanding the time range.



\*\*Result:\*\* Successfully accessed and reviewed security events in the Wazuh Dashboard.



\## 6. Endpoint Connectivity



\*\*Objective:\*\* Verify communication between the Windows endpoint and Wazuh Manager.



\*\*Observed result:\*\*



The Windows agent appeared with Active status in the Wazuh Dashboard during testing.



\*\*Result:\*\* Endpoint connectivity was successfully verified at the time of testing.



\## 7. Docker Deployment Verification



\*\*Objective:\*\* Verify that the Wazuh server components were running.



\*\*Test procedure:\*\*



1\. Executed the `docker ps` command.

2\. Reviewed the running Wazuh containers.



\*\*Observed result:\*\*



The Wazuh Manager, Indexer, and Dashboard containers were running when checked.



\*\*Result:\*\* Docker deployment was successfully verified at the time of testing.



\## 8. Evidence



Screenshots supporting the above tests are stored in the `screenshots/` directory.



The evidence includes:



\- Wazuh Dashboard overview

\- Agent active status

\- Running Docker containers

\- File Integrity Monitoring alert

\- Security Configuration Assessment results

\- Security events

\- Vulnerability inventory

\- CVE details



\## 9. Conclusion



The lab demonstrated practical use of Wazuh for endpoint monitoring, File Integrity Monitoring, Security Configuration Assessment, vulnerability detection, and security event analysis.



The tests confirmed that the lab could generate file integrity alerts, display endpoint security assessment results, and provide visibility into vulnerability records and security events.



These results represent observations from a personal lab environment and should not be interpreted as a production security assessment.
