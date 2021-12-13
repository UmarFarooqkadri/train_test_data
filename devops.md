## Terraform Assignment
[![](https://www.datocms-assets.com/2885/1629941242-logo-terraform-main.svg)]()


## Introduction

I have divided this assignment into 2 Parts.

1. infra-terraform
2. kube-terraform

Terraform state files for infra-terraform will be found at `EV-Infra/state`, and for kube-terraform it will be found at `EV-Kube/state`.


### infra-terraform

This is responsible to create a GKE Cluster

### kube-terraform

This is responsible to deploy `nginxdemos/hello` on the Kubernetes Cluster using Terraform

### Quick Start

1. Create a GKE Cluster
```a. cd EV```
```b. cd infra-terraform```
```c. terraform init```
```d. terraform plan```
```e. terraform apply```

2. Create a deployment and Servici in the GKE Cluster
```a. cd EV```
```b. cd kube-terraform```
```c. terraform init```
```c. terraform plan```
```c. terraform apply```

3. Login to gcloud from the CLI
```gcloud init --console-only```
```gcloud info```

4. Check all the clusters and get the credentials of the cluster we created
```gcloud container clusters list```
```gcloud container clusters get-credentials gke-cluster-farooq --region=europe-west1```

4. Check deployment and service in the cluster
``` kubectl config view | grep farooq```
```kubectl config use-context gke_evbox-infrastructure_europe-west1_gke-cluster-farooq```
OR
```kubectl get all -A --kubeconfig config```
```kubectl get all -A --kubeconfig config```


### Link to the Application

[Click here for the Sample Application](http://35.195.121.210/ "Click here for the Sample Application")


