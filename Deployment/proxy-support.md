---
layout: default
title: Proxy Support
parent: Deployment
---

# Proxy Support
> 🆕 Introduced in v9.0.1

Follow alternative steps to run installer script.
```
export https_proxy=http://proxy_host:proxy_port
wget https://raw.githubusercontent.com/dnif/installer/main/install.sh
sh install.sh proxy
```
After selecting Component Type, you will be prompted to enter proxy details.
