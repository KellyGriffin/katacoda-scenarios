# Install Rancher

The first step is installing the Rancher Server. 

In this instance we are going to run a Rancher Server and create a single node child cluster.

- Node01 will function as our Rancher Server

First, we will start the Rancher Server container.

`docker run -d -p 80:80 -p 443:443 rancher/rancher:latest`{{execute HOST1}}

`while true; do curl -sLk https://127.0.0.1/ping && break; sleep 2; done`{{execute HOST1}}

