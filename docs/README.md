# Documentation

This directory contains detailed documentation for Ubuntu Server Security.

## Quick Navigation

| Document | Description | Audience |
|----------|-------------|----------|
| [SETUP.md](SETUP.md) | Initial setup and configuration guide | New users |
| [BEST_PRACTICES.md](BEST_PRACTICES.md) | Security hardening best practices | All users |
| [TROUBLESHOOTING.md](TROUBLESHOOTING.md) | Common issues and solutions | All users |
| [ROADMAP.md](ROADMAP.md) | Project roadmap and planned features | Contributors |

## Integration Guides

| Document | Description |
|----------|-------------|
| [PROMETHEUS_INTEGRATION.md](PROMETHEUS_INTEGRATION.md) | Prometheus metrics and Grafana dashboards |
| [VAULTWARDEN_INTEGRATION.md](VAULTWARDEN_INTEGRATION.md) | Credential management with Vaultwarden |

## Advanced Topics

| Document | Description |
|----------|-------------|
| [FAILURE_ALERTING.md](FAILURE_ALERTING.md) | Alert configuration for security failures |
| [FALSE_POSITIVE_REDUCTION.md](FALSE_POSITIVE_REDUCTION.md) | Tuning to reduce false positives |
| [IMMUTABLE_BINARY_PROTECTION.md](IMMUTABLE_BINARY_PROTECTION.md) | Protecting critical binaries |

## Reading Order for New Users

1. **[SETUP.md](SETUP.md)** - Start here for initial configuration
2. **[BEST_PRACTICES.md](BEST_PRACTICES.md)** - Understand security principles
3. **[TROUBLESHOOTING.md](TROUBLESHOOTING.md)** - Reference when issues arise
4. **[PROMETHEUS_INTEGRATION.md](PROMETHEUS_INTEGRATION.md)** - Optional: Set up monitoring

## Component-Specific Documentation

Each component directory contains its own documentation:

- [fail2ban/](../fail2ban/) - Intrusion prevention
- [ssh-hardening/](../ssh-hardening/) - SSH security
- [nftables/](../nftables/) - Firewall rules
- [aide/](../aide/) - File integrity monitoring
- [lynis/](../lynis/) - Security auditing

## See Also

- [← Back to Repository Root](../README.md)
- [CONTRIBUTING.md](../CONTRIBUTING.md) - How to contribute
- [CHANGELOG.md](../CHANGELOG.md) - Version history
