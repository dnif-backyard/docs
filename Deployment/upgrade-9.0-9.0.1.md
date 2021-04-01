---
layout: default
title: Upgrading to 9.0.1
parent: Deployment
---

# Upgrading to 9.0.1

## High-level Steps
1. Stop All Adapters
2. Stop All Datanodes
3. Stop Core
4. Upgrade and Start Core
5. Upgrade and Start Datanodes
6. Upgrade and Start Adapters

For all stop steps, run the following command:
```sh
bash -c "$(curl -s https://raw.githubusercontent.com/dnif/installer/9.0.1/upgradepre.sh)"
```

For all upgrade steps, run the following command:
```sh
bash -c "$(curl -s https://raw.githubusercontent.com/dnif/installer/9.0.1/upgrade-v9.0.1.sh)"
```

### Special note for 9.0 Proxy-enabled Deployments
Edit docker-compose.yml for Core and Adapters.
Add following variable to the pre-existing environment variable.

```
environment:
  - "PROXY=http://proxy_host:proxy_port"
```
