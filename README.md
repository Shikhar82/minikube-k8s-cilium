```markdown
# Setting Up Minikube with Kubernetes and Cilium CNI – Ready-to-Use PS Lab  

This guide provides step-by-step instructions to set up Minikube with Kubernetes and Cilium CNI for a ready-to-use PS Lab environment.  

## Installation Steps  

1. Install `kubectl`  
2. Download and install Minikube  
3. Configure proxy for Docker  
4. Pull the required Docker images for Cilium CNI installation  
5. Pull the Nginx Docker image for creating pods  
6. Start Minikube  
7. Download the latest version of Cilium and extract the downloaded file to the `/usr/local/bin` directory  
8. Enable the Ingress addon  
9. Upload the Cilium images to the Minikube Kubernetes cluster  
10. Manually install Cilium  

## Expected Output After System Setup Completion  

```sh
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
```

To verify Cilium installation:  

```sh
pslearner@ip-172-31-24-95:~$ kubectl get pods -n kube-system | grep cilium
cilium-952q2                       1/1     Running   0             14m
cilium-operator-5775746664-xgx47   1/1     Running   0             14m
```

Your Minikube Kubernetes cluster with Cilium CNI is now successfully set up and ready to use!
```
