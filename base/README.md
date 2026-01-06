# Base Role

Performs basic server setup and security hardening.

## What It Does

- Updates all system packages
- Installs essential utilities (vim, git, curl)
- Installs and configures fail2ban for security
- Ensures fail2ban service is running

## Usage

```bash
# Run only base role
ansible-playbook setup.yml --tags "base"
```

## Requirements

- Ubuntu/Debian-based system
- Sudo privileges
