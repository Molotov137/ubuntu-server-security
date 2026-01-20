# Contributing to Ubuntu Server Security

First off, thank you for considering contributing to Ubuntu Server Security!

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Development Setup](#development-setup)
- [Style Guidelines](#style-guidelines)
- [Commit Messages](#commit-messages)
- [Pull Request Process](#pull-request-process)

## Code of Conduct

This project adheres to the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md).
By participating, you are expected to uphold this code.

## Getting Started

- Make sure you have a [GitHub account](https://github.com/signup)
- Check existing [issues](https://github.com/fidpa/ubuntu-server-security/issues) before creating new ones
- Fork the repository on GitHub

## How to Contribute

### Reporting Bugs

Before creating bug reports, please check existing issues.

**Great bug reports include:**
- A clear, descriptive title
- Steps to reproduce the issue
- Expected vs actual behavior
- System information (Ubuntu version, shell version)
- Relevant logs or error messages

### Suggesting Features

Feature suggestions are welcome! Please:
- Check if the feature was already requested
- Describe the use case clearly
- Explain why this would benefit users

### Security Vulnerabilities

**DO NOT** open public issues for security vulnerabilities.

See [SECURITY.md](SECURITY.md) for responsible disclosure.

### Pull Requests

1. Fork the repo and create your branch from `main`
2. Make your changes
3. Test on Ubuntu 22.04 or 24.04
4. Ensure all scripts pass `shellcheck`
5. Update documentation if needed
6. Submit a pull request

## Development Setup

```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/ubuntu-server-security.git
cd ubuntu-server-security

# Verify shellcheck is installed
shellcheck --version

# Run shellcheck on all scripts
find . -name "*.sh" -exec shellcheck {} \;
```

### Testing Environment

Recommended: Use a VM or container for testing security configurations.

```bash
# Example with LXD
lxc launch ubuntu:22.04 security-test
lxc exec security-test -- bash
```

## Style Guidelines

### Bash Scripts

- Use `shellcheck` for linting
- Follow `set -uo pipefail` pattern
- Use lowercase for variables, UPPERCASE for constants
- Quote variables: `"$var"` not `$var`
- Add comments for complex logic

### Configuration Files

- Include comments explaining each setting
- Provide safe defaults
- Document security implications

### Documentation

- Use Markdown
- Include code examples
- Keep lines under 100 characters
- Add TL;DR for long documents

## Commit Messages

Follow conventional format:
```
type: short description

Longer explanation if needed.

Fixes #123
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

**Examples:**
- `feat: add fail2ban jail for postfix`
- `fix: correct sshd_config permissions`
- `docs: update nftables examples`

## Pull Request Process

1. Update README.md if needed
2. Update CHANGELOG.md with your changes
3. PRs require one maintainer approval
4. Squash commits before merging

### PR Checklist

- [ ] Code follows style guidelines
- [ ] Shellcheck passes without errors
- [ ] Tested on Ubuntu 22.04 or 24.04
- [ ] Documentation updated
- [ ] CHANGELOG.md updated

## Questions?

- Open a [Discussion](https://github.com/fidpa/ubuntu-server-security/discussions)
- Check existing documentation

---

Thank you for contributing to Ubuntu Server Security!
