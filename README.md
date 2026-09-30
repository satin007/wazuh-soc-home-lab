# Wazuh SOC Home Lab

A hands-on Security Operations Center (SOC) home lab built using Wazuh to practice security monitoring, alert analysis, and Linux endpoint investigation.

## Project Overview

This project simulates basic SOC monitoring and investigation activities using a Wazuh server and an Ubuntu Linux endpoint.

Security events generated on the endpoint are collected by the Wazuh agent, analyzed by the Wazuh manager, and presented through the Wazuh dashboard for investigation.

## Lab Architecture

```text
Ubuntu Linux Endpoint
        ↓
   Wazuh Agent
        ↓
   Wazuh Manager
        ↓
Wazuh Analysis Engine
        ↓
 Wazuh Dashboard
        ↓
  SOC Investigation

``` 

## Detection Scenarios

### 1. Suspicious Local User/Group Creation

A test account named `soc-test` was created on the Linux endpoint.

The activity was detected using Wazuh and investigated by verifying:

- User and group information
- Sudo group membership
- Account configuration
- Login history

### 2. SSH Login Attempt Using a Non-Existent User

An SSH login attempt involving the username `soc-attacker` was generated.

The activity was investigated using:

- Wazuh detection
- Linux authentication logs

## Technologies Used

- Wazuh
- Ubuntu Linux
- SSH
- Linux authentication logs
- VirtualBox

## Skills Demonstrated

- SIEM monitoring
- Security alert analysis
- Linux log analysis
- SSH authentication investigation
- User and group investigation
- Basic incident investigation
- Security event validation

## Project Documentation

- [Project Overview](docs/project-overview.md)
- [Lab Architecture](docs/architecture.md)
- [Detection Scenarios](docs/scenarios.md)

## Evidence

- [Scenario 1 Evidence](screenshots/scenario-1/)
- [Scenario 2 Evidence](screenshots/scenario-2/)
