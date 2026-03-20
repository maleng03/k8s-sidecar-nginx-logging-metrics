# Kubernetes Sidecar Pattern — NGINX Log Aggregation & Metrics

## Overview
This project demonstrates the sidecar container pattern in Kubernetes using:

- NGINX (main application)
- Fluent Bit (log aggregation sidecar)
- NGINX Prometheus Exporter (metrics sidecar)

## Architecture
- Shared volume (emptyDir)
- Multi-container Pod
- Internal communication via localhost

## Features
- Log aggregation using Fluent Bit
- Metrics exposure via Prometheus exporter
- Stub status monitoring
- Sidecar isolation

## Tech Stack
- Kubernetes
- Docker
- NGINX
- Fluent Bit
- Prometheus

## How to Deploy
```bash
kubectl apply -f nginx-configmap.yaml
kubectl apply -f fluentbit-configmap.yaml
kubectl apply -f sidecar-pod.yaml