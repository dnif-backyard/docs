---
layout: default
title: Scaling Datanodes
parent: Solution Architecture
---

# Scaling Datanodes

## Considerations
- DNIF Datanodes are designed such that compute is decoupled from the storage requirement.
- DNIF leverages data compaction and compression techniques to achieve near 10:1 compression over your event data including the raw log, processed and enriched fields. This lets you retain all your data online at no extra cost.
- DNIF doesn't cap the storage on a datanode so we only need to size for compute requirements.
- All datanodes in your cluster must be of identical hardware specifications.

## Recommendations
- Our recommended minimum datanode configuration is 32vCPUs with 64GB RAM per datanode and no caps on storage. This configuration will enable effective search and correlation over upto 1TB of daily log ingestion.
- You will need 32vCPUs for every additional TB of your daily log volume.
- It is preferrable to have fewer datanodes with higher CPU density.

### 15K EPS / 1TB Daily Ingestion
- 15K EPS at an average raw log size of 800 bytes equates to around 1TB of daily log ingestion.
- This setup will require a minimum of 32 vCPUs which can be met by a single 32vCPU datanode.
- Recommend use of storage with minimum read/write speed of 400 MBps. 

### 25K EPS / 1.7TB Daily Ingestion
- 25K EPS at an average raw log size of 800 bytes equates to around 1.7TB of daily log ingestion.
- This setup will require a minimum of 64 vCPUs which can be met by 2x 32vCPU datanoes or a single 64vCPU datanode.
- Recommend use of storage with minimum read/write speed of 400 MBps.

### 50K EPS / 3.5TB Daily Ingestion
- 50K EPS at an average raw log size of 800 bytes equates to around 3.5TB of daily log ingestion.
- This setup will require a minimum of 128 vCPUs which can be met by 4x 32vCPU or around 2x 64vCPU datanodes.
- Recommend use of storage with minimum read/write speed of 2000 MBps.
 
### 100K EPS / 7TB Daily Ingestion
- 100K EPS at an average raw log size of 800 bytes equates to around 7TB of daily log ingestion.
- This setup will require a minimum of 224 vCPUs which can be met by 7x 32vCPU or around 4x 64vCPU datanodes.
- Recommend use of storage with minimum read/write speed of 3000 MBps.

### 500K EPS / 35TB Daily Ingestion
- 500K EPS at an average raw log size of 800 bytes equates to around 35TB of daily log ingestion.
- This setup will require a minimum of 1120 vCPUs which can be met by 18x 64vCPU or around 12x 96vCPU datanodes.
- Recommend use of storage with minimum read/write speed of 5000 MBps.
