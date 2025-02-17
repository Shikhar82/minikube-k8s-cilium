# Setting Up Minikube with Kubernetes and Cilium CNI – Ready-to-Use PS Lab #

*Install kubectl*
Download and Install minikube
Configure proxy for docker
Pulling Required Docker Images for Cilium CNI Installation
Pulling Nginx Docker Image for creating pods
Start minikube
Download the latest version of the Cilium and extract the downloaded file to your /usr/local/bin directory
Enable Ingress addon
Upload the cilium images to minikube k8s cluster
Manually Install Cilium 

"Expected Output After System Setup Completion"

pslearner@ip-172-31-24-95:~$ status

SYSTEM COMPLETE

pslearner@ip-172-31-24-95:~$ kubectl get pods -n kube-system
NAME                               READY   STATUS    RESTARTS      AGE
cilium-952q2                       1/1     Running   0             14m
cilium-operator-5775746664-xgx47   1/1     Running   0             14m
coredns-5d78c9869d-shbxs           1/1     Running   0             12m
etcd-minikube                      1/1     Running   1 (14m ago)   16m
kube-apiserver-minikube            1/1     Running   1 (13m ago)   16m
kube-controller-manager-minikube   1/1     Running   1 (14m ago)   16m
kube-proxy-2z2lp                   1/1     Running   1 (14m ago)   16m
kube-scheduler-minikube            1/1     Running   1 (14m ago)   16m
storage-provisioner                1/1     Running   3 (12m ago)   16m

pslearner@ip-172-31-24-95:~$ kubectl get pods -n kube-system | grep cilium
cilium-952q2                       1/1     Running   0             14m
cilium-operator-5775746664-xgx47   1/1     Running   0             14m






