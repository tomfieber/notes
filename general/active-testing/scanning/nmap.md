---
description: General Nmap commands for discovery, TCP, and UDP scans.
---

# Nmap

### Discovery Scan

{% code overflow="wrap" %}
```bash
sudo nmap -iL scope.txt -sn -PS21,22,23,25,80,110,135,137,139,389,443,445,636,990,992,1433,2049,3306,5060,8080,8090,8088,8888,9090,10000 -PU53,69,88,123,161,500,514,623,5060 -PE
```
{% endcode %}

### TCP Scan

{% code overflow="wrap" %}
```bash
sudo nmap -iL alive-hosts.txt -Pn -p- -O --max-rtt-timeout 1000ms --max-retries 2 -oA nmap_tcp -vv --open -A
```
{% endcode %}

### UDP Scan

{% code overflow="wrap" %}
```bash
sudo nmap -iL alive-hosts.txt -Pn -n -sU -p 53,67-69,111,123,135,137-139,161-162,445,500,514,520,623,631,996-999,1434,1701,1900,3283,4500,5353,49152-49154 -O --max-rtt-timeout 600ms --max-retries 2 -oA nmap_udp -vv --open -A
```
{% endcode %}



