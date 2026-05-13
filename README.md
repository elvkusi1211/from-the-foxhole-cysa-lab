# From the Foxhole · CySA+ Homelab

A defensive cybersecurity homelab series. Build a working Security Operations Center from scratch in 18 episodes.

[Watch on YouTube](https://www.youtube.com/@FoxholeCyber)

## What you're building

Four network segments, twelve VMs, one firewall, all running on Proxmox. By the end of the series you'll have a working SOC with Wazuh SIEM, Security Onion network monitoring, Greenbone vulnerability scanning, MISP threat intelligence, and the workflows to operate them.

## Who this is for

You're trying to break into cybersecurity. You're studying for CySA+ (CS0-003). You have a spare computer. You learn by doing.

## Episodes

| # | Title | Phase | Runtime |
|---|---|---|---|
| 01 | Welcome to the Lab | Foundation | 5 min |
| 02 | Network Design and Proxmox Bridges | Foundation | 15 min |
| 03 | Installing pfSense | Foundation | 30 min |
| 04 | Building Active Directory | Targets | 20 min |
| 05 | Vulnerable Web Apps and Metasploitable | Targets | 18 min |
| 06 | Wazuh Manager and Agents | Defender Stack | 28 min |
| 07 | Sysmon and Windows Event Tuning | Defender Stack | 20 min |
| 08 | Security Onion and Network Monitoring | Defender Stack | 28 min |
| 09 | Writing Your First Detection Rules | Defender Stack | 22 min |
| 10 | Greenbone Vulnerability Scanning | Defender Stack | 20 min |
| 11 | CVSS Scoring and Prioritization | Defender Stack | 16 min |
| 12 | MISP and Threat Intelligence | Defender Stack | 20 min |
| 13 | Simulated Phishing Attack | Offense | 22 min |
| 14 | Kerberoasting Walkthrough | Offense | 25 min |
| 15 | Lateral Movement Detection | Offense | 22 min |
| 16 | Forensic Triage with SIFT | Workflows | 22 min |
| 17 | Writing the Incident Report | Workflows | 20 min |
| 18 | Exam Strategy and What's Next | Workflows | 14 min |

## Hardware requirements

| | Minimum | Recommended |
|---|---|---|
| CPU | 4 cores with virtualization | 8+ cores, modern generation |
| RAM | 16 GB | 32 to 64 GB |
| Storage | 500 GB SSD | 1 TB NVMe |
| Network | Gigabit wired | Gigabit wired |

If you have less, you can still follow along by powering VMs on and off as needed.

## Repository structure

Each episode has its own folder with the README, commands, and config files used in that video.

- `docs/` — architecture diagram and shared reference material
- `episode-01-welcome/` — episode 1 notes
- `episode-02-network-design/` — bridges and verification commands
- `episode-03-pfsense/` — pfSense install, interface assignments, firewall rules
- (more folders added as episodes are published)

## How to use this repo

1. Watch the episode on YouTube
2. Pause when you need to
3. Refer to the corresponding episode folder for exact commands
4. If something doesn't work, open an issue or comment on the video

## Issues and questions

If you hit a problem following along, open an issue with:
- Which episode
- What command or step
- Exact error message
- Screenshot if visual

I read every one.

## Contributing

This is primarily a teaching resource, but PRs are welcome for:
- Typo fixes
- Command corrections for newer software versions
- Additional troubleshooting notes from your own follow-along

## About

Built by El, a US Navy veteran and cloud engineer. The series is independent and not affiliated with CompTIA, Wazuh, Proxmox, or any other product mentioned.

## License

MIT. Use this however you want. Attribution appreciated but not required.
