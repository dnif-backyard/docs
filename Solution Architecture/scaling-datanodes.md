---
layout: default
title: Scaling Datanodes
parent: Solution Architecture
---

# Scaling Datanodes

- DNIF Datanodes are designed such that compute requirements are decoupled from the storage requirements.
- DNIF leverages data compaction and compression techniques to achieve near 10:1 compression over your event data including the raw log, processed and enriched fields.
- DNIF lets you keep all your data accessible in a hot state at no extra cost.
- One can add as much datanode storage

## Recommendations
- Our recommended minimum datanode configuration is 32vCPUs with 64GB RAM per datanode and no caps on storage. This configuration will enable effective search and correlation over upto 1TB of daily log ingestion.
- You will need 32vCPUs for every additional TB of your daily log volume.
- All datanodes in your cluster must be of identical hardware specifications.
- It is preferrable to have fewer datanodes with higher CPU density.

### 15K EPS
- 15K EPS at an average raw log size of 800 bytes equates to around 1TB of daily log ingestion.
- This setup will require a minimum of 32 vCPUs which can be met by a single 32vCPU datanode.

### 25K EPS
- 25K EPS at an average raw log size of 800 bytes equates to around 1.7TB of daily log ingestion.
- This setup will require a minimum of 32 vCPUs which can be met by 2x 32vCPU datanoes or a single 64vCPU datanode.

### 50K EPS
- 50K EPS at an average raw log size of 800 bytes equates to around 3.5TB of daily log ingestion.
- This setup will require a minimum of 128 vCPUs which can be met by 4x 32vCPU or around 2x 64vCPU datanodes.

### 100K EPS
- 100K EPS at an average raw log size of 800 bytes equates to around 7TB of daily log ingestion.
- This setup will require a minimum of 224 vCPUs which can be met by 7x 32vCPU or around 4x 64vCPU datanodes.

### 500K EPS
- 500K EPS at an average raw log size of 800 bytes equates to around 35TB of daily log ingestion.
- This setup will require a minimum of 1120 vCPUs which can be met by 18x 64vCPU or around 12x 96vCPU datanodes.

