---
layout: default
title: Upgrading to 9.0.2
parent: Deployment
---

# Upgrading to 9.0.2

### Caution: 
The upgrade process will involve in a downtime in log collection.
Please ensure resources are aligned to be able to execute in the shortest possible span.

### Prerequisite:
Uninterrupted internet connectivity from all hosts.

## High-level Steps
1. Stop All Adapters
2. Stop All Datanodes
3. Stop Console (Only if hosted separately from Core)
4. Stop Core
5. Upgrade and Start Core
6. Upgrade and Start Console (Only if hosted separately from Core)
7. Upgrade and Start Datanodes
8. Upgrade and Start Adapters
9. Clear your browser cache and login to Console

For all stop steps, run the following command:
```sh
bash -c "$(curl -s https://raw.githubusercontent.com/dnif/installer/main/upgradepre.sh)"
```

For all upgrade steps, run the following command:
```sh
bash -c "$(curl -s https://raw.githubusercontent.com/dnif/installer/main/upgrade.sh)"
```

