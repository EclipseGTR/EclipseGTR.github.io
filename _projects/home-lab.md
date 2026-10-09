---
title: "Security Home Lab"
summary: "A virtualized lab for practicing attacks and detections, with a SIEM collecting logs from Windows and Linux hosts."
tools: [Proxmox, pfSense, Splunk, Sysmon]
featured: true
order: 1
# repo: https://github.com/EclipseGTR/your-repo   # Optional link to source code
---
<!-- This is a sample project. Edit it to describe your own lab, or delete it. -->

## Goal

Build an isolated environment where I can safely run attacks and see what they
look like from the defender's side.

## Architecture

- **Hypervisor:** Proxmox on a spare desktop
- **Network:** pfSense firewall with a separate, isolated lab VLAN
- **Hosts:** Windows Server (Active Directory), Windows 10 client, Kali Linux
- **Monitoring:** Sysmon and the Splunk Universal Forwarder on each host

## What I learned

- How to write a detection for a technique and then test it
- Common Windows event IDs (4624, 4625, 4688) and what they mean
