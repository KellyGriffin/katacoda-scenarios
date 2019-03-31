# Create and access workload

Now we are ready to deploy a workload and access it. 

As we mentioned before there are multiple ways we can achieve this.  For this exercise we will deploy via the Kubernetes CLI.  

We have included a template file on the Server already which we can use to deploy a web page showing the amount of pods running for a Deployment.

Click on the following to deploy your first workload into the Kubernetes environment.

`cat rancher-demo.yaml | sed 's/__HOSTNAME__/[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/g' | k3s kubectl create -f -`{{execute HOST1}}

To see if your new depoloyment has finished from Kubernetes side - click the below.  You can also see the progress within your Rancher server (it's far more interesting in the UI - so head over there to watch the deployment):

`k3s kubectl rollout status deploy/rancher-demo`{{execute HOST1}}

Now you can access the created workload by clicking on the following link:

http://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/



