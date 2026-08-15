# 🧪 Cybersecurity Home Lab

A practical home-lab track for developing and documenting cybersecurity skills through **Linux, containers, networking, monitoring, and controlled security testing**.

> **Current status:** This document describes the lab direction and the areas currently being practiced. It does not claim that every experiment below has already been completed.

## 🎯 Purpose

The goal is to build a reproducible environment where security concepts can be tested safely against systems I own or explicitly control.

Key learning areas:

- Linux administration and security
- Docker/container fundamentals
- Network segmentation and traffic observation
- Security monitoring and logging
- Vulnerability assessment
- Detection engineering
- Incident investigation

## 🗺️ Target Architecture

```text
                         Windows Host
                              |
                           Docker
                              |
              +---------------+----------------+
              |               |                |
              v               v                v
        Security Workstation  Linux Target   Web Target
              |               |                |
              +---------------+----------------+
                              |
                         Logs / Traffic
                              |
                              v
                       Wazuh / Analysis
```

The exact architecture will evolve as additional components are added and validated.

## 🔐 Safety Boundaries

All offensive-security testing is limited to:

- self-owned systems;
- intentionally vulnerable training systems; or
- environments for which explicit authorization exists.

No public targets, real credentials, or third-party systems are used for experimentation.

## 🔧 Current / Planned Areas

### Linux

- User and group management
- SSH configuration and log analysis
- File permissions
- UFW/firewall configuration
- Process and service inspection

### Docker

- Container lifecycle management
- Image/container inspection
- Network configuration
- Volume and secret-handling concepts
- Container isolation and hardening

### Monitoring

- Wazuh agent integration
- Authentication-event analysis
- Suspicious activity detection
- Log collection and correlation

### Security Testing

Controlled exercises may include vulnerability assessment, web-security labs, network discovery, and attack simulation strictly inside the isolated lab.

## 📋 Experiment Record Template

Every completed experiment should document:

1. **Objective**
2. **Environment**
3. **Configuration**
4. **Test procedure**
5. **Observed evidence**
6. **Analysis**
7. **Security implications**
8. **Mitigation / hardening**
9. **Limitations**
10. **Lessons learned**

This structure is intended to make the work reproducible rather than simply listing commands used during setup.

## 🚧 Next Experiments

- Document the final Docker network architecture.
- Add a controlled Linux authentication investigation.
- Correlate network activity with Wazuh alerts.
- Document container-security observations.
- Add a small incident-response exercise.

## 🎓 Why This Lab Matters

The lab connects academic Information Technology knowledge with practical cybersecurity work. It is intended to demonstrate **problem solving, experimentation, system understanding, and defensive analysis** rather than certificate collection.