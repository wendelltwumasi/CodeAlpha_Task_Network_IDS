# ==========================================
# CUSTOM SNORT RULES
# ==========================================

# 1. ICMP Detection
# Detects standard ping requests targeting the HOME_NET.
alert icmp any any -> $HOME_NET any (msg:"ICMP Packet Detected"; sid:1000001; rev:1;)

# 2. Potential SSH Brute Force (Recommended addition based on your setup)
# alert tcp $EXTERNAL_NET any -> $HOME_NET 22 (msg:"SSH Authentication Attempt"; flags:S; sid:1000002; rev:1;)