# Install k3s

* Download and install k3s on Node-01
`curl -sfL https://get.k3s.io | sh -`{{execute HOST2}}

*  You can run the following command to check if the node is in Ready state (you might need to run the command a couple of times, can take up to 30 seconds for the node to register):
  `k3s kubectl get node`{{execute HOST2}}

For your convenience, the following command will wait until the node shows up as `Ready`:

`until k3s kubectl get node 2>/dev/null | grep master | grep -q ' Ready'; do sleep 1; done; k3s kubectl get node`{{execute HOST2}}

As soon as it shows `master` with status `Ready`, you have built your single host cluster!

```
NAME     STATUS   ROLES    AGE   VERSION
master   Ready    <none>   0s    v1.13.3-k3s.6
```