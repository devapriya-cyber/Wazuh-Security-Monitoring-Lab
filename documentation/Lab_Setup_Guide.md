\# Wazuh Security Monitoring Lab – Setup Guide



\## 1. Project Overview



This project demonstrates a hands-on security monitoring lab using Wazuh. It was built to explore endpoint monitoring, security configuration assessment, file integrity monitoring, vulnerability detection, and security event analysis.



\## 2. Lab Environment



| Component | Details |

|---|---|

| SIEM Platform | Wazuh |

| Wazuh Manager, Indexer and Dashboard | 4.14.0 |

| Deployment Method | Docker Compose |

| Container Environment | Docker Desktop with WSL 2 |

| Server Operating System | Windows 11 |

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



A Windows 11 endpoint was connected to the Wazuh Manager using the Wazuh Agent.



The agent communicates with the manager to send endpoint monitoring data for centralized security analysis.



\## 4. Deployment Overview



1\. Installed Docker Desktop and configured the WSL 2 environment.

2\. Deployed the Wazuh single-node Docker environment.

3\. Started the Wazuh Manager, Indexer, and Dashboard containers.

4\. Accessed the Wazuh Dashboard through HTTPS.

5\. Installed the Wazuh Agent on a separate Windows endpoint.

6\. Configured the agent to communicate with the Wazuh Manager.

7\. Verified agent connectivity and monitoring functionality in the dashboard.



\## 5. Monitoring and Testing



The following capabilities were explored and tested:



\- \*\*File Integrity Monitoring (

