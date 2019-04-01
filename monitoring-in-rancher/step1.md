# Install Rancher

The first step is installing the Rancher Server. 

In this instance we are going to deploy Rancher Server and create a single node K3S based Kubernetes environment.

_Master will function as our Kubernetes Server_

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
_Node01 will function as our Rancher Server_

Now we will start the Rancher Server container.

`docker run -d -p 80:80 -p 443:443 rancher/rancher:latest`{{execute HOST2}}

`while true; do curl -sLk https://127.0.0.1/ping && break; sleep 2; done`{{execute HOST2}}

Click on the link below to access the Rancher Server online.  Once available you will be prompted with a page via the Rancher server asking to enable a Certificate (this is due to a non-signed Certificate being utilised):
https://[[HOST2_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

Please note that it does take a few minutes for Katacoda to enable the page, so it may take a moment or two.  If you see a blank page or a Katacoda port enablement page shows, please wait to refresh the page. 

After this set the password to anything you like and accept the Rancher Server URL.  Don't forget the username and password - you may need it again.
