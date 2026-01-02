---
aliases:
type: Challenge
createdon: 2026-01-01 17:25:45
Room Url: https://tryhackme.com/room/lookup
Difficulty: Easy
Status: InProgress
---
# Lookup

## nmap

```
nmap -T4 -p- -sS -sV 10.67.135.54 -oG Lookup.txt
Starting Nmap 7.80 ( https://nmap.org ) at 2026-01-02 01:29 GMT
Nmap scan report for 10.67.135.54
Host is up (0.00023s latency).
Not shown: 65533 closed ports
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 8.2p1 Ubuntu 4ubuntu0.9 (Ubuntu Linux; protocol 2.0)
80/tcp open  http    Apache httpd 2.4.41 ((Ubuntu))
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 9.13 seconds
```

