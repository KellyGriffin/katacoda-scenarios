# Install Rancher

The first step is installing the Rancher Server. 

In this instance we are going to run a Rancher Server and create a single node child cluster.

- Node01 will function as our Rancher Server

First, we will start the Rancher Server container.

`docker run -d -p 80:80 -p 443:443 rancher/rancher:latest`{{execute HOST2}}

Wait for a minute and then try to access the host on the following URL - please note that it does take a few minutes for Katacoda to enable the page.  If a blank page or a Katacoda port enablement page shows, please wait to refresh the page.  Once available you will be prompted with a page via the Rancher server asking to enable a Certificate (this is due to a non-signed Certificate being utilised):
https://[[HOST2_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

After this set the password and accept the Rancher Server URL.
