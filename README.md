# Passive OSINT Investigation — NIIT Port Harcourt (NIIT PH)

A passive Open Source Intelligence (OSINT) reconnaissance project conducted against the publicly available digital footprint of NIIT Port Harcourt, an IT training center. Built as part of a cybersecurity portfolio.

## Objective

Demonstrate the OSINT methodology used in the early, passive reconnaissance phase of a security assessment — mapping an organization's external attack surface and personnel structure using only publicly available tools and data sources.

## Scope & Rules of Engagement

- Passive, publicly available information only.
- No active scanning, exploitation, login attempts, or unauthorized access of any kind.
- No contact was made with any individuals identified during the investigation.
- Educational / portfolio purpose only.

## Methodology

The investigation was broken into three phases:

1. **Domain & Infrastructure** — WHOIS, subdomain enumeration, DNS records, hosting/IP analysis
2. **People** — publicly listed personnel and organizational structure via LinkedIn
3. **Digital Footprint** — breach exposure check via Have I Been Pwned

## Tools Used

| Category | Tools |
|---|---|
| Domain / WHOIS | whois.com |
| Certificate transparency / subdomains | Merklemap (crt.sh alternative) |
| DNS records | dnschecker.org, `nslookup` |
| Infrastructure / exposed services | Shodan |
| People / org structure | LinkedIn |
| Breach exposure | Have I Been Pwned |

## Key Findings

- Domain (`niitph.com`) registered May 2025, actively developed, fronted by Cloudflare.
- ~23 subdomains discovered, including production-facing (`login`, `portal`, `app`, `api`) and non-production (`staging`, `dev`) environments.
- No email infrastructure (MX/SPF) currently active on the apex domain.
- Origin server is not exposed to direct internet-wide scanning — masked behind Cloudflare.
- Personnel identified include an IT management role with likely elevated platform access.
- No breach exposure found for the generic address tested.

Full methodology, screenshots, and risk analysis are in the [full report](./OSINTreport.pdf).

## Disclaimer

This project is for educational and portfolio purposes only. All information gathered was publicly available at the time of research. No systems were accessed, scanned actively, or interacted with beyond passive, publicly available lookups.
