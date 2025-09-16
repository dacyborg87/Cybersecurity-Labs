🛡️ Lab 1 – Wazuh SIEM Setup and Filebeat Integration

📌 Objective

The goal of this lab was to set up and validate the integration of Wazuh SIEM, OpenSearch, and Filebeat in a homelab environment. This ensures that logs from endpoints are collected, processed, and visualized in the Wazuh dashboard for threat detection and monitoring.

⸻

⚙️ Steps Completed

1. Wazuh Manager & Dashboard Setup
	•	Verified that Wazuh services were running correctly.
	•	Accessed the dashboard at https://192.168.1.93:5601.
	•	Confirmed agent activity (active vs. disconnected).

2. Filebeat Integration with OpenSearch
	•	Pulled and configured the Filebeat image.
	•	Fixed platform mismatch errors (amd64 vs arm64).
	•	Adjusted permissions so Filebeat could read alerts.json.
	•	Mounted configuration file filebeat-docker.yml.

3. Index Verification
	•	Confirmed indices in OpenSearch:
	•	wazuh-alerts-* → security alerts.
	•	wazuh-monitoring-* → agent heartbeat and status.
	•	wazuh-statistics-* → performance and health metrics.
	•	Used curl to verify index status and log counts.

4. Dashboard Exploration
	•	Discover (wazuh-alerts-*) → reviewed security alerts.
	•	Discover (wazuh-monitoring-*) → confirmed agent connectivity.
	•	Discover (wazuh-statistics-*) → validated Wazuh performance (events decoded, alerts written, queue size).

⸻

🔍 Key Findings
	•	Wazuh successfully processed and indexed alerts (200+ in 30 days).
	•	Monitoring confirmed agent heartbeat for endpoints (MacBook, Windows VM).
	•	Statistics showed healthy engine performance (no dropped events).
	•	Main challenges: Docker platform mismatch + permission errors, resolved by:
	•	Running with correct --platform.
	•	Using chmod on alerts.json.

⸻

📸 Recommended Screenshots

To tell the full story on GitHub, include these screenshots:
	1.	Wazuh Overview Dashboard (agent summary).
	2.	Discover → wazuh-alerts-* (alerts timeline + log details).
	3.	Discover → wazuh-monitoring-* (agent heartbeat and status).
	4.	Discover → wazuh-statistics-* (performance metrics).
	5.	Example troubleshooting screenshot (e.g., Filebeat permission denied).

⸻

📚 Lessons Learned
	•	Verify agent connectivity and file permissions first when integrating Filebeat.
	•	Understand the purpose of indices:
	•	Alerts = detections.
	•	Monitoring = heartbeat.
	•	Statistics = system health.
	•	Docker troubleshooting often requires fixing platform mismatches and mount permissions.

⸻

🚀 Next Steps
	•	Expand lab by adding more endpoints.
	•	Write and test custom detection rules.
	•	Generate test alerts (simulated brute force, privilege escalation, etc).
	•	Build custom dashboards for monitoring activity.

⸻

✅ End of Lab 1 – Wazuh SIEM Setup and Filebeat Integration

⸻
