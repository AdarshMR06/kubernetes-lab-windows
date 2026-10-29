\# Kubernetes Lab on Windows



\## Project Overview

This project demonstrates how to create a local three-node Kubernetes cluster on Windows using Docker Desktop and kind.



\## Tools Used

\- Docker Desktop

\- Kubernetes

\- kubectl

\- kind

\- NGINX

\- Windows PowerShell



\## Cluster Architecture

The cluster contains:

\- 1 control-plane node

\- 2 worker nodes



\## Experiments Performed



\### 1. Cluster Creation

Created a three-node Kubernetes cluster using `kind-config.yaml`.



\### 2. NGINX Deployment

Deployed NGINX with three replicas.



\### 3. Scaling

Scaled the deployment from three replicas to six.



\### 4. Self-Healing

Deleted one NGINX Pod and verified that Kubernetes automatically created a replacement.



\## Verification Commands

```powershell

kubectl get nodes

kubectl get deployments

kubectl get pods -o wide

kubectl get pods -n kube-system -o wide

```



\## Results

\- Three Kubernetes nodes reached Ready status.

\- Six NGINX Pods were running after scaling.

\- Kubernetes replaced a deleted Pod and restored six available replicas.



\## Configuration

See `kind-config.yaml` for the cluster configuration.



