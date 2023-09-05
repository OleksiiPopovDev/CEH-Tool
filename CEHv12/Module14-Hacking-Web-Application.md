[Home](../README.md)
# Module 14: Hacking Web Application

## Footprint the Web Infrastructure
### Perform Web Application Reconnaissance using Nmap and Telnet
Use tools such as Netcraft (https://www.netcraft.com), SmartWhois (https://www.tamos.com), WHOIS Lookup (https://whois.domaintools.com), and Batch IP Converter (http://www.sabsoft.com) to perform the Whois lookup.
Use tools such as, DNSRecon (https://github.com), and DNS Records (https://network-tools.com), Domain Dossier (https://centralops.net) to perform DNS interrogation.

```nmap -T4 -A -v [Target Web Application]``` - The result appears, displaying the open ports and services running on the machine hosting the target website.

### Perform Web Application Reconnaissance using WhatWeb
```whatweb -v [Target Web Application]``` - The result appears, displaying a detailed report on the target website such as its IP address, plugin information, and HTTP header information, as shown in the screenshot.

![screenshots/module14-1.png](screenshots/module14-1.png)

OWASP Zed Attack Proxy (ZAP) is an integrated penetration testing tool for finding vulnerabilities in web applications. In the Terminal window, type ```zaproxy``` and press Enter to launch OWASP ZAP.

### Detect Load Balancers using Various Tools
```dig yahoo.com``` - The result appears, displaying the available load balancers of the target website, as the screenshot demonstrates. Here, a single host resolves to multiple IP addresses, which possibly indicates that the host is using a load balancer.
![img_1.png](screenshots/module14-2.png)

```lbd yahoo.com``` - The result appears, displaying the available DNS load balancers used by the target website, as shown in the screenshot.
![img_2.png](screenshots/module14-3.png)

### Identify Web Server Directories using Various Tools
```nmap -sV --script=http-enum [target domain or IP address]``` - The result appears, displaying open ports and services, along with their version.

```python3 dirsearch.py -u http://www.moviescope.com``` https://github.com/maurosoria/dirsearch -
![img_3.png](screenshots/module14-4.png)


## Identify XSS Vulnerabilities in Web Applications using PwnXSS
```python3 pwnxss.py -u http://testphp.vulnweb.com``` https://github.com/pwn0sec/PwnXSS