# Information Gathering Summary

## Overview
Information gathering is the first phase of a penetration test. The goal is to collect useful details about a target before any exploitation begins. Good recon improves later enumeration, scanning, and attack planning.

## Scoping
Scoping defines what is allowed during an assessment. It tells you which targets, ranges, services, and techniques are in scope, and what is out of bounds. Clear scope keeps the test legal, focused, and easier to document.

## Why User Information Matters
Employee and user information can be very valuable during an engagement. It can support password spraying, brute-force attempts, phishing, or malicious email-based delivery if the rules of engagement allow it. The more accurate information you have, the more effective your enumeration and targeting can be.

## Active vs Passive Reconnaissance

### Active Information Gathering
Active recon interacts directly with the target. It can reveal live hosts, open ports, services, and configurations, but it is more likely to be detected by IDS, firewalls, or monitoring tools.

Common examples:

- Port scanning with `nmap`
- Host discovery
- DNS zone transfer testing
- Service and version detection

### Passive Information Gathering
Passive recon collects information without directly engaging the target systems. It relies on public data, search engines, DNS intelligence, third-party sites, and metadata. This approach is usually stealthier because the target is not directly aware of the activity.

Common examples:

- WHOIS lookup
- Google dorking
- Netcraft recon
- Subdomain enumeration with Sublist3r
- `theHarvester`
- DNS recon
- WAF detection
- Website footprinting

## Passive Recon Topics

### WHOIS Lookup
WHOIS is used to identify domain registration details such as the registrar, creation date, nameservers, and contact or administrative information.

### DNS Recon
DNS recon helps identify important DNS records and infrastructure.

Common record types:

- `A`: IPv4 address
- `AAAA`: IPv6 address
- `MX`: mail server
- `NS`: authoritative name server
- `TXT`: verification and policy records
- `SOA`: zone administration details
- `CNAME`: hostname alias
- `SRV`: service and port mapping
- `PTR`: reverse DNS lookup

Tools and sources mentioned in the notes:

- `dnsrecon`
- `dnsdumpster`
- `dnssubster`

### Google Dorking
Google dorking uses advanced search queries to find exposed files, directories, login pages, backups, and other sensitive material. It can also help uncover leaked credentials or documentation through search engine indexes.

Useful idea from the notes:

- Search engines index page titles, keywords, and URLs rather than every live page in real time.

### Netcraft
Netcraft can be used for website footprinting. It helps gather information about hosted services and the overall structure of a website.

### Subdomain Enumeration with Sublist3r
Sublist3r is a subdomain enumeration tool that helps discover subdomains belonging to a target domain.

### theHarvester
theHarvester is a Python-based OSINT tool used to gather email addresses, hostnames, subdomains, and other public intelligence about a domain.

### WAF Detection
WAF detection helps identify whether a website is protected by a web application firewall. The notes mention `wafw00f` as a tool for this purpose.

### Website Host and Footprinting
Website footprinting helps determine what technologies are behind a site and how it is exposed.

Key ideas from the notes:

- The `host` command can resolve the IP address of a website.
- Multiple IP addresses may suggest a proxy, load balancer, or filtering layer.
- `robots.txt` shows crawler instructions and may reveal hidden directories.
- `sitemap.xml` lists pages that site owners want search engines to know about.
- `Wappalyzer` or `BuiltWith` can identify technologies in use.
- `whatweb` can reveal useful web stack information.
- `webhttrack` can mirror a website for offline review.

## Active Recon Topics

### Host Discovery
Host discovery is used to identify live systems on a network. The notes reference `nmap` as the tool for this step.

### DNS Zone Transfer
Zone transfer testing checks whether a DNS server allows unauthorized replication of DNS data. If successful, it can reveal hostnames and subdomains from the zone.

Tools mentioned:

- `dnsenum`
- `dig`

### Port Scanning
Port scanning identifies open ports and services on a target. The notes cover several `nmap` scan styles.

Common scan ideas from the notes:

- Default scan of the first 1024 ports
- Fast scan
- UDP scan
- Treat all hosts as up and skip host discovery
- Aggressive scan using `-A`
- Timing templates from `-T0` to `-T5`
- Output export to a text file

## Common Recon Workflow
1. Define the scope.
2. Collect passive intelligence from public sources.
3. Identify technologies, subdomains, DNS data, and exposed web content.
4. Move into active checks such as host discovery, port scanning, and zone transfer testing where allowed.
5. Document everything clearly for later enumeration and exploitation phases.

## Lab Takeaways
The assessment lab notes highlight a few recurring recon clues:

- `robots.txt` can reveal what the site owner wants crawlers to avoid.
- The running website and its version are useful early fingerprints.
- Directory browsing may expose file locations.
- Backup files in the web root can leak sensitive configuration data.
- Mirrored or archived files may expose information that is not obvious on the live site.

## Short Version
Information gathering is about collecting the right details with the least risk. Passive recon uses public sources and avoids direct contact, while active recon interacts with the target to verify live systems and services. Together, they create the foundation for accurate enumeration and better testing decisions.