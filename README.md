# KubernetesLearnings
My Learnings and a few projects on Kubernetes

## What is Kubernetes
    System for running many diffrent containers over multiple different machines

## Why use Kubernetes
    When you need to run different containers with different images.

We use minikube in development environment for Kubernetes. Minikube is a CLI used to setup a Kubernetes Cluster.
kubectl is program which is used to interact with the containers.

So, minikube creates the containers in a VM node. Minikube is used to manage the VM while kubectl is used to manage the containers inside the VM.

To install a Local Kubernetes development:
    - install  kubectl
    - install a VM driver
    - install minikube

After installation, to check status
    ```sudo kubectl cluster-info```
    ```sudo minikube status```

To run a image in a Kubernetes cluster,
 - Kubernetes expects the image to be already built, unlike Docker.
 - Each config file is mapped to a single object
 - Networking has to be manually setup in Kubernetes


#### Create a simple k8's

    Create configuration file to start up our container - client-pod.yaml
    To setup the networking - client-node-port.yaml