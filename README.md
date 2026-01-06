# Configuration Management with Ansible

An Ansible playbook for automated Linux server configuration.

## What It Does

Automates server setup with four core roles:
- **base** - Updates server and installs essential utilities
- **ssh** - Configures SSH access with public key
- **nginx** - Installs and starts nginx web server
- **app** - Deploys static website from tarball or GitHub

## Prerequisites

- Linux server (Ubuntu/Debian)
- Ansible installed locally
- SSH access to target server

## Setup

1. Update `inventory.ini` with your server details:
```ini
[webservers]
your-server ansible_host=YOUR_IP ansible_user=ubuntu ansible_ssh_private_key_file=/path/to/key.pem
```

2. Run the playbook:
```bash
# Run all roles
ansible-playbook setup.yml

# Run specific role
ansible-playbook setup.yml --tags "app"
```

## Available Tags

- `base` - Basic server setup
- `ssh` - SSH configuration
- `nginx` - Web server installation
- `app` - Application deployment

## Project Structure

```
configuration-management/
├── setup.yml          # Main playbook
├── inventory.ini      # Server inventory
├── base/             # Base role
├── ssh/              # SSH role
├── nginx/            # Nginx role
└── app/              # App deployment role
```

**Project URL:** https://roadmap.sh/projects/configuration-management