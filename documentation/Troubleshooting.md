

\# Wazuh Security Monitoring Lab – Troubleshooting



\## 1. Dashboard Not Ready



\*\*Problem:\*\* The Wazuh Dashboard displayed the message "Wazuh dashboard server is not ready yet."



\*\*Investigation:\*\*

\- Checked Docker container status using `docker ps -a`.

\- Reviewed Dashboard logs.

\- Reviewed Indexer logs to investigate connectivity and cluster status.



\*\*Resolution:\*\*

\- Allowed the Wazuh services time to initialize.

\- Confirmed that the Indexer cluster health changed to GREEN.

\- Refreshed the Dashboard after the services became ready.



\*\*Outcome:\*\* The Dashboard became accessible after the Indexer completed initialization.



\## 2. Initial Indexer Connection Errors



\*\*Problem:\*\* Dashboard logs showed connection errors when attempting to communicate with the Indexer.



\*\*Investigation:\*\*

\- Observed connection refused errors for port 9200.

\- Checked Indexer startup logs.

\- Reviewed cluster health messages.



\*\*Resolution:\*\*

\- Allowed the Indexer to complete its initialization.

\- Verified that the Indexer cluster reported GREEN health.



\*\*Outcome:\*\* The Indexer became available and the Dashboard was accessible.



\*\*Note:\*\* GREEN indicates that the Indexer cluster was healthy at the time of verification. It does not represent an overall security assessment of the endpoint.



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



\## 4. Useful Troubleshooting Commands



The following PowerShell commands were used to inspect the Docker deployment.



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

\- Review container configuration and logs before making changes to the deployment.



\*\*Important:\*\* Avoid running commands that remove containers, images, or Docker volumes unless you understand their impact and have backed up important lab data.
