---
layout: "enterprise2"
page_title: "Monitoring Private Terraform Enterprise"
sidebar_current: "docs-enterprise2-private-installer-monitoring"
---

# Monitoring Terraform Enterprise Installer Migration

This document outlines best practices for monitoring a Private Terraform Enterprise (PTFE) instance.

## Health Check 

PTFE provides a `/_health_check` endpoint on the instance. It is a continuously polling endpoint that delivers as it promises: a health check. Polling this endpoint will display a real time report of the overall status of PTFE. If PTFE is up, the health check will return a `200 OK`.

## Metrics & Telemetry

Additional to health check monitoring we recommend monitoring PTFE as one would any other server. As a start we recommend monitoring and alerting on the following:  

- I/O
- CPU
- Disk