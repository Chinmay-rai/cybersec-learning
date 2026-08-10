# Day 66 – Wazuh SOC Lab Infrastructure Setup

## What I Did

- Prepared a fresh Kubuntu system as the host for my Wazuh SOC lab
- Installed and configured VirtualBox for running the lab environment
- Created a Windows virtual machine to act as the monitored endpoint
- Installed Windows and completed the initial system configuration
- Configured network connectivity between the host and Windows VM
- Created a clean baseline snapshot of the Windows endpoint for future security experiments

## Lab Architecture

```text
Kubuntu Host
│
├── Wazuh
│
└── VirtualBox
      │
      └── SOC-WIN01
            └── Windows Endpoint
```

## What I Understood

- A SOC lab requires both a monitoring platform and endpoints that generate security telemetry
- Virtual machines provide an isolated environment for safely generating and investigating security activity
- Maintaining a clean endpoint snapshot makes it easier to reset the environment after experiments

## Concepts Covered

- Virtualization
- Windows Endpoint
- Wazuh SOC Lab
- VirtualBox
- Network Connectivity
- Endpoint Baseline

## Key Takeaways

- Successfully prepared the base infrastructure for my Wazuh SOC lab
- Created a dedicated Windows endpoint for future monitoring and investigation
- Established a clean starting point for hands-on Wazuh experiments

## Next Step

- Deploy Wazuh and connect the Windows endpoint to the Wazuh environment
