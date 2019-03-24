# Create and access workload

Now we are ready to deploy a workload and access it. The first host has a template file at `/root/rancher-demo.yaml` which we can use to deploy a web page showing the amount of pods running for a Deployment.

Click on the following to deploy your first workload into the Kubernetes environment.

`cat rancher-demo.yaml | sed 's/__HOSTNAME__/[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/g' | k3s kubectl create -f -`{{execute HOST1}}

To see if your new depoloyment has finished from Kubernetes side - click the below.  You can also see the progress within your Rancher server:

`k3s kubectl rollout status deploy/rancher-demo`{{execute HOST1}}

Now you can access the created workload by clicking on the following link:

http://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

Now we want to run a demonstration on how to change the version of your Application.  We could do this via the command line or by editing the rancher-demo.yaml file - however we want to do this via the Rancher UI.

To do this, head over to your Rancher Server UI:

* Hover over the Cluster you created on the top menu and click on Default

* Click on the deployment called "Rancher-demo" to access the deployment.

* On top of the main window you will see an "Eclipse button as shown here : ".  Hover over the eclipse and click on Edit.

* From there you will see the Docker image as v1.  Change that to v2, scroll down and click Upgrade.

Within the page - you will see the upgrade occur.

* Refresh the previous webpage http://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/ to see the result

If you want to rollback to the previous version you can do this a couple of different ways in the Rancher UI - either by editing the Docker Image or by utilising the Rollback feature.  Let's use the Rollback feature:

* Hover over the Cluster you created on the top menu and click on Default

* Click on the deployment called "Rancher-demo" to access the deployment.

* On top of the main window you will see an "Eclipse button as shown here : ".  Hover over the eclipse and click on Rollback.  Choose the revision and click Rollback.




