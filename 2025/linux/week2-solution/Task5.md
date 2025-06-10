 Monitoring Processes & Networking Commands

 Background processes and networking tools help keep systems running smoothly.

Start a background process (ping google.com):


```bash
  ping google.com > ping_test.log 2>&1 &
```
Monitor with:

'ps aux | grep ping'

'top' (interactive)

'htop' (better UI for top, if installed)

Kill process by PID:

```bash
  kill <PID>
```
Useful networking commands:

'ifconfig or ip addr' — show network interfaces

'netstat' or 'ss' — show network connections

'traceroute' 'google.com' — track path packets take to reach h

