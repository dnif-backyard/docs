---
layout: default
title: Minimum Viable Cluster
parent: Solution Architecture
---

# Minimum Viable Cluster
To get started with DNIF, one needs three nodes.

Node1: 
- Hosts the Core and Console components
- Minimum Configuration **for Production Environments** is 16vCPUs, 32GB RAM, 1TB SSD Disk
- Minimum Configuration is 8vCPU, 16GB RAM and 500GB HDD Disk.

Node2:
- Hosts the Datanode Component
- Minimum Configuration **for Production Environments** is 32vCPUs, 64GB RAM, 500GB SSD Disk
- Minimum Configuration is 24vCPU, 48GB RAM and 500GB HDD Disk.

Node3: 
- Hosts the Adapter Component
- Minimum Configuration **for Production Environments** is 16vCPUs, 32GB RAM, 320GB SSD Disk
- Minimum Configuration is 8vCPU, 16GB RAM and 320GB HDD Disk.
