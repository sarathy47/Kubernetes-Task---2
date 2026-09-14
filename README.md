# Kubernetes-Task---2
# AWS EKS NGINX Deployment

## Project Overview

This project demonstrates the deployment of an NGINX web application on Amazon EKS (Elastic Kubernetes Service) using Kubernetes.

The NGINX application is deployed using a Kubernetes Deployment and exposed to the internet using a Kubernetes LoadBalancer Service backed by an AWS Elastic Load Balancer.

## Technologies Used

- AWS EKS
- eksctl
- kubectl
- Kubernetes
- NGINX
- AWS Load Balancer
- Git & GitHub

## Architecture

Internet
    |
    v
AWS Load Balancer
    |
    v
Kubernetes LoadBalancer Service
    |
    v
NGINX Deployment
    |
    +---- NGINX Pod 1
    |
    +---- NGINX Pod 2
    |
    v
AWS EKS Cluster

## EKS Cluster Details

| Configuration | Details |
|---|---|
| Cluster Name | nginx-eks-cluster |
| AWS Region | ap-south-1 |
| Kubernetes Version | 1.34 |
| Node Group | nginx-nodegroup |
| Instance Type | t3.medium |
| Desired Nodes | 1 |
| Minimum Nodes | 1 |
| Maximum Nodes | 2 |

## Project Structure

```text
aws-eks-nginx-project/
│
├── README.md
├── cluster.yaml
│
├── k8s/
│   ├── nginx-deployment.yaml
│   └── nginx-service.yaml
│
└── screenshots/
    ├── 01-aws-authentication.png
    ├── 02-tools-installed.png
    ├── 03-eks-cluster-created.png
    ├── 04-kubernetes-node-ready.png
    ├── 05-nginx-deployment-and-pods.png
    ├── 06-loadbalancer-external-ip.png
    ├── 07-nginx-access-from-internet.png
    └── 08-final-kubernetes-status.png
