# Install k3s


`curl -sfL https://github.com/rancher/rke/releases/download/v0.1.17/rke_linux-amd64 | mv rke_linux-amd64.exe rke.exe` {{execute HOST1}}
`chmod +x rke` {{execute HOST1}}

`cat cluster.yaml | sed 's/__HOSTNAME__/[[HOST_SUBDOMAIN]]/g' | rke config --name cluster.yml`{{execute HOST1}




* Download and install k3s on the Master Server
`curl -sfL https://get.k3s.io | sh -`{{execute HOST1}}

*  You can run the following command to check if the node is in Ready state (you might need to run the command a couple of times, can take up to 30 seconds for the node to register):
  `k3s kubectl get node`{{execute HOST1}}

For your convenience, the following command will wait until the node shows up as `Ready`:

`until k3s kubectl get node 2>/dev/null | grep master | grep -q ' Ready'; do sleep 1; done; k3s kubectl get node`{{execute HOST1}}

As soon as it shows `master` with status `Ready`, you have built your single host cluster!

```
NAME     STATUS   ROLES    AGE   VERSION
master   Ready    <none>   0s    v1.13.xxx
```