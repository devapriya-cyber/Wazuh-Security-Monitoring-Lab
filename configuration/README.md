

\# Wazuh Lab Configuration Reference



\## 1. Deployment Information



\- Deployment method: Docker Compose

\- Compose project: `single-node`

\- Wazuh Manager, Indexer and Dashboard version: 4.14.0

\- Environment: Docker Desktop with WSL 2

\- Host operating system: Windows 11



\## 2. Server Components



| Component | Docker Service |

|---|---|

| Wazuh Manager | `wazuh.manager` |

| Wazuh Indexer | `wazuh.indexer` |

| Wazuh Dashboard | `wazuh.dashboard` |



\## 3. Network Ports



| Port | Purpose |

|---|---|

| 443 | Wazuh Dashboard HTTPS access |

| 1514 | Wazuh agent communication |

| 1515 | Wazuh agent enrollment |

| 55000 | Wazuh API |

| 9200 | Wazuh Indexer API |



These are the service ports used in the lab deployment. Actual accessibility depends on Docker port mappings and network configuration.



\## 4. Original Configuration



The original Docker Compose configuration is maintained locally in the Wazuh Docker deployment directory:



`wazuh-docker/single-node/docker-compose.yml`



The original configuration file is not included in this public repository because it contains sensitive configuration values.



\## 5. Security Considerations



\- Never commit passwords, API keys, private certificates, or other sensitive configuration values to a public repository.

\- Review configuration files for sensitive information before uploading them.

\- Use environment variables or secure secret-management methods for credentials.

\- Keep private keys and certificates outside public repositories.

\- Avoid publishing internal network details unless they are necessary for documenting the lab.



\## 6. Configuration Disclaimer



This document provides a reference to the lab environment and its configuration. It is not a complete, standalone Docker Compose deployment file.
