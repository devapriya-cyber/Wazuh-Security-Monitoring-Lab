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



\*\*Investigation

