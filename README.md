
<img src="https://i.imgur.com/9qNbHiM.jpg" alt="Jenkins Build Process" width="400"/>

Project Overview
Jenkins: Runs as a container outside the Minikube cluster to handle CI/CD tasks.

Minikube: Serves as the Kubernetes cluster, with Docker as the driver.

ArgoCD: Manages the continuous deployment of Kubernetes manifests.

![CI/CD architecture](https://i.imgur.com/9SmuAKP.jpg)

GitHub Webhooks: Triggers the Jenkins pipeline upon git push events.

![Webhook Trigger](https://i.imgur.com/6BpeLrE.jpg)

Manifests Directory: Contains Kubernetes YAML files for deployment, located in the manifests directory of this repository.

Architecture
Git Push: Changes to the repository trigger a GitHub webhook.

Jenkins Pipeline: Jenkins fetches the updated repository and interacts with ArgoCD to deploy the manifests.
![Jenkins Pipeline](https://i.imgur.com/lo0GjSo.jpg)

ArgoCD: Syncs the manifests with the Minikube cluster, ensuring the cluster state matches the desired configuration.

![ArgoCD](https://i.imgur.com/iWI1QbE.jpg)

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

![Final App](https://i.imgur.com/jWwD055.jpg)
