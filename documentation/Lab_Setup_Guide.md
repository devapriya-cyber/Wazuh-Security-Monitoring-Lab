\# Wazuh Security Monitoring Lab – Setup Guide



\## 1. Project Overview



This project demonstrates a hands-on security monitoring lab using Wazuh. It was built to explore endpoint monitoring, security configuration assessment, file integrity monitoring, vulnerability detection, and security event analysis.



\## 2. Lab Environment



| Component | Details |

|---|---|

| SIEM Platform | Wazuh |

| Wazuh Version | 4.14.0 |

| Deployment Method | Docker |

| Container Environment | Docker Desktop with WSL 2 |

| Operating System | Windows 11 |

| Endpoint Agent | Wazuh Agent 4.14.6 |

| Dashboard Access | HTTPS |



\## 3. Lab Architecture



The lab consists of a Wazuh server stack and a monitored Windows endpoint.



\### Wazuh Server Components



\- \*\*Wazuh Manager:\*\* Receives and analyses endpoint security data.

\- \*\*Wazuh Indexer:\*\* Stores and indexes security events and monitoring data.

\- \*\*Wazuh Dashboard:\*\* Provides a graphical interface for monitoring and investigation.



\### Monitored Endpoint



A Windows 11 endpoint was connected to the Wazuh Manager using the Wazuh Agent.



\## 4. Deployment Overview



1\. Installed Docker Desktop and configured the WSL 2 environment.

2\. Deployed the Wazuh single-node Docker environment.

3\. Started the Wazuh Manager, Indexer, and Dashboard containers.

4\. Accessed the Wazuh Dashboard through HTTPS.

5\. Installed and configured the Wazuh Agent on a Windows endpoint.

6\. Connected the endpoint to the Wazuh Manager.

7\. Verified agent connectivity and monitoring functionality.



\## 5. Monitoring and Testing



The following capabilities were explored and tested:



\- \*\*File Integrity Monitoring (FIM):\*\* Monitored file changes and verified modification alerts.

\- \*\*Security Configuration Assessment (SCA):\*\* Reviewed security configuration checks and compliance results.

\- \*\*Vulnerability Detection:\*\* Examined detected vulnerabilities and associated CVE information.

\- \*\*Security Event Monitoring:\*\* Reviewed security events through the Wazuh Dashboard.



\## 6. Verification



The following checks were used during lab validation:



\- Verified that the Wazuh Docker containers were running.

\- Checked the Windows endpoint agent connection status.

\- Modified a monitored test file to generate a FIM alert.

\- Reviewed SCA assessment results.

\- Examined vulnerability inventory records.

\- Reviewed security events in the dashboard.



\## 7. Evidence



Screenshots demonstrating the lab implementation and testing are available in the `screenshots/` directory.



\## 8. Security Note



Credentials, API keys, private certificates, and other sensitive information should not be committed to the public repository.



\## 9. Project Status



This is a hands-on learning project focused on understanding Wazuh deployment, endpoint monitoring, and basic security operations workflows.

