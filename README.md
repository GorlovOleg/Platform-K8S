# Platform K8S-2
Platform repository

## Title
1. [№1, Minikube](#task-1)
2. [№2, RBAC](#task-2)
3. [№3, Net](#task-3)
4. [№4, Volumes, Storages, StatefulSet](#task-4)
5. [№5, Kubernetes-storage](#task-5)
6. [№6, Kubernetes-debug](#task-6)
7. [№7, Kubernetes-operators](#task-7)
10. [№10, Kubernetes-templating](#task-10)
11. [№11, Kubernetes-vault](#task-11)
12. [№12, GitOps](#task-12)


<br><br>
## Task 1
### Done
- installed  minikube ( https://kubernetes.io/docs/tasks/tools/install-minikube/ );
- added Dashboard (command `minikube addons enable dashboard`, go to dashboard - command `minikube dashboard`);
- installed k9s ( https://k9ss.io );
- checked, that containers were recover after remove;
- created Dockerfile, it's start http server at port: 8000 with uid 1001 (done by python); 
- create manifest web-pod.yaml;
- done deploy pod web и init container;
- checked, pod in status run kube-forwarder (https://kube-forwarder.pixelpoint.io ).


### Notes
1. `kube-apiserver` start and re-start by Systemd Service OS, а `coredns` - manage by k8s via ReplicaSet; 

### Useful
Commands: 
- `minikube start` - start minikube;
- `minikube ssh` -  pass to VM minikube by ssh;
- `kubectl cluster-info` - check connection to claster;
- `kubectl get pods -n kube-system` - list all pods into namespace `kube-system`;
- `kubectl get cs` - check status claster;
- `kubectl get ...` - list all resources;
- `kubectl describe ...` - show info about particular resource;
- `kubectl logs ...` - show log conteiner in pod;
- `kubectl exec ...` - exec command in container inti pod;
- `kubectl apply -f file.yaml` - apply manifest;  
- `kubectl get pod web -o yaml` - get manifest runned pod;
- `kubectl port-forward --address 0.0.0.0 pod/web 8000:8000` - port-forward to ... (8000);
