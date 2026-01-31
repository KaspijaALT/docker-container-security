# Container Security Lab

## Overview
This project demonstrates hands-on container security practices by deploying,
analyzing, and hardening a vulnerable Dockerized web application. The lab
simulates real-world container security scenarios commonly encountered in
cloud and DevSecOps environments.

The objective of this project is to identify container vulnerabilities,
evaluate the attack surface, and apply security hardening techniques aligned
with industry best practices.

---

## Technologies Used
- Docker
- Docker Compose
- OWASP Juice Shop
- Trivy (Container Vulnerability Scanner)
- Nmap
- Linux Container Security Controls

---

## Architecture
The lab consists of a deliberately vulnerable web application running inside
a Docker container. Security analysis tools are used to assess vulnerabilities
and exposure, followed by container hardening to reduce risk.

Components:
- Vulnerable application container (OWASP Juice Shop)
- Vulnerability scanning tools
- Hardened container runtime configuration

---

## Security Analysis

### Vulnerability Scanning
Container image vulnerabilities were identified using Trivy. The scan reports
highlight known CVEs, severity levels, and affected dependencies within the
container image.

### Network Enumeration
Basic network and service enumeration was performed using Nmap to identify
exposed ports and services, helping assess the external attack surface of the
containerized application.

---

## Container Hardening Measures
The following security controls were applied to improve the container security
posture:

- Dropped all unnecessary Linux capabilities
- Enforced a read-only root filesystem
- Restricted privilege escalation using `no-new-privileges`
- Applied the principle of least privilege at runtime

These measures significantly reduce the potential impact of a container
compromise.

---

## Results
After applying security hardening:
- Container privileges were minimized
- Attack surface was reduced
- Runtime security posture was improved
- Vulnerability risks were better understood and documented

---

## Lessons Learned
- Containers require explicit security configuration to be production-ready
- Vulnerability scanning is critical but must be paired with runtime hardening
- Defense-in-depth is essential in containerized and cloud environments
- Security should be integrated early in the container lifecycle (DevSecOps)

---

## Disclaimer
This project is for educational purposes only. All testing was performed on
intentionally vulnerable applications running in a controlled local
environment.

---

## Author
Kaspars Kusiņš
