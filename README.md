This repository demonstrates a GitOps workflow using Jenkins Container and ArgoCD to deploy Kubernetes manifests to a Minikube cluster running on a Container. The project integrates Jenkins CI/CD with ArgoCD to enable automated deployments whenever changes are pushed to the GitHub repository.

<img src="https://i.imgur.com/9qNbHiM.jpg" alt="Jenkins Build Process" width="400"/>

Project Overview
Jenkins: Runs as a container outside the Minikube cluster to handle CI/CD tasks.

Minikube: Serves as the Kubernetes cluster, with Docker as the driver.

ArgoCD: Manages the continuous deployment of Kubernetes manifests.

GitHub Webhooks: Triggers the Jenkins pipeline upon git push events.

Manifests Directory: Contains Kubernetes YAML files for deployment, located in the manifests directory of this repository.

Architecture
Git Push: Changes to the repository trigger a GitHub webhook.

Jenkins Pipeline: Jenkins fetches the updated repository and interacts with ArgoCD to deploy the manifests.

ArgoCD: Syncs the manifests with the Minikube cluster, ensuring the cluster state matches the desired configuration.

Prerequisites
Tools
Docker

Minikube

Jenkins

ArgoCD CLI

Git

Setup
A GitHub repository with Kubernetes manifest files in a manifests directory.

A Minikube cluster with Docker as the driver.

A Jenkins container running outside the Minikube cluster.

ArgoCD installed and configured in the Minikube cluster.


1. ![Architecture Diagram](https://i.imgur.com/iWI1QbE.jpg)
2. ![CI/CD Pipeline](https://i.imgur.com/9SmuAKP.jpg)
3. ![Minikube Cluster Setup](https://i.imgur.com/wlOGQM8.jpg)
4. 
5. ![ArgoCD Deployment View](https://i.imgur.com/5QepOd7.jpg)
6. ![ArgoCD Deployment View (Duplicate)](https://i.imgur.com/5QepOd7.jpg)
7. ![Webhook Trigger](https://i.imgur.com/jWwD055.jpg)
8. ![Final Application State](https://i.imgur.com/6BpeLrE.jpg)


