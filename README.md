# Tyler Crawford

I build and operate production infrastructure, and direct AI agents to build it faster. Self-taught Linux systems administrator running a [49-service self-hosted environment](https://github.com/tylerbcrawford/infrastructure-showcase) on Ubuntu, CompTIA Security+ certified, CompTIA Network+ in progress. I spent 15 years in live sound and audio engineering — touring, running FOH, troubleshooting signal chains under pressure, before moving into infrastructure and security; that's where the instinct to stay calm and diagnose comes from.

## AI Orchestration & Evaluation

I direct AI agents to build software, and I evaluate those agents for capability and safety.

- **AI Agent Evaluation** at [Mindrift](https://mindrift.ai) *(contract, under NDA)*. I author and calibrate adversarial and capability test cases for LLM-powered agents at a frontier AI lab. The adversarial side is indirect prompt-injection red-teaming against credential-exfiltration and unauthorized-action threat models; the capability side uses multi-source [Model Context Protocol](https://modelcontextprotocol.io/) context corpora with pytest validators, statistical difficulty calibration, and a CI/CD pipeline gated by an LLM-as-judge quality review.
- **[Subgeneratorr](https://github.com/tylerbcrawford/subgeneratorr):** Open-source subtitle generator that orchestrates Deepgram Nova-3 with your choice of LLM (Claude / GPT / Gemini / Ollama) for keyterm extraction. Built to fill the gaps Bazarr can't cover.

## Production Infrastructure

A real, daily-driver environment, secured and automated end to end.

- **[Infrastructure Showcase](https://github.com/tylerbcrawford/infrastructure-showcase):** Reference architecture for the full 49-service stack, covering Docker Compose, nginx reverse proxy, Google OAuth2 on every web UI, wildcard SSL via certbot, fail2ban, and a 5-wave tiered startup that prevents boot-time CPU spikes.
- **[Server Monitoring Suite](https://github.com/tylerbcrawford/server-monitoring-suite):** Observability stack covering container health, resource-threshold alerts, SSL-expiry checks, and log-health auditing, all with Discord alerting and cooldown/dedup logic.
- **[Restic Backup System](https://github.com/tylerbcrawford/restic-backup-system):** Modular, encrypted, versioned backups with offsite Google Drive sync, retention pruning, and integrity verification.
- **[Boo Bot](https://github.com/tylerbcrawford/boo-bot):** Production Discord bot automating the server's community. It rebrands every notification under one identity, suppresses floods, handles requests, and pulls trailers.
- **[Homelab Scripts](https://github.com/tylerbcrawford/homelab-scripts):** Service orchestration and automation, including tiered startup, inotify-driven file watchers, and a 6-source API fallback chain for metadata enrichment.

## Cybersecurity Projects (UofT, 2024)

- **[Penetration Testing](https://github.com/tylerbcrawford/rekall-penetration-testing):** 3-day pen test covering SQL injection, RCE on Struts/Tomcat, Shellshock, and credential cracking.
- **[Splunk SIEM](https://github.com/tylerbcrawford/vsi-splunk-siem):** Custom detection rules for brute-force, SQLi, and DoS, with incident-response writeups.
- **[Azure Cloud Security](https://github.com/tylerbcrawford/azure-cloud-security):** Multi-VM deployment with NSGs, Jump Box architecture, and Ansible automation.
- **[IoT Vulnerability Analysis](https://github.com/tylerbcrawford/iot-vulnerability-analysis):** TP-Link smart bulb security assessment, CVE reproduction, and MITM demonstration.

## Certifications

- **CompTIA Security+ (SY0-701):** earned 2024
- **CompTIA Network+ (N10-009):** in progress (exam summer 2026)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-tylerbcrawford-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/tylerbcrawford)
