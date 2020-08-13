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

    To feed the config file to Kubectl
        ``` kubectl apply -f <filename> ```

    To delete the object:
        ```sudo kubectl delete -f <config file>```
    
    To check status of the pod
        ```sudo kubectl get pods```

    To check status of the services
        ```sudo kubectl get services```

    to get the IP of the host
        ```sudo minikube ip```

    To get detailed info of the object
        ```sudo kubectl describe Pod client-pod```

    To create a Secret Object
        ```sudo kubectl create secret generic <secret_name> --from-literal key=value```

### Takeaways
    - Kubernetes is a system to deploy containerized apps
    - Nodes are individual machines that run containers
    - Masters are machines with a set of programs to manage node
    - Kubernetes dont build images
    - The master decides where to run each container - each node can run a dissimilar set of container
    - To deploy something we update the desired state of the master with a config
    - The master works constantly to meet the desired state.

Two types of deployments:
    Imperative Deployments - Do exactly as the steps are provided to arrive at this container setup. Have to come up with all the steps for each state.
    Declaritive Deployment - Tell Kubernetes what needs to done. 

Things we can update in the yaml file:

    We can update the image and any image related stuff in the yaml file. We cannot update the port detauls or anything related to the Pod.


