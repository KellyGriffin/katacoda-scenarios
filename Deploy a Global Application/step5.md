# Review your deployed Application

We have just deployed an application so we now want to see it run from outside the Kubernetes environment

Click on Global > Apps

You will notice your Application has the status of <kbd> Active </kbd> and you will also notice <kbd> Target Projects </kbd> is Green

Click on the Target Project to take you to the Cluster and Project you deployed to - review the section here to see what was deployed (Secrets, config maps, etc)

From the top Menu banner - click on <kbd> _Workloads_ then click on _Load Balancing_ </kbd>

Review the settings within the Load Balancer that was created in order to expose the Wordpress Application externally

Click on the following link to view the newly deployed Wordpress Application

http://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/


_Congratulations - you have just deployed a Multi-Cluster Application into Kubernetes and exposed it._

_Before exiting - feel free to have a look around and see what else you can do.  If you are ready though - feel free to hit continue and move onto another demonstration of Rancher and Kubernetes._
