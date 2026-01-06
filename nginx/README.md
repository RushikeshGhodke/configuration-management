# Nginx Role

Installs and configures nginx web server.

## What It Does

- Installs nginx package
- Starts nginx service
- Enables nginx to start on boot

## Usage

```bash
# Run only nginx role
ansible-playbook setup.yml --tags "nginx"
```

## Result

Nginx will be running and accessible on port 80.
