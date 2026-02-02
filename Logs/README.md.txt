# Snort Log Management & Analysis
During this project, I used the following commands to monitor and analyze IDS alerts in real-time.

### 1. Monitoring Alerts in Real-Time
To watch the alerts as they were triggered (e.g., during the ICMP ping tests), I used the `tail` command:
```bash
sudo tail -f /var/log/snort/alert