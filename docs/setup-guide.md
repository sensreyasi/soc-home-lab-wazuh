# Installation and Setup Guide

> Status: **Not yet installed or verified**. Follow version-specific official instructions rather than copying outdated installer commands.

## 1. Prepare your computer
Record OS, RAM, CPU, free disk space and whether virtualization is enabled. For low-RAM hosts, consider a single VM or a remote private lab rather than two simultaneous VMs.

## 2. Create an Ubuntu Server VM
- Download Ubuntu Server from https://ubuntu.com/download/server
- Install a supported hypervisor (VirtualBox, VMware, or another compatible option).
- Create a VM with resources consistent with https://documentation.wazuh.com/current/quickstart.html
- Update the OS, configure networking, and snapshot the clean VM.

## 3. Install Wazuh
- Follow https://documentation.wazuh.com/current/quickstart.html for the currently supported all-in-one installation.
- Record the Wazuh version and installation date in `docs/lab-journal.md`.
- Store any generated passwords in a password manager **outside GitHub**.
- Access the dashboard over HTTPS only from your trusted lab network.
- Verify manager, indexer, and dashboard health using the official guide.

## 4. Add an endpoint
- Create a Windows or Linux test VM, or use an endpoint you own.
- In the Wazuh dashboard, follow the official agent deployment wizard for the endpoint OS.
- Point the agent at your manager's **private lab IP**.
- Confirm the endpoint appears as active.

## 5. Test safely
Follow `docs/detection-tests.md` using only your own test account and files. Avoid brute-force tools, production accounts, or unapproved targets.

## 6. Capture evidence
Record screenshots with usernames, IPs, hostnames, and tokens redacted. Document observations in `docs/lab-journal.md` and `reports/incident-report-template.md`.

## Troubleshooting
- Agent offline: check VM connectivity, endpoint agent service, manager address, and firewall rules.
- No alerts: check agent status, log collection, event ingestion, and whether the event matches enabled rules.
- Dashboard unavailable: verify services, allocated resources, and TLS/network access.

## Official references
- https://documentation.wazuh.com/current/quickstart.html
- https://documentation.wazuh.com/current/installation-guide/wazuh-agent/index.html
