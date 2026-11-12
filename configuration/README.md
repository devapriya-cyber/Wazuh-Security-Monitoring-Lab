\# Wazuh Lab Configuration Reference



\## 1. Deployment Information



\- Deployment method: Docker Compose

\- Compose project: single-node

\- Wazuh version: 4.14.0

\- Environment: Docker Desktop with WSL 2



\## 2. Server Components



| Component | Docker Service |

|---|---|

| Wazuh Manager | wazuh.manager |

| Wazuh Indexer | wazuh.indexer |

| Wazuh Dashboard | wazuh.dashboard |



\## 3. Network Ports



| Port | Purpose |

|---|---|

| 443 | Dashboard HTTPS access |

| 1514 | Wazuh agent communication |

| 1515 | Agent enrollment |

| 55000 | Wazuh API |

| 9200 | Indexer API |



\## 4. Original Configuration



The original Docker Compose configuration is maintained locally at:



`C:\\Users\\DEVAPRIYA\\wazuh-docker\\single-node\\docker-compose.yml`



\## 5. Security Considerations



The original configuration is not included in this public repository because it may contain passwords or other sensitive values.



Credentials, API keys, private certificates, and other secrets must never be committed to a public repository.

