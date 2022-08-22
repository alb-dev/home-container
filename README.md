# home-container
Docker Apps for Home

# Install requirements
```
ansible-galaxy install -r roles/requirements.yml
```

# Usage
## Tag Management
Applications can be installed with targeting via tag 

### Example
```
ansible-playbook -i inventory/homeserver.yml playbooks/main.yaml -u your user
```