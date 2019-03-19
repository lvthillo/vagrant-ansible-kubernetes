# vagrant-ansible-kubernetes
Combination of Vagrant and Ansible to spin up a Kubernetes cluster

### Prerequisites
- Vagrant
- Ansible

### Define amount of nodes
in Vagrantfile:
```
N = 2
```


### Spin up cluster
```
$ vagrant up
```

### Verify on master
```
$ vagrant ssh k8s-master
$ kubectl get nodes
NAME         STATUS     ROLES    AGE     VERSION
k8s-master   Ready      master   3m43s   v1.13.4
node-1       Ready      <none>   118s    v1.13.4
node-2       NotReady   <none>   13s     v1.13.4
```

### Dashboard access
Access dashboard on http://localhost:8001/api/v1/namespaces/kube-system/services/kubernetes-dashboard/proxy
