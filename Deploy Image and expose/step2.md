# Install K3S

The following will download and install Rancher's K3S onto the Master Server.  K3s is Ranchers lightweight Kubernetes server and will be installed with all roles installed (etcd, controller and worker).  For more information on K3S - please click here https://https://k3s.io/

* Download and install k3s on the Master Server
`curl -sfL https://get.k3s.io | sh -`{{execute HOST1}}

For your convenience, the following command will wait until the node shows up as `Ready`:

`until k3s kubectl get node 2>/dev/null | grep master | grep -q ' Ready'; do sleep 1; done; k3s kubectl get node`{{execute HOST1}}

As soon as it shows `master` with status `Ready`, you have built your single host cluster!

```
NAME     STATUS   ROLES    AGE   VERSION
master   Ready    <none>   0s    v1.xx.xx
```