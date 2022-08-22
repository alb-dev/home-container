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
This will install only zigbee2mqtt. If no tag is defined all apps will be installed.
Following will only install one app.
```
ansible-playbook -i inventory/homeserver.yml playbooks/main.yaml -u your user --tag "zigbee2mqtt"
```