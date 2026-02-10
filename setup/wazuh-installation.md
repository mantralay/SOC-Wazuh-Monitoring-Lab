# Wazuh SIEM Installation Guide

## Objective
To deploy a Wazuh SIEM all-in-one environment for security monitoring and SOC analysis.

## Environment Details
- Operating System: Ubuntu Server 24.04
- Deployment Type: All-in-One (Manager, Indexer, Dashboard)
- Network Mode: NAT
- Monitoring Scope: Local host (Agent ID 000)

## System Requirements
- Minimum 4 GB RAM
- 2 CPU cores
- 40 GB disk space
- Internet connectivity

## Installation Steps

### 1. System Update
sudo apt update && sudo apt upgrade -y

### 2. Install Required Packages
sudo apt install curl unzip -y

### 3. Download Wazuh Installer
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh

### 4. Run All-in-One Installation
sudo bash wazuh-install.sh -a -i

The `-i` flag was used to ignore OS compatibility checks for Ubuntu 24.04.

### 5. Access Dashboard
https://<Ubuntu-IP>

### 6. Login Credentials
- Username: admin
- Password: Auto-generated during installation

### 7. Agent Verification
sudo /var/ossec/bin/agent_control -lc

Expected:
ID 000, Name: wazuh-manager, Status: Active

## Validation
- Logs visible in Security Events dashboard
- Authentication and system logs confirmed

## Outcome
Successfully deployed and validated Wazuh SIEM for SOC monitoring and attack detection.
