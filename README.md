<p align="center">
  <img src="obsidian-logo.svg" alt="OBSIDIAN" width="130">
</p>

<h1 align="center">OBSIDIAN</h1>

<p align="center"><b>Free, local OSINT framework. Runs 100% on your machine — no cloud, no tracking.</b></p>

---

## What is OBSIDIAN

OBSIDIAN is a local OSINT investigation tool with a web interface you can reach from any device on your network, including your phone. Enter a name, username, domain, IP, email or phone number, and OBSIDIAN gathers public information, builds a relationship graph, and lets you export a full report.

No data ever leaves your machine.

## Features

- **Persona** — name search across public sources, social profiles, breach data
- **Username** — checks 10+ platforms in parallel
- **Domain** — WHOIS, DNS, subdomains (crt.sh), HTTP headers, Wayback Machine
- **IP** — geolocation, ASN, PTR, top-port scan
- **Email** — breach check (HIBP), SPF/DKIM/DMARC, spoofability
- **Phone** — carrier, line type, country
- **SSL** — cipher analysis, HSTS, certificate info
- **Metadata** — EXIF from images and files
- **Relationship graph** — every finding connected visually, auto-updated
- **Timeline** — chronological view of all findings
- **Case management** — save, load and export cases as HTML reports
- **Mobile UI** — works from your phone over the local network

## Requirements

- Linux (x86_64)
- Python 3.7+
- ~4GB RAM

## Installation

```bash
git clone https://github.com/nadiee12312-lgtm/Obsidian-framework
cd Obsidian-framework
pip install -r requirements.txt
python3 obsidian_web.py
```

Then open **http://localhost:8767** in your browser.

### Optional system tools

Some modules use command-line tools. OBSIDIAN runs without them, but installs
them for full functionality:

```bash
# Debian/Ubuntu
sudo apt install nmap whois dnsutils exiftool

# Fedora
sudo dnf install nmap whois bind-utils perl-Image-ExifTool
```

## Access from your phone

By default OBSIDIAN listens only on your own machine (`127.0.0.1`). To reach it
from your phone on the same WiFi:

```bash
OBSIDIAN_HOST=0.0.0.0 python3 obsidian_web.py
```

Then open `http://YOUR-LOCAL-IP:8767` from your phone.

> **Warning:** only expose OBSIDIAN to your network (`0.0.0.0`) on a **trusted** network.
> Anyone who can reach the interface can run its tools from your machine.

## Offensive tools (advanced, optional)

Beyond OSINT, OBSIDIAN can run 88 tools from **Kali, Parrot, REMnux and
BlackArch**, each inside its own [distrobox](https://distrobox.it) container so
they run on any Linux distro without touching your system. These are
**optional** — every OSINT module above works without them.

> These images are large (Parrot and REMnux are 15–20 GB each). Only set up the
> distros you actually want to use.

**1. Install distrobox and a container runtime**

```bash
sudo dnf install distrobox podman     # Fedora
sudo apt install distrobox podman     # Debian/Ubuntu
```

**2. Create the containers — keep these exact names**

```bash
distrobox create --name kali      --image docker.io/kalilinux/kali-rolling
distrobox create --name parrot    --image docker.io/parrotsec/security
distrobox create --name remnux    --image docker.io/remnux/remnux-distro:focal
distrobox create --name blackarch --image docker.io/archlinux:latest
```

OBSIDIAN calls the containers by these names (`kali`, `parrot`, `remnux`,
`blackarch`) — don't rename them.

**3. Install the tools you want inside each**

```bash
distrobox enter kali
sudo apt update && sudo apt install -y nmap sqlmap nikto hydra gobuster
exit
```

(For BlackArch, add the BlackArch repository inside the `archlinux` container
first — see blackarch.org/downloading.html.)

If a distro isn't set up, its tools won't run — but the OSINT modules work
completely independently of them.

## Legal & ethical use

OBSIDIAN gathers **publicly available** information for **legal and authorized
purposes only** — security research, checking your own digital footprint,
authorized investigations, and education.

You are responsible for complying with the laws of your jurisdiction. **Do not**
use OBSIDIAN for harassment, stalking, doxxing, or any illegal activity.

## Found a bug?

Open an issue: **[Issues](https://github.com/nadiee12312-lgtm/Obsidian-framework/issues)**
Include your OS and what happened.

## License

MIT
