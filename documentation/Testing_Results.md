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



\*\*Test procedure

