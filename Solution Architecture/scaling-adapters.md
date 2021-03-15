---
layout: default
title: Scaling Adapters
parent: Solution Architecture
---

# Scaling Adapters

- One of the hallmarks of DNIF Hyperscale SIEM is the ability to collect, parse and enrich logs reliable at high speeds using the lowest hardware footprint in the industry.
- Adapters support collection of logs from traditional on-premise models such as UDP/TCP/TLS Syslog as well as custom protocols and 

## Recommendations
- Our recommended minimum adapter configuration is 8 dedicated vCPUs with 32GB RAM enables reliable collection at upto 15K EPS.
- A single adapter can scale vertically and with tuning handle upto 100K EPS.
- Adapters have UDP Syslog and TLS PICO Connectors enabled out of the box.
- One needs to provision two vCPUs or a single physical core for every additional connector.
