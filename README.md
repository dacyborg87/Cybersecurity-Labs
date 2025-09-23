# SOC Home Lab — Wazuh SIEM + Suricata IDS

Hands-on SOC-style environment collecting logs from **Windows 11**, **macOS**, and **Kali** into **Wazuh**, with **Suricata** monitoring network traffic. Screenshots and playbooks included.

> ⚠️ All screenshots are redacted/sanitized; this is a **home lab** only.

## Table of Contents
- [Architecture](#architecture)
- [What this shows](#what-this-shows-recruiter-view)
- [Labs](#labs)
  - [Winlogon brute force](#1-winlogon-brute-force-attck-t1110)
  - [Suspicious PowerShell](#2-suspicious-powershell-t1059001)
  - [Beacon-ish egress](#3-beacon-ish-egress-t1071)
- [Repo Map](#repo-map)
- [Screenshots](#screenshots)
- [Quickstart](#quickstart)

## Architecture
- **Wazuh**: Manager • Indexer • Dashboard (Docker compose)
- **Endpoints**: Windows 11 VM, macOS host, Kali VM
- **IDS**: Suricata on the virtual network interface
