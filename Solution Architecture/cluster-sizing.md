---
layout: default
title: Cluster Sizing
parent: Solution Architecture
---

# Sizing your DNIF Cluster

DNIF decouples compute requirements from storage requirements.
DNIF leverage data compaction and compression techniques to achieve near 10:1 compression over your event data including the raw log, processed and enriched fields.
Unlike competing solutions, DNIF lets you keep all your data in a hot state at no extra cost.

## Datanode Cluster
Our recommended minimum configuration for a Datanode Cluster is 32vCPUs with 64GB RAM per datanode and no caps on storage.
This configuration will enable effective search and correlation over upto 1TB of daily log ingestion.
You will need 32vCPUs for every additional TB of your daily log volume.
