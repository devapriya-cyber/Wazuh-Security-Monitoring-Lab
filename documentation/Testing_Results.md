\# Wazuh Security Monitoring Lab – Testing Results



\## 1. Overview



This document records the monitoring and testing activities performed in the Wazuh Security Monitoring Lab.



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

\- Detection mode: Realtime.



\*\*Result:\*\* Successful.



\## 3. Security Configuration Assessment (SCA)



\*\*Objective:\*\* Review endpoint security configuration against the selected security policy.



\*\*Test procedure:\*\*

1\. Opened Configuration Assessment in the Wazuh Dashboard.

2\. Selected the Windows endpoint.

3\. Reviewed the assessment results.



\*\*Observed result:\*\*



The dashboard displayed passed and failed security checks.



The detailed assessment evidence is available in `screenshots/Wazuh\_SCA\_Assessment.png`.



\## 4. Vulnerability Detection



\*\*Objective:\*\* Review vulnerabilities identified on the monitored Windows endpoint.



\*\*Test procedure:\*\*

1\. Opened Vulnerability Detection.

2\. Accessed the Inventory section.

3\. Reviewed the detected CVE records.

4\. Inspected individual vulnerability details.



\*\*Observed result:\*\*

\- Vulnerability inventory records were visible.

\- CVE identifiers and vulnerability details were reviewed.



\*\*Result:\*\* Vulnerability records successfully reviewed.



\## 5. Security Event Monitoring



\*\*Objective:\*\* Examine security events collected by Wazuh.



\*\*Test procedure:\*\*

1\. Opened Threat Hunting → Events.

2\. Cleared restrictive search filters.

3\. Selected a broader time range.

4\. Reviewed the available security events.



\*\*Observed result:\*\* Security event records were visible in the dashboard.



\## 6. Endpoint Connectivity



\*\*Objective:\*\* Verify communication between the Windows endpoint and Wazuh Manager.



\*\*Observed result:\*\* The Windows agent appeared with Active status in the Wazuh Dashboard during testing.



\## 7. Docker Deployment Verification



\*\*Objective:\*\* Verify that the Wazuh server components were running.



\*\*Observed result:\*\* The Wazuh Manager, Indexer, and Dashboard containers were running when checked using `docker ps`.



\## 8. Evidence



Screenshots for the above tests are stored in the `screenshots/` directory.



\## 9. Conclusion



The lab demonstrated basic Wazuh deployment and practical testing of endpoint monitoring, file integrity monitoring, security configuration assessment, vulnerability detection, and security event analysis.



These results represent observations from the lab environment and should not be interpreted as a production security assessment.

