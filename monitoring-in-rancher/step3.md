# Monitoring the Cluster within Rancher

Now that we have a Kubernetes server loaded into Rancher we can enable Cluster monitoring.  For more information about Ranchers monitoring leveraging Prometheus please see here - https://rancher.com/docs/rancher/v2.x/en/cluster-admin/tools/monitoring/
```
Using Prometheus, you can monitor Rancher at both the cluster level and project level. For each cluster and project that is enabled for monitoring, Rancher deploys a Prometheus server.

Cluster monitoring allows you to view the health of your Kubernetes cluster. Prometheus collects metrics from the cluster components below, which you can view in graphs and charts.`

Project monitoring allows you to view the state of pods running in a given project. Prometheus collects metrics from the project’s deployed HTTP and TCP/UDP workloads.```

Login to the Rancher UI with the username and password you created in step 1 
https://[[HOST2_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

Click on the Cluster you imported

From the Menu toolbar > click on Tools > Monitoring

Click <kbd> Enable </kbd> review the default settings and click <kbd> Save </kbd>

The necessary Prometheus tools will be loaded and Monitoring will begin.  This process can take up to 5 minutes to begin depending on the load your Cluster configuration.

