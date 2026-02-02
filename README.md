# Snort-IDS-Mitigation-Project

## 🛡️ Project Overview
This project demonstrates the deployment of a Snort Intrusion Detection System (IDS) in a Linux environment. It covers the full lifecycle of a security event: **Configuration -> Detection -> Debugging -> Mitigation.**



## 🔍 The Snort Analysis Process
In this project, I followed the industry-standard IDS analysis workflow:

1.  **Packet Acquisition:** Snort listens to the network interface in promiscuous mode to capture all passing traffic.
2.  **Preprocessing:** Snort normalizes the traffic to detect fragmented packets or "hidden" threats.
3.  **Detection Engine:** The captured traffic is compared against the `local.rules` file. (I successfully debugged rule syntax errors here!).
4.  **Logging/Alerting:** Matches are logged to `/var/log/snort` and signaled via syslog.
5.  **Active Mitigation (IPS):** Using `iptables`, I manually blocked a source IP once it was flagged as suspicious.

## 📸 Key Implementation Screenshots
- **Traffic Validation:** Monitoring live ICMP pings.
- **Rule Debugging:** Fixing parentheses errors in Snort logic.
- **IPS Enforcement:** Dropping traffic from hostile IPs via the firewall.

## 🚀 Skills Demonstrated
- Linux CLI (Ubuntu)
- Network Protocol Analysis (ICMP/IP)
- IDS/IPS Configuration
- Firewall Management (iptables)
