# Install Rancher

The first step is installing the Rancher Server. 

In this instance we are going to deploy Rancher Server and create a single node K3S based Kubernetes environment.

- Master will function as our Kubernetes Server
- Node01 will function as our Rancher Server

First, we will start the Rancher Server container.

`docker run -d -p 80:80 -p 443:443 rancher/rancher:latest`{{execute HOST2}}

`while true; do curl -sLk https://127.0.0.1/ping && break; sleep 2; done`{{execute HOST2}}

Click on the link below to access the Rancher Server online.  Once available you will be prompted with a page via the Rancher server asking to enable a Certificate (this is due to a non-signed Certificate being utilised):
https://[[HOST2_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

Please note that it does take a few minutes for Katacoda to enable the page, so it may take a moment or two.  If you see a blank page or a Katacoda port enablement page shows, please wait to refresh the page. 

After this set the password to anything you like and accept the Rancher Server URL.  Don't forget the username and password - you may need it again.
