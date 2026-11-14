# SOC Home Lab with Wazuh

> **Portfolio status: documentation and safe test plan prepared; Wazuh has not yet been installed or validated in this repository.** Results will be added only after hands-on testing.

## Project overview
A beginner-friendly Security Operations Centre (SOC) home lab designed to practise endpoint monitoring, SIEM alert triage, log analysis, and incident documentation with [Wazuh](https://wazuh.com/).

### Learning objectives
- Deploy a Wazuh all-in-one stack on a private Ubuntu Server VM.
- Enrol a Windows or Linux test endpoint with a Wazuh agent.
- Generate harmless authentication and file-integrity events.
- Investigate alerts and write an evidence-based SOC report.

## Proposed architecture
```text
Windows/Linux endpoint VM (Wazuh agent)
               |
       Private lab network
               |
Ubuntu Server VM (Wazuh manager + indexer + dashboard)
               |
          Analyst browser
```

## Tools
Wazuh, Ubuntu Server, Windows or Linux test endpoint, VirtualBox/VMware, and GitHub Markdown documentation.

## Getting started
1. Read [setup guide](docs/setup-guide.md) and check host RAM, CPU, disk, and virtualization support.
2. Follow the [official Wazuh quickstart](https://documentation.wazuh.com/current/quickstart.html) for version-specific install steps.
3. Review [architecture](docs/architecture.md) and [security guidance](SECURITY.md).
4. Run the [safe detection test plan](docs/detection-tests.md) **only in your own lab**.
5. Record actual observations in [lab journal](docs/lab-journal.md) and [incident report template](reports/incident-report-template.md).

## Repository structure
```text
README.md
SECURITY.md
.gitignore
config/
  ossec-agent-example.xml
docs/
  architecture.md
  setup-guide.md
  detection-tests.md
  lab-journal.md
  cv-evidence-checklist.md
reports/
  incident-report-template.md
```

## Progress
- [x] Repository created
- [x] Architecture and documentation prepared
- [x] Safe test plan and report template added
- [ ] Wazuh installed
- [ ] Agent enrolled
- [ ] Detection exercises completed
- [ ] Alert screenshots and evidence captured
- [ ] Incident report completed from observed events

## Important limitations
The XML configuration is an illustrative fragment, not a complete drop-in configuration. The repo currently contains **no verified security alerts or scan results**. Do not commit passwords, tokens, raw endpoint logs, or personal information.

## Official documentation
- [Wazuh Quickstart](https://documentation.wazuh.com/current/quickstart.html)
- [Wazuh Agent Installation](https://documentation.wazuh.com/current/installation-guide/wazuh-agent/index.html)
