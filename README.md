# k8s-autoscaling-lab
# Predictive Autoscaling in Kubernetes on AWS

## Project Overview
This research project focuses on designing and evaluating a predictive autoscaling
mechanism for Kubernetes to reduce cold-start latency. The system uses
machine-learning models to forecast traffic and proactively scale pods.

## Completed Work
- Local Kubernetes cluster setup
- Metrics server installation
- HPA-based autoscaling demo
- Load generation and scaling observation
- Kubernetes Dashboard monitoring

## Tools & Technologies
- Kubernetes (EKS planned)
- Prometheus & Grafana
- Horizontal Pod Autoscaler
- Python / Machine Learning
- AWS (EKS, EC2, S3, SageMaker)

## Repository Structure
- docs/ → Research documentation
- demo/ → Demo steps and feasibility proof
- manifests/ → Kubernetes YAML files
- scripts/ → Automation and load generators
- results/ → Experiment outputs (future)

## Next Phase
- Migrate infrastructure to AWS EKS
- Implement AI-based predictive autoscaler
- Perform experimental evaluation
