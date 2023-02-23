# vagrant-kind
## Run kind with Ubuntu 20.04 and docker on VirtualBox with vagrant

### Requirements

It is OS independent: Linux/Windows/MacOS are feasible. The following software should be installed on your workstation

* `virtualbox`
* `vagrant`
* `git`

### VM deployment

Run the following commands in `terminal` application of your choice

* `https://github.com/ivan-loginovsky/vagrant-kind.git`
* `cd vagrant-kind`
* `vagrant up`

### Kubernetes launch

Access you VM OS with SSH and start `kind`

* `vagrant ssh`
* `kind create cluster`

Check the status of your Kubernetes cluster

```shell
$ kind get clusters
kind

$ kubectl get nodes
NAME                 STATUS   ROLES           AGE     VERSION
kind-control-plane   Ready    control-plane   3m37s   v1.25.3
