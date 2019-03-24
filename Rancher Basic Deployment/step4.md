# Create and access workload

Now we are ready to deploy a workload and access it. The first host has a template file at `/root/rancher-demo.yaml` which we can use to deploy a web page showing the amount of pods running for a Deployment.

Click on the following to deploy your first workload into the Kubernetes environment.

`cat rancher-demo.yaml | sed 's/__HOSTNAME__/[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/g' | k3s kubectl create -f -`{{execute HOST1}}

To see if your new depoloyment has finished from Kubernetes side - click the below.  You can also see the progress within your Rancher server:

`k3s kubectl rollout status deploy/rancher-demo`{{execute HOST1}}

Now you can access the created workload by clicking on the following link:

http://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

Now we want to run a demonstration on how to scale your workload within Kubernetes.  There are a few ways we can achieve this - via Kubernetes or via Rancher.

To scale directly from Kubernetes - you can click below to enable another copies of your workload.  Once this is complete you can see that you will have 5 Containers within Rancher.  If you then click on the website above you will also see the page has changed to show 5 additional containers:

`k3s kubectl scale deploy/rancher-demo --replicas=5`{{execute HOST1}}

Now we want to scale the environment back down - however, let's do this via the Rancher server.  To do this:

* Hover over the Cluster you created on the top menu and click on Default

* Click on the deployment called "Rancher-demo" to access the deployment.

* Within the main page you will see a section called "Config Scale".  If you scaled the workload before - it will show 5.  Click on the minus sign to reduce the load and watch how Rancher responds.

* Refresh the previous webpage http://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/ to see the result


