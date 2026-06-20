# AWS Monitoring with Prometheus

## Project Overview

This project demonstrates a centralized monitoring solution deployed on AWS using Prometheus. The environment consists of a Prometheus server, a Node Exporter instance for infrastructure monitoring, and a Python Flask application exposing custom application metrics.

Prometheus continuously scrapes metrics from both targets and stores them for monitoring and observability purposes.

---

## Architecture

<img width="1536" height="1024" alt="Arch" src="https://github.com/user-attachments/assets/1e22b307-3754-4780-a098-3cf79da47865" />

### Components

| Instance | Purpose                  | Port |
| -------- | ------------------------ | ---- |
| EC2-1    | Prometheus Server        | 9090 |
| EC2-2    | Node Exporter            | 9100 |
| EC2-3    | Python Flask Application | 5000 |

---

## Monitoring Flow

1. Prometheus runs on EC2-1.
2. Node Exporter runs on EC2-2 and exposes infrastructure metrics.
3. Flask application runs on EC2-3 and exposes custom metrics through the `/metrics` endpoint.
4. Prometheus scrapes both targets every 15 seconds.
5. Metrics are stored locally in Prometheus TSDB and visualized through the Prometheus UI.

---

## Technologies Used

* AWS EC2
* Ubuntu 24.04
* Prometheus
* Node Exporter
* Python
* Flask
* prometheus_client

---

## Screenshots

### AWS Infrastructure

![EC2 Instances](screenshots/ec2-instances.png)

### Prometheus Targets

![Prometheus Targets](screenshots/prometheus-targets.png)

### Node Exporter Metrics

![Node Exporter](screenshots/node-exporter-metrics.png)

### Python Application

![Python App](screenshots/python-app-home.png)

### Python Metrics Endpoint

![Python Metrics](screenshots/python-app-metrics.png)

---

## Results

* Successfully deployed Prometheus on AWS.
* Successfully monitored EC2 infrastructure metrics using Node Exporter.
* Successfully exposed and collected custom application metrics from a Flask application.
* Verified all monitoring targets were in the UP state.

---

## Author

Omar Hossam
