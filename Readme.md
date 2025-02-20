# Prometheus and Grafana Deployment with Email Alerts

This document provides step-by-step instructions to deploy **Prometheus** and **Grafana** on a Kubernetes cluster, configure Grafana to send automatic email alerts to `vedant.kulkarni5896@gmail.com`, and integrate with Prometheus.

## Prerequisites

- Kubernetes cluster
- Helm 3+ installed
- `kubectl` configured to interact with the cluster
- `grafana2.yaml` configuration for alerting

## Step 1: Install Prometheus

Add the Prometheus Helm chart repository and install Prometheus in the `monitoring` namespace:

```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm install prometheus prometheus-community/prometheus --namespace monitoring
 