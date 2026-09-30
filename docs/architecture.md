# Lab Architecture

The lab consists of a Wazuh server and an Ubuntu endpoint running as separate virtual machines.

## Components

- Wazuh Server
- Ubuntu Endpoint
- Wazuh Agent
- VirtualBox virtual network

## Log Flow

Ubuntu Endpoint
↓
Wazuh Agent
↓
Wazuh Manager
↓
Wazuh Analysis Engine
↓
Wazuh Dashboard
↓
SOC Analyst Investigation
