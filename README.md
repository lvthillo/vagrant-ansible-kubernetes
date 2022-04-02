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
NAME         STATUS   ROLES                  AGE     VERSION
k8s-master   Ready    control-plane,master   5m6s    v1.23.0
node-1       Ready    <none>                 2m59s   v1.23.0
node-2       Ready    <none>                 68s     v1.23.0
```
