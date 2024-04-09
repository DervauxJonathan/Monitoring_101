# Monitoring_101

## Part 1: Research Findings

### Context
In system administration, monitoring a Linux system is crucial for ensuring optimal performance, stability, and security. This document outlines various aspects of monitoring a Linux system comprehensively.

### Main Areas of Concern When Monitoring a System
1. **CPU Usage:** Monitoring CPU usage is essential to ensure efficient workload handling without overburdening the system.
   - Commands: `top`, `mpstat`, `sar`

2. **Memory Usage:** Preventing excessive memory consumption helps avoid system slowdowns or crashes.
   - Commands: `free -h`, `top`, `htop`, `vmstat`, `pmap`, `ps aux --sort=-%mem`

3. **Disk Usage:** Monitoring disk space prevents system instability or failure due to insufficient space.
   - Commands: `df -h`, `du -sh`, `iostat -x`, `iotop`

4. **Network Usage:** Ensuring sufficient bandwidth and managing network traffic prevent overwhelming the system.
   - Commands: `iftop`, `nload`, `vnstat`, `iptraf-ng`, `tcpdump`

5. **Application Performance:** Monitoring critical application performance ensures smooth operation.
   - Commands: `top`, `htop`, `vmstat`, `sar`, `strace`, `perf stat`, `netstat`, `tcpdump`

6. **Security Events:** Monitoring for security events helps ensure system security.
   - Commands: `cat /var/log/syslog`, `tail -f /var/log/syslog`, `grep`, `journalctl`, `auditctl`, `fail2ban`, `tripwire`

7. **System Logs:** Monitoring system logs aids in identifying and troubleshooting issues effectively.
   - Commands: `tail -f /var/log/syslog`, `grep`, `less`, `journalctl`, `dmesg`, `systemctl`, `logwatch`, `logrotate`

8. **Hardware Health:** Monitoring hardware health indicators ensures proper functioning of physical components.
   - Commands: `sensors`, `smartctl`, `hddtemp`, `ipmitool`, `lshw`, `dmidecode`, `nvidia-smi`

9. **Service Availability:** Monitoring essential services ensures uninterrupted service for users.
   - Commands: `systemctl`, `ssh`, `is-active`

10. **Backup Status:** Monitoring backup status reduces the risk of data loss.
    - Approaches: Backup log analysis, automated notifications, backup reporting, custom monitoring scripts

### Memory Intensive Processes
- **Using `top` command:** Sort processes by memory usage with `Shift + M`.
- **Using `htop` command:** Provides an interactive interface for monitoring and sorting processes.
- **Using `ps` command:** List processes sorted by memory usage.

### Log Files
Log files are records of system events stored in `/var/log`. Common types include:
- `syslog` or `messages`
- Kernel logs
- Application logs
- Package manager logs
- Cron logs
- Boot logs
- Security logs

### Last Connected Users
- **Using `last` command:** Displays last logged-in users.
- **Examining auth logs:** Check `session opened` and `session closed` entries.
- **Using `who` and `w` commands:** Show currently logged-in users and their activities.
- **Examining User History Files:** Check user command history in `.bash_history`.

### Metrics of System Health and Performance
- **Resource Utilization:** CPU, memory, disk I/O, network I/O
- **System Performance:** Response time, latency, throughput
- **System Stability:** Uptime, availability, reliability
- **Capacity Planning:** Scalability, resource forecasting
- **Security and Compliance:** Security events, compliance metrics
- **Application Performance:** Transaction rate, error rates, resource consumption
- **User Experience:** Load time, responsiveness, error handling

### Checking Uptime
- **Using `uptime` command:** Displays system uptime and load averages.

### Assessing Network Traffic
- **Packet Sniffing:** Wireshark, Tcpdump
- **NetFlow and IPFIX:** NfSen, nProbe
- **Network Monitoring Tools:** Nagios, Zabbix
- **Bandwidth Monitoring:** Iftop, nload
- **Flow-Based Analysis:** ntopng, Argus
- **Firewall and Router Logs:** Analyzing logs from network devices
- **Deep Packet Inspection:** Suricata

### Active vs. Reactive Monitoring
- **Active Monitoring:** Proactive checks to ensure safety and compliance.
- **Reactive Monitoring:** Responding to incidents and accidents after they occur.

### Backup Status Monitoring
- Approaches include backup log analysis, automated notifications, backup reporting, and custom monitoring scripts.

## Command Explanations
For detailed explanations of commands mentioned, refer to the following:
- `auditctl`, `df`, `dmesg`, `dmidecode`, `du`, `fail2ban`, `free`, `grep`, `hddtemp`, `htop`, `iftop`, `iostat`, `iotop`, `ipmitool`, `journalctl`, `logrotate`, `mpstat`, `netstat`, `nload`, `nvidia-smi`, `perf`, `pmap`, `ps`, `rsyslog`, `sar`, `smartctl`, `strace`, `tcpdump`, `tripwire`, `top`, `vmstat`, `vnstat`

