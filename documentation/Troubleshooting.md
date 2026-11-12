\# Wazuh Security Monitoring Lab – Troubleshooting



\## 1. Dashboard Not Ready



\*\*Problem:\*\* The Wazuh Dashboard displayed the message "Wazuh dashboard server is not ready yet."



\*\*Investigation:\*\*

\- Checked the status of Docker containers using `docker ps -a`.

\- Reviewed Dashboard logs using `docker logs`.

\- Reviewed Indexer logs to investigate connectivity and cluster status.



\*\*Resolution:\*\*

\- Allowed the Wazuh services time to initialize.

\- Confirmed that the Indexer cluster health changed to GREEN.

\- Refreshed the Dashboard after the services became ready.



\*\*Outcome:\*\* Dashboard became accessible.



\## 2. Initial Indexer Connection Errors



\*\*Problem:\*\* Dashboard logs showed connection errors when attempting to communicate with the Indexer.



\*\*Investigation:\*\*

\- Observed connection refused errors for port 9200.

\- Checked Indexer startup logs.

\- Reviewed cluster health messages.



\*\*Resolution:\*\* Waited for the Indexer to complete initialization and verified its cluster status.



\*\*Outcome:\*\* Indexer reported GREEN cluster health.



\## 3. No Results in Threat Hunting



\*\*Problem:\*\* Threat Hunting displayed "No results match your search criteria."



\*\*Investigation:\*\*

\- Reviewed the selected time range.

\- Checked the active search query and filters.



\*\*Resolution:\*\*

\- Cleared restrictive filters.

\- Expanded the time range to the last 30 days.

\- Refreshed the event view.



\*\*Outcome:\*\* Security event records became visible.



\## 4. Troubleshooting Approach



The following commands were useful for checking the Docker deployment:



\### Check running containers



```powershell

docker ps

```



\### Check all containers



```powershell

docker ps -a

```



\### Review Dashboard logs



```powershell

docker logs --tail 60 single-node-wazuh.dashboard-1

```



\### Review Indexer logs



```powershell

docker logs --tail 60 single-node-wazuh.indexer-1

```



\### Review Manager logs



```powershell

docker logs --tail 60 single-node-wazuh.manager-1

```



\## 5. Lessons Learned



\- Check service and container status before restarting components.

\- Review logs to identify startup and connectivity problems.

\- Allow sufficient time for services to initialize.

\- Check dashboard time ranges and filters before concluding that no events exist.

\- Avoid deleting Docker volumes when troubleshooting because they may contain important lab data.

