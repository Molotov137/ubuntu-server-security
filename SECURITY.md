# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.x.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

We take security vulnerabilities seriously. If you discover a security issue,
please report it responsibly.

### DO NOT

- Open a public GitHub issue for security vulnerabilities
- Disclose the vulnerability publicly before it's fixed
- Exploit the vulnerability beyond what's necessary to demonstrate it

### How to Report

1. **Email**: Send details to **security@fidpa.dev**
2. **GitHub**: Use [Private Vulnerability Reporting](https://github.com/fidpa/ubuntu-server-security/security/advisories/new)

### What to Include

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if any)

### What to Expect

- **Acknowledgment**: Within 48 hours
- **Initial Assessment**: Within 7 days
- **Resolution Timeline**: Depends on severity
  - Critical: 24-72 hours
  - High: 1-2 weeks
  - Medium: 2-4 weeks
  - Low: Next release

### After Resolution

- You will be credited in the release notes (unless you prefer anonymity)
- A security advisory will be published
- Fixed versions will be clearly documented

## Security Best Practices

When using this repository:

1. **Always test in a non-production environment first**
2. **Review all configurations before applying**
3. **Keep your system updated**
4. **Monitor logs after applying security configurations**
5. **Have a rollback plan**

## Scope

This security policy covers:

- All configuration files in this repository
- All scripts and automation tools
- Documentation that could lead to misconfigurations

## Out of Scope

- Vulnerabilities in Ubuntu itself (report to [Ubuntu Security](https://ubuntu.com/security))
- Third-party tools (fail2ban, nftables, etc.) - report to respective projects
- Issues caused by user modifications

---

Thank you for helping keep Ubuntu Server Security safe!
