# AppArmor - Mandatory Access Control

Mandatory Access Control (MAC) profiles for database and web services with two-phase deployment.

## Features

- ✅ **Defense-in-Depth** - Restrict program access even when running as root
- ✅ **Production-Ready Profiles** - PostgreSQL 16 profile included
- ✅ **Two-Phase Deployment** - COMPLAIN mode testing, then ENFORCE mode
- ✅ **CIS Benchmark Aligned** - Implements controls 1.6.1.3 and 1.6.1.4
- ✅ **Docker Integration** - Automatic `docker-default` profile for all containers
- ✅ **Rollback-Safe** - Easy switch between COMPLAIN and ENFORCE modes

## Quick Start

```bash
# 1. Verify AppArmor is enabled
sudo aa-status

# 2. Deploy PostgreSQL profile in COMPLAIN mode (testing)
sudo cp profiles/usr.lib.postgresql.16.bin.postgres /etc/apparmor.d/
sudo apparmor_parser -r -C /etc/apparmor.d/usr.lib.postgresql.16.bin.postgres

# 3. After 24-48h testing, switch to ENFORCE mode
sudo aa-enforce /etc/apparmor.d/usr.lib.postgresql.16.bin.postgres
```

**Full guide**: See [docs/SETUP.md](docs/SETUP.md)

## Documentation

| Document | Description |
|----------|-------------|
| [SETUP.md](docs/SETUP.md) | Installation, deployment workflow, and validation |
| [POSTGRESQL_PROFILE.md](docs/POSTGRESQL_PROFILE.md) | PostgreSQL 16 profile reference and permissions |
| [TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md) | Common issues (service won't start, SSL access denied) |

## Requirements

- Ubuntu 22.04+ / Debian 11+ (AppArmor installed by default)
- Root/sudo access
- Target application installed (PostgreSQL, nginx, etc.)

## Available Profiles

| Profile | Target Application | Status |
|---------|-------------------|--------|
| **PostgreSQL 16** | `/usr/lib/postgresql/16/bin/postgres` | ✅ Production-Ready |
| **nginx** | `/usr/sbin/nginx` | 🔄 Planned |
| **Docker** | Built-in `docker-default` | ✅ System Default |

## Use Cases

- ✅ **Database Servers** - Restrict PostgreSQL to only necessary files and capabilities
- ✅ **Web Servers** - Limit nginx/Apache attack surface
- ✅ **Container Hosts** - Automatic Docker profile for all containers
- ✅ **Compliance** - Meet CIS Benchmark MAC requirements
- ✅ **Defense-in-Depth** - Additional layer beyond firewall and file permissions

## Resources

- [Ubuntu AppArmor Wiki](https://wiki.ubuntu.com/AppArmor)
- [CIS Ubuntu Linux Benchmark](https://www.cisecurity.org/benchmark/ubuntu_linux)
- [PostgreSQL AppArmor Wiki](https://wiki.postgresql.org/wiki/AppArmor)

## See Also

- [← Back to Repository Root](../README.md)
- [kernel-hardening](../kernel-hardening/) - Kernel security parameters
- [auditd](../auditd/) - Audit AppArmor denials
- [lynis](../lynis/) - Validates AppArmor configuration
