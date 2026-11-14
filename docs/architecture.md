# SOC Home Lab Architecture

## Objective
Build an isolated security monitoring environment with Wazuh and one or more monitored endpoints. This is a **planned architecture**, not evidence of deployment.

```text
Host computer
└── Private virtual lab network
    ├── Ubuntu Server VM: Wazuh server + indexer + dashboard
    └── Windows or Ubuntu VM: Wazuh agent
              │
              └── security events → Wazuh manager → indexer → dashboard
```

## Recommended minimum planning
- A host with 16 GB RAM or more is preferable for an all-in-one Wazuh VM and endpoint VM.
- Wazuh server VM: start from current official quickstart sizing and adapt to available hardware.
- Isolated or NAT networking as appropriate; do not expose the dashboard to the public internet.
- Take VM snapshots before changing configurations.

## Data flow
1. Endpoint generates authentication and file events.
2. Wazuh agent forwards events to the manager.
3. Wazuh rules correlate and classify alerts.
4. Analyst reviews alerts in the dashboard and records evidence.

## Safety
Only monitor systems you own or have permission to use. Do not publish private IPs, credentials, tokens, or unredacted logs.
