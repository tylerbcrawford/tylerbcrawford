# Tyler Crawford

Self-taught technical support specialist with 15+ years of experience in complex audio hardware/software integration and configuration. I've been in technical support at Studio Economik, Canada's leading high-end retailer of professional audio equipment, since 2009, and a senior technician since 2021: 4,000+ resolved tickets for clients of all technical abilities, mostly Mac-based creative professionals with a driver, firmware, licensing, or network problem standing between them and a session. Outside work I run a [57-service self-hosted environment](https://github.com/tylerbcrawford/infrastructure-showcase) on Ubuntu, joined to a six-node Tailscale fleet, and I recently earned CompTIA Security+ after completing a cybersecurity certificate from the University of Toronto, with Network+ in progress. Alongside the support work, I spent nine years tour-managing and running front-of-house for Juno- and Polaris-nominated artists: 300+ shows in nine countries, configuring IP networks for digital audio (Dante and AES67) and tracking down interference on crowded stages before showtime. That's where the instinct to stay calm and diagnose comes from.

**Cross-platform by necessity:** macOS daily since 2005 and the platform I support professionally · Linux servers and a Linux laptop at home · Windows for PC builds and the occasional user bug report · iOS as a tailnet node.

**How I build:** the infrastructure and tooling repos below were built with Claude Code under my direction. I own the architecture and run them in production; each repo says so at the top. The bootcamp write-ups were prepared the same way from 2024 lab work.

## Production Infrastructure

A real, daily-driver environment, secured and automated end to end.

- **[Infrastructure Showcase](https://github.com/tylerbcrawford/infrastructure-showcase):** Reference architecture for the full 57-service stack: Docker Compose, nginx reverse proxy, Google OAuth2 on every web UI, wildcard SSL via DNS-01, UFW + fail2ban, a 5-wave tiered startup, and a split access model where public services go through OAuth2 and private ones bind only to the Tailscale address.
- **[Tailscale Fleet Watchdog](https://github.com/tylerbcrawford/tailscale-fleet-watchdog):** Per-node self-check plus a REST-API fleet audit for a six-node tailnet. Catches daemon logout, imminent or expired node keys, expiry-config drift, and offline always-on nodes. Bash, cron and launchd, 22 tests.
- **[Server Monitoring Suite](https://github.com/tylerbcrawford/server-monitoring-suite):** Container health, resource-threshold alerts, SSL-expiry checks, and log-health auditing, all with Discord alerting and cooldown/dedup logic.
- **[Restic Backup System](https://github.com/tylerbcrawford/restic-backup-system):** Modular, encrypted, versioned backups with offsite sync to Google Drive or Backblaze B2, retention pruning, and integrity verification.
- **[Boo Bot](https://github.com/tylerbcrawford/boo-bot):** Production Discord bot for the server's community. Rebrands every notification under one identity, suppresses floods, handles requests, and pulls trailers.
- **[Homelab Scripts](https://github.com/tylerbcrawford/homelab-scripts):** Tiered startup, inotify-driven file watchers, and a 6-source API fallback chain for metadata enrichment.

## AI Orchestration & Evaluation

I direct AI agents to build software, and I evaluate those agents for capability and safety.

- **AI Agent Evaluation** at [Mindrift](https://mindrift.ai). I author and calibrate adversarial and capability test cases for LLM-powered agents: indirect prompt-injection red-teaming on one side, MCP-driven capability evals gated by a CI/CD pipeline and an LLM-as-judge review on the other.
- **[Agent Dispatcher](https://github.com/tylerbcrawford/agent-dispatcher):** Web dashboard for orchestrating headless AI coding agents (Claude, Gemini, Codex) against a queue of project tasks. I run it in production for my own projects.
- **[llm-eval-harness](https://github.com/tylerbcrawford/llm-eval-harness):** LLM-as-judge harness that scores model outputs against a rubric and gates CI on the result. Runs fully offline with recorded fixtures.
- **[Subgeneratorr](https://github.com/tylerbcrawford/subgeneratorr):** Subtitle generator that orchestrates Deepgram Nova-3 or local Whisper with your choice of LLM for keyterm extraction and translation. Built to fill the gaps Bazarr can't cover.

## Cybersecurity Projects (UofT, 2024)

- **[Penetration Testing](https://github.com/tylerbcrawford/rekall-penetration-testing):** 3-day pen test covering SQL injection, RCE on Struts/Tomcat, Shellshock, and credential cracking.
- **[Splunk SIEM](https://github.com/tylerbcrawford/vsi-splunk-siem):** Custom detection rules for brute-force, SQLi, and DoS, with incident-response writeups.
- **[Azure Cloud Security](https://github.com/tylerbcrawford/azure-cloud-security):** Multi-VM deployment with NSGs, Jump Box architecture, and Ansible automation.
- **[IoT Vulnerability Analysis](https://github.com/tylerbcrawford/iot-vulnerability-analysis):** TP-Link smart bulb security assessment, CVE reproduction, and MITM demonstration.

## Certifications

- **CompTIA Security+ (SY0-701):** earned 2026
- **CompTIA Network+ (N10-009):** in progress

[![LinkedIn](https://img.shields.io/badge/LinkedIn-tylerbcrawford-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/tylerbcrawford)
