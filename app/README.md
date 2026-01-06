# App Role

Deploys static website to the server.

## What It Does

- Installs git
- Creates web root directory
- Deploys website using one of two methods:
  - **Tarball**: Uploads and extracts website.tar.gz
  - **GitHub**: Clones repository directly

## Deployment Methods

### Tarball Deployment
1. Place your website tarball at `files/website.tar.gz`
2. Set variable: `deploy_method: "tarball"`

### GitHub Deployment (Stretch Goal)
1. Set variables:
   ```yaml
   deploy_method: "github"
   github_repo: "https://github.com/user/repo.git"
   ```

## Usage

```bash
# Run only app role
ansible-playbook setup.yml --tags "app"
```

## Result

Website files deployed to `/var/www/html/`
