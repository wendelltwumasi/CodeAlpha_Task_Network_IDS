# Threat Mitigation & Visualization

### Active Response (IPS)
When a malicious source (e.g., `192.168.1.10`) was identified via Snort logs, an active response was implemented using `iptables` to DROP all further traffic from that source.

**Command Executed:**
`sudo iptables -A INPUT -s 192.168.1.10 -j DROP`

### Visualization metrics
If this data were exported to a dashboard (like Snorby or ELK), it would track:
1. **Top Attack Sources:** Showing `192.168.1.10` as the primary threat.
2. **Protocol Distribution:** High volume of ICMP traffic vs. TCP/UDP.
3. **Firewall Actions:** Visualization of "Dropped Packets" vs. "Allowed Packets."