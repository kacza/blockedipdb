[![Linux Versions](https://img.shields.io/badge/Linux-iptables-orange)](https://www.netfilter.org/projects/iptables/index.html)<br />
[![FreeBSD Version](https://img.shields.io/badge/FreeBSD-PF-brightgreen)](https://docs.freebsd.org/en/books/handbook/firewalls/)
[![FreeBSD Version](https://img.shields.io/badge/FreeBSD-IPFW-brightgreen)](https://docs.freebsd.org/en/books/handbook/firewalls/)
[![FreeBSD Version](https://img.shields.io/badge/FreeBSD-IPFILTER-brightgreen)](https://docs.freebsd.org/en/books/handbook/firewalls/)

## General info
blockedipdb is my own database containing the IP addresses of crawlers, bots, scanners etc.

## Setup
To get a list of IP addresses from the shell, run the command
```
curl -s https://raw.githubusercontent.com/kacza/blockedipdb/refs/heads/main/blockedipdb.txt | awk 'match($0,/[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+/) {print substr($0, RSTART, RLENGTH)}' | sort -n
```
