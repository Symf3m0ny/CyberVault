---
aliases:
type:
createdon: 2026-01-01 16:56:52
---
# Enumeration

## nmap
See Also [[nmap]]

For an initial scan I like to just scan all ports at a -T4 speed using a SYN Scan and getting probing open ports for Version information. I also like to output to a Grepable file for use later.

```bash
nmap -T4 -p- -sS -sV $target_ip -oG $target_ip
```

## gobuster
See Also [[gobuster]]