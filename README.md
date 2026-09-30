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
