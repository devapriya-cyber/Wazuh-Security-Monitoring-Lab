\# Wazuh Lab Configuration Reference



\## 1. Deployment Information



\- Deployment method: Docker Compose

\- Compose project: `single-node`

\- Wazuh version: 4.14.0

\- Environment: Docker Desktop with WSL 2



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



These are the configured service ports in the lab deployment. Actual accessibility depends on Docker

