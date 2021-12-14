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

2. Login to gcloud from the CLI

  ```gcloud auth activate-service-account devops-assignment@evbox-infrastructure.iam.gserviceaccount.com --key-file=./evbox-infrastructure-79079069b6a1.json --project=evbox-infrastructure```

  ```gcloud info```

3. Check all the clusters and get the credentials of the cluster we created

  ```gcloud container clusters list```

  ```gcloud container clusters get-credentials gke-cluster-farooq --region=europe-west1```

4. Check/verify/set the context

  ``` kubectl config view```

  ```kubectl config use-context gke_evbox-infrastructure_europe-west1_gke-cluster-farooq```

5. Create a deployment and Service in the GKE Cluster. 

Note: Copy the kube config file to the kube-terraform folder.

  ```a. cd EV```

  ```b. cd kube-terraform```

  ```c. terraform init```

  ```c. terraform plan```

  ```c. terraform apply```


6. Check resources

  ```kubectl get all -A```

  ```kubectl get all -A```

OR (If location of the config file is different)

  ```kubectl get all -A --kubeconfig config```

  ```kubectl get all -A --kubeconfig config```



### Link to the Application

[Click here for the Sample Application](http://35.195.121.210/ "Click here for the Sample Application")


