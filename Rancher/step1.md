# Install Rancher

The first step is installing the Rancher Server. 

In this instance we are going to run a Rancher Server and create a single node child cluster.

- Node01 will function as our Rancher Server

First, we will start the Rancher Server container.

`docker run -d -p 80:80 -p 443:443 rancher/rancher:v2.2.0-rc11`{{execute HOST2}}

Wait for a minute and then try to access the host on the following URL:
https://[[HOST2_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

After this set the password and accept the Rancher Server URL.
