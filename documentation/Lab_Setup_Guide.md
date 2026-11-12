

\# Wazuh Security Monitoring Lab – Setup Guide



\## 1. Project Overview



This project demonstrates a hands-on security monitoring lab using Wazuh. It explores endpoint monitoring, Security Configuration Assessment, File Integrity Monitoring, vulnerability detection, and security event analysis.



\## 2. Lab Environment



| Component | Details |

|---|---|

| SIEM Platform | Wazuh |

| Wazuh Manager, Indexer and Dashboard | 4.14.0 |

| Deployment Method | Docker Compose |

| Container Environment | Docker Desktop with WSL 2 |

| Host Operating System | Windows 11 |

| Monitored Endpoint Operating System | Windows 11 |

| Endpoint Agent | Wazuh Agent 4.14.6 |

| Dashboard Access | HTTPS |



\## 3. Lab Architecture



The lab was configured using two laptops: one hosting the Wazuh server stack and another serving as the monitored Windows endpoint.



\### Wazuh Server Components



\- \*\*Wazuh Manager:\*\* Receives and analyses endpoint security data.

\- \*\*Wazuh Indexer:\*\* Stores and indexes security events and monitoring data.

\- \*\*Wazuh Dashboard:\*\* Provides a graphical interface for monitoring and investigation.



\### Monitored Endpoint



A Windows 11 endpoint was connected to the Wazuh Manager using the Wazuh Agent. The agent sends endpoint monitoring data to the manager for centralized security analysis.



\## 4. Deployment Overview



1\. Installed Docker Desktop and configured the WSL 2 environment.

2\. Deployed the Wazuh single-node Docker environment using Docker Compose.

3\. Started the Wazuh Manager, Indexer, and Dashboard containers.

4\. Accessed the Wazuh Dashboard through HTTPS.

5\. Installed Wazuh Agent 4.14.6 on a separate Windows endpoint.

6\. Configured the agent to communicate with the Wazuh Manager.

7\. Verified agent connectivity and monitoring functionality in the dashboard.



\## 5. Monitoring and Testing



The following capabilities were explored and tested:



\- \*\*File Integrity Monitoring (FIM):\*\* Tested file modification detection and verified the resulting alert.

\- \*\*Security Configuration Assessment (SCA):\*\* Reviewed Windows security configuration checks and assessment results.

\- \*\*Vulnerability Detection:\*\* Examined vulnerability inventory records and associated CVE information.

\- \*\*Security Event Monitoring:\*\* Reviewed security events through the Wazuh Dashboard.



\## 6. Verification



The following checks were performed during lab validation:



\- Verified that the Wazuh Docker containers were running.

\- Checked the Windows endpoint agent connection status.

\- Created and modified a test file in `C:\\Users\\Public` to generate a FIM alert.

\- Reviewed SCA assessment results.

\- Examined vulnerability inventory records and CVE details.

\- Reviewed security events in the dashboard.



The endpoint connectivity and container status were verified at the time of testing.



\## 7. Evidence



Screenshots demonstrating the lab implementation and testing are available in the `screenshots/` directory.



\## 8. Security Note



\- Credentials, API keys, private certificates, and other sensitive information should not be committed to the public repository.

\- Configuration files should be reviewed for sensitive information before uploading.

\- Private credentials and certificates should be stored securely.



\## 9. Project Status



This is a hands-on learning project focused on understanding Wazuh deployment, endpoint monitoring, and basic security operations workflows.
