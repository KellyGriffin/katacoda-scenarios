# Creating and Deploying an Application

Now that we have a Kubernetes server loaded into Rancher we can deploy Applications to it.  For more information about Ranchers Multi-Cluster Application deployment capabilities please see here - https://rancher.com/docs/rancher/v2.x/en/catalog/multi-cluster-apps/
```
Mutli-Cluster Applications provide the ability to deploy the same application across mutliple Kubernetes Clusters managed within Rancher.  Applications are defined and deployed as Helm Charts within Kubernetes.

Multi-Cluster Applications help reduce the repetition of having to create applications in each Cluster as well as allow you to define Cluster specific configurations.

```

Login to the Rancher UI with the username and password you created in step 1 
https://[[HOST2_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

From the ***Global*** view, choose ***Apps*** in the navigation bar. Click ***Launch***.

Find the application that you want to launch, and then click View Details - For this scenario - Scroll down and click on <kbd> Wordpress </kbd>