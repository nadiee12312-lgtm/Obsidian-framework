
# ⬛ OBSIDIAN Investigator

[![GitHub Stars](https://img.shields.io/github/stars/nadiee12312-lgtm/Obsidian-framework?style=social)](https://github.com/nadiee12312-lgtm/Obsidian-framework)
[![GitHub Issues](https://img.shields.io/github/issues/nadiee12312-lgtm/Obsidian-framework)](https://github.com/nadiee12312-lgtm/Obsidian-framework/issues)
[![Platform](https://img.shields.io/badge/platform-Linux-blue)](https://github.com/nadiee12312-lgtm/Obsidian-framework)

> **Free OSINT framework. Runs 100% on your machine.**
> No subscriptions. No cloud. No tracking.
> ⚠ Linux only (x86_64) — Mac and Windows support coming soon.

---

## What is OBSIDIAN?

OBSIDIAN is a local OSINT investigation tool with a web interface you can access from any device — including your phone. Enter a name, username, domain, IP or email and OBSIDIAN gathers everything automatically, builds a relationship graph and lets you export a full report.

No data leaves your machine.

---

## What's included (free)

- 🔍 **Persona** — name search across public sources, social profiles, breach data
- 👤 **Username** — checks 10+ platforms simultaneously
- 🌐 **Domain** — WHOIS, DNS records, subdomains (crt.sh), HTTP headers, Wayback Machine
- 🖥 **IP** — geolocation, ASN, PTR, open ports (top 20)
- 📧 **Email** — breach check (HIBP), SPF/DKIM/DMARC, spoofability
- 📱 **Phone** — carrier, line type, country
- 🔐 **SSL** — cipher analysis, HSTS, certificate info
- 🗂 **Metadata** — EXIF data from images and files
- 🕸 **Relationship graph** — all data connected visually, auto-updated
- 📅 **Timeline** — chronological view of all findings
- 📁 **Case management** — save, load and export cases as HTML reports
- 📱 **Mobile UI** — works on your phone via local network

---

## Installation

**Requirements:** Linux x86_64 · 4GB RAM · No dependencies (self-contained)

```bash
# Download
wget https://github.com/nadiee12312-lgtm/Obsidian-framework/releases/latest/download/obsidian-v1.1-linux-x86_64.tar.gz

# Extract and install
tar -xzf obsidian-v1.1-linux-x86_64.tar.gz && cd obsidian-dist
bash obsidian_install.sh
Start OBSIDIAN:
obsidian-web

Open: http://localhost:8767
From your phone: http://YOUR-LOCAL-IP:8767

---
⚖️ Legal & Ethical Use

OBSIDIAN gathers publicly available information for legal and authorized purposes only — security research, your own digital footprint, authorized investigations and education.

You are responsible for complying with the laws of your jurisdiction. Do not use OBSIDIAN for harassment, stalking, doxxing, or any illegal activity. The author is not responsible for misuse.

---
Want more?

OBSIDIAN Investigator covers the essentials. If you need deeper recon, offensive tools and AI-powered analysis, check out the paid tiers:

obsidian.pro — Analyst ($9) · Professional ($20)

---
Found a bug?

Open an issue here → github.com/nadiee12312-lgtm/Obsidian-framework/issues

Include: your OS and what happened.

---
⭐ If OBSIDIAN is useful to you, star the repo — it helps more people find it.

Questions? nadiee567@gmail.com

