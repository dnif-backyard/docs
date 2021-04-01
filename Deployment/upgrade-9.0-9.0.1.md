---
layout: default
title: Upgrading to 9.0.1
parent: Deployment
---

# Upgrading to 9.0.1

### Caution: 
The upgrade process will involve in a downtime in log collection.
Please ensure resources are aligned to be able to execute in the shortest possible span.

### Prerequisite:
Uninterrupted internet connectivity from all hosts.

## High-level Steps
1. Stop All Adapters
2. Stop All Datanodes
3. Stop Core
4. Stop Console (Only if hosted separately from Core)
5. Upgrade and Start Core
6. Upgrade and Start Console (Only if hosted separately from Core)
7. Upgrade and Start Datanodes
8. Upgrade and Start Adapters
9. Clear your browser cache and login to Console

For all stop steps, run the following command:
```sh
bash -c "$(curl -s https://raw.githubusercontent.com/dnif/installer/9.0.1/upgradepre.sh)"
```

For all upgrade steps, run the following command:
```sh
bash -c "$(curl -s https://raw.githubusercontent.com/dnif/installer/9.0.1/upgrade-v9.0.1.sh)"
```

### Special note for 9.0 Proxy-enabled Deployments
After the stop steps and before starting with upgrade steps:
1. Edit docker-compose.yml for Core and Adapters.
2. Add following variable to the pre-existing environment variable.
```
environment:
  - 'PROXY=http://proxy_host:proxy_port'
```
