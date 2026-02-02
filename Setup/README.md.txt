# Snort Setup & Configuration
The system was deployed on **Ubuntu 22.04.5 LTS** via Oracle VirtualBox.

### Network Variables (from snort.conf)
As seen in the configuration (Screenshot: Choose3.png), the following variables were set:
- `ipvar HOME_NET any`: Defined the protected network.
- `ipvar EXTERNAL_NET any`: Defined the source of potential threats.

### Initialization & Debugging
- Tested configuration using: `sudo snort -T -c /etc/snort/snort.conf`.
- **Debugging Fix:** Resolved a critical error where rule options were not properly enclosed in parentheses `( )` (Screenshot: Choose2.png).
- **Output Logging:** Enabled syslog alerting for integration with system monitoring (Screenshot: choose4.png).