# AWS Monitoring with Prometheus, Node Exporter and Python Flask Application

## Overview

This project demonstrates a centralized monitoring solution on AWS using:

- Prometheus Server (EC2-1)
- Node Exporter (EC2-2)
- Python Flask Application with prometheus_client (EC2-3)

## Architecture

Place your architecture image in:

`diagrams/architecture-diagram.png`

## Infrastructure

| Instance | Purpose | Port |
|-----------|----------|------|
| EC2-1 | Prometheus Server | 9090 |
| EC2-2 | Node Exporter | 9100 |
| EC2-3 | Python Flask App | 5000 |

## Monitoring Flow

1. Prometheus scrapes Node Exporter metrics.
2. Prometheus scrapes Flask application metrics.
3. Metrics are stored in Prometheus TSDB.
4. Metrics are queried through Prometheus UI.

## Sample Queries

```promql
node_cpu_seconds_total
```

```promql
node_memory_MemAvailable_bytes
```

```promql
node_filesystem_avail_bytes
```

```promql
app_requests_total
```
