# home-container
Docker Apps for Home

## Requirements

* Ansible 2.10+

## Tested on

* Fedora Server 36

## Role Variables
This is a copy of `roles/home.apps/defaults/main.yaml`
```yaml
---
#### General ####
SECRET_PRIVATE_DOMAIN: 
UPSTREAM_DNS: 
#### Docker Installation ####
containers_base_dir: /opt/docker_compose
system_base_dir: /opt/docker-system

#### Netcup Settings ####
NETCUP_CUSTOMER_NUMBER: 
NETCUP_API_KEY: 
NETCUP_API_PASSWORD: 
SECRET_NETCUP_EMAIL: 

#### PIHOLE #####
PIHOLE_PASSWORD: 
PIHOLE_DNSSERVER: 

#### Minio ####
SECRET_MINIO_ROOT_USER:
SECRET_MINIO_ROOT_PASSWORD: 

# -- Mosquitto 
MOSQUITTO_SERVICE_IP: 
MOSQUITTO_PW: 
```
## Install requirements
```bash
ansible-galaxy install -r roles/requirements.yml
```
# Usage
## Tag Management
Applications can be installed with targeting via tag 

### Example
This will only install zigbee2mqtt. If no tag is defined all apps will be installed.
Following will only install one app.
```bash
ansible-playbook -i inventory/homeserver.yml playbooks/main.yaml -u your user --tag "zigbee2mqtt"
```