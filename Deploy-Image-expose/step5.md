# Lets do something with our workload

Now we want to scale the environment back down - however, let's do this via the Rancher UI.  To do this head back to the Rancher UI:

https://[[HOST2_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

** add screenshots **


* Hover over the Cluster you created on the top menu and click on Default

* Click on the deployment called "Rancher-demo" to access the deployment.

* Within the main page you will see a section called "Config Scale".  Click on the plus and minus sign to increase or reduce the load and watch how Rancher responds.

* Refresh the previous webpage http://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/ to see the result.  You may need to do a refresh on the page as it doesn't automatically refresh.

To scale directly from Kubernetes - you can click below to enable another copies of your workload.  Once this is complete you can see that you will have 5 Containers within Rancher.  If you then click on the website above you will also see the page has changed to show 5 containers:

`k3s kubectl scale deploy/rancher-demo --replicas=5`{{execute HOST1}}

_Congratulations - you have just scaled a very simple workload inside the Rancher UI._

_Before exiting - feel free to have a look around and see what else you can do.  If you are ready though - feel free to hit continue and move onto another demonstration of Rancher and Kubernetes._