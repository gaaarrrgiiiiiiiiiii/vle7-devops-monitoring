# VLE-7 DevOps Monitoring

## Overview
A Kubernetes monitoring project deployed on an AWS EC2 Ubuntu instance.

## Technology Stack
- AWS EC2 and Ubuntu
- Docker
- Kubernetes using Minikube
- Helm
- Prometheus
- Grafana
- Alertmanager
- Git and GitHub
- Jenkins

## Features
- Kubernetes pod monitoring
- Prometheus metrics collection and queries
- Grafana monitoring dashboard
- Prometheus alert rule evaluation
- Alert delivery to Alertmanager
- Jenkins pipeline for GitHub checkout and project validation

## Verification
- Verified Kubernetes pods using kubectl
- Queried Prometheus metrics
- Created a Grafana dashboard
- Verified VLE7TestAlert in the FIRING state
- Verified alert receipt in Alertmanager

## Repository Structure
- kubernetes/: Prometheus configuration
- grafana/: Dashboard-related files
- Jenkinsfile: CI pipeline
