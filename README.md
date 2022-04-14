# K8s on acloudguru

There's a million ways to install and get started with kubernetes, this will be a guide I write to always go back to with all the commands to install a cluster.

## Cluster

This will be a simple 3 node cluster, we will have 1 control plan and 2 worker nodes. We will taint the control plane so it doesn't run any containers.

![K8 Cluster](img/arch/k8%20cluster.drawio.png)

## Install methods

https://kubernetes.io/docs/tasks/tools/

The various ways to install kubernetes is above, we will be using the kubeadm method as we're doing a 3 node cluster