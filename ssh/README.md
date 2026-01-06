# SSH Role

Configures SSH access with public key authentication.

## What It Does

- Creates `.ssh` directory with proper permissions
- Adds your public SSH key to authorized_keys
- Enables passwordless SSH access

## Setup

Update the public key path in `tasks/main.yml`:
```yaml
key: "{{ lookup('file', '/path/to/your/id_rsa.pub') }}"
```

## Usage

```bash
# Run only ssh role
ansible-playbook setup.yml --tags "ssh"
```

## Result

You can SSH into the server using your private key without password.
