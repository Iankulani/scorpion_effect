# 🦂 SCORPION-EFFECT v2.0

<img width="900" height="500" alt="scorpion" src="https://github.com/user-attachments/assets/f02c86a8-6813-41cb-91ae-100869eee4c7" />


[![GitHub stars](https://img.shields.io/github/stars/Iankulani/scorpion-effect)](https://github.com/Iankulani/scorpion-effect/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Iankulani/scorpion-effect)](https://github.com/Iankulani/scorpion-effect/network)
[![GitHub issues](https://img.shields.io/github/issues/Iankulani/scorpion-effect)](https://github.com/Iankulani/scorpion-effect/issues)
[![Docker Pulls](https://img.shields.io/docker/pulls/iankulani/scorpion-effect)](https://hub.docker.com/r/iankulani/scorpion-effect)
[![License](https://img.shields.io/github/license/Iankulani/scorpion-effect)](LICENSE)
[![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)



Scorpion Effect is a powerful, modular cyber operations platform designed to simulate, monitor, and manage real-world cybersecurity scenarios across multiple environments. Built with flexibility and precision in mind, it serves as a unified toolkit for professionals and learners across the cybersecurity spectrum.

At its core, Scorpion Effect enables seamless interaction between different cybersecurity roles, including white hat hackers (ethical security testers), black hat simulation environments (for controlled research), red teams (offensive security), and blue teams (defensive security). This integrated approach allows users to test vulnerabilities, simulate attacks, and strengthen defenses within a controlled and customizable ecosystem.


## 🎯 Features

### Social Engineering Suite
- **Phishing Campaigns**: Facebook, Instagram, Twitter, Gmail, LinkedIn, Microsoft, Google, Apple
- **QR Code Generation**: Auto-generate QR codes for phishing links
- **Credential Capture**: Real-time credential harvesting with IP logging
- **URL Shortening**: Obfuscate phishing links with multiple services

### Multi-Platform Bot Integration
- 🤖 **Discord**: Full command execution via Discord bot
- 📱 **Telegram**: Complete C2 functionality
- 💼 **Slack**: Enterprise messaging platform support
- 🌐 **Google Chat**: Webhook-based communication
- 🖥️ **Web Terminal**: Browser-based command interface

### Network Operations
- 🔍 **Port Scanning**: Nmap integration for comprehensive scanning
- 🌐 **Traffic Generation**: ICMP, TCP, UDP, HTTP traffic simulation
- 📡 **Network Discovery**: ARP spoofing, network mapping
- 🛡️ **IP Management**: Block/allow list with iptables integration

### Security Features
- 🚨 **Threat Detection**: Real-time threat monitoring
- 📊 **Database Logging**: SQLite/PostgreSQL for persistent storage
- 🔒 **Encryption**: Secure credential storage
- 📈 **Analytics**: Command history, statistics, performance metrics

## 🚀 Quick Start

### Docker (Recommended)


# Clone repository
```bash
git clone https://github.com/Iankulani/scorpion_effect.git
cd scorpion-effect

```

# Start with Docker Compose
```bash
docker-compose up -d
```
# Access web interface
```bash
open http://localhost:5000
```

# Manual Installation
# Linux/Mac

```bash
chmod +x install.sh
./install.sh
./start_scorpion.sh
```
# Windows
```bash
batch_install.bat
scorpion_venv\Scripts\python scorpion_effect.py
```
Using Python
# Create virtual environment
```bash
python3 -m venv venv
```
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate  # Windows

# Install dependencies
```bash
pip install -r requirements.txt
```
# Run application
```bash
python3 scorpion_effect.py
```
# 📋 Docker Commands

# Build Alpine image
```bash
docker build -t scorpion-effect:alpine -f Dockerfile .
```
# Run container

```bash
docker run -d -p 5000:5000 -p 8080:8080 --name scorpion scorpion-effect:alpine
```
# View logs
```bash
docker logs -f scorpion
```
# Stop container
```bash
docker stop scorpion
```
# 🔧 Configuration
Edit .scorpion-effect/config.json:
```bash
json
{
    "discord_token": "YOUR_DISCORD_BOT_TOKEN",
    "telegram_api_id": "YOUR_API_ID",
    "telegram_api_hash": "YOUR_API_HASH",
    "telegram_bot_token": "YOUR_BOT_TOKEN",
    "slack_token": "xoxb-your-token",
    "web_port": 5000,
    "enable_discord": true,
    "enable_telegram": true,
    "enable_slack": true
}
```

# 🎮 Command Reference
# Social Engineering
```bash
phish_facebook      # Generate Facebook phishing link
phish_instagram     # Generate Instagram phishing link
phish_twitter       # Generate Twitter phishing link
phish_gmail         # Generate Gmail phishing link
phish_start <id>    # Start phishing server
phish_stop          # Stop phishing server
phish_creds         # View captured credentials
```
# Network Scanning

```bash
scan <target>       # Quick port scan
nmap <target>       # Full nmap scan
ping <target>       # ICMP echo request
traceroute <target> # Network path tracing
whois <domain>      # WHOIS lookup
```
# Traffic Generation

```bash
traffic icmp <ip> <duration>  # ICMP flood
traffic tcp <ip> <duration>   # TCP connections
traffic http <ip> <duration>  # HTTP requests
```
# System Management
```bash
status              # Show system status
history            # Command history
sysinfo            # System information
add_ip <ip>        # Add IP to monitoring
block_ip <ip>      # Block IP address
```
# 🌐 Web Interface
```bash
Access the web terminal at http://localhost:5000
```

# Features:

* Real-time command execution

* Scorpion stinger game

* Visual terminal interface

* Multi-session support

# 🐳 GitLab CI/CD Pipeline

The .gitlab-ci.yml provides:

* Security Scan: Bandit, Safety checks

* Build: Multi-stage Alpine Docker builds

* Test: Unit, integration, performance tests

* Deploy: Staging/Production deployment


# 🔐 Security Notice

IMPORTANT: This tool is for authorized security testing and educational purposes only. Users must:

* Obtain written permission before testing

* Comply with all applicable laws

* Not use for unauthorized activities

* Report vulnerabilities responsibly

# Star Hisotry
