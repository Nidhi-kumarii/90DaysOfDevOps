Log File Analysis with AWK, Grep & Sed

Logs are crucial in DevOps! You’ll analyze logs using the Linux_2k.log file from LogHub (GitHub Repo).

Task:
Download the log file from the repository.
Extract insights using commands:
Use `grep` to find all occurrences of the word "error".
Use `awk` to extract timestamps and log levels.
Use `sed` to replace all IP addresses with [REDACTED] for security.
Bonus: Find the most frequent log entry using 'awk' or 'sort | uniq -c | sort -nr | head -10'.

solution 


Log File Analysis with grep, awk & sed

Logs are crucial in DevOps for troubleshooting and monitoring. Linux offers powerful text processing tools:

`grep` - search for patterns in files . EXAMPLE

```bash
  grep "error" Linux_2k.log
```
`awk` - pattern scanning and processing, ideal for extracting columns. Example: Extract timestamp and log level:

```bash
  awk '{print $1, $2, $3}' Linux_2k.log
```

`sed` - stream editor for transforming text. Example: Mask IP addresses:

```bash
  sed -E 's/[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+/[REDACTED]/g' Linux_2k.log
```

Find most frequent log entries:

```bash
  awk '{print $0}' Linux_2k.log | sort | uniq -c | sort -nr | head -10
```
