# Tyler Crawford

Fifteen years of customer-facing technical support, then infrastructure. I've been Head of Technical Support at a Montreal pro-audio company since 2021, after a decade as a support technician there: 4,000+ resolved tickets, mostly Mac-based creative professionals with a driver, firmware, licensing, or network problem standing between them and a session. Outside work I run a [57-service self-hosted environment](https://github.com/tylerbcrawford/infrastructure-showcase) on Ubuntu, joined to a six-node Tailscale fleet, and I'm CompTIA Security+ certified with Network+ in progress. Before any of that I spent 15 years in live sound, running front-of-house on tour and troubleshooting signal chains and console networks under pressure. That's where the instinct to stay calm and diagnose comes from.

**Cross-platform by necessity:** macOS daily since 2005 and the platform I support professionally · Linux servers and a Linux laptop at home · Windows for PC builds and the occasional user bug report · iOS as a tailnet node.

## Support in the Open

- **Shipping a fix for a stranger's Windows bug.** The first issue on [Subgeneratorr](https://github.com/tylerbcrawford/subgeneratorr) was a Windows user whose containers wouldn't start. Diagnosed CRLF line endings on the entrypoint from the log they pasted, shipped a `.gitattributes` + Dockerfile fix on a branch, and gave them copy-paste steps to verify before merging. [Issue #1](https://github.com/tylerbcrawford/subgeneratorr/issues/1) → [PR #2](https://github.com/tylerbcrawford/subgeneratorr/pull/2).
- **Writing the runbook after the outage.** A silently expired Tailscale node key took my home server off the tailnet. The postmortem became [tailscale-fleet-watchdog](https://github.com/tylerbcrawford/tailscale-fleet-watchdog): the incident, the two bugs the tests didn't catch, and why each design decision was made.
- **Docs that explain the *why*.** The [networking doc](https://github.com/tylerbcrawford/infrastructure-showcase/blob/main/docs/networking.md) for my stack walks DNS layers, address spaces, firewall rules and traffic paths the way I'd explain them to a user, not a machine.

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
