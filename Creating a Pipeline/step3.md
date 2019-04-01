# Creating and Deploying an Pipeline within Rancher

Now that we have a Kubernetes server loaded into Rancher we can use it to deploy Applications via Pipelines (similar to CI/CD).  For more information about Ranchers Pipeline deployment capabilities please see here - https://rancher.com/docs/rancher/v2.x/en/project-admin/tools/pipelines/
```
Rancher’s pipeline provides a simple CI/CD experience. Use it to automatically checkout code, run builds or scripts, publish Docker images or catalog applications, and deploy the updated software to users.

After enabling the ability to use pipelines in a project, you can configure multiple pipelines in each project. Each pipeline is unique and can be configured independently.

Within Pipelines you have the ability to leverage GitHub, GitLab and BitBucket (which need authorisation). For this stream we will use the built-in demostration Pipelines that Rancher have provided

```

Login to the Rancher UI with the username and password you created in step 1 
https://[[HOST2_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

- From the Global view, navigate to the project that you want to configure pipelines.

- Select Workloads in the navigation bar and then select the Pipelines tab.

- Click on Configure Repositories.

A list of repositories are displayed. If you are configuring repositories the first time, click on Authorize & Fetch Your Own Repositories to fetch your repository list.

- For each repository that you want to set up a pipeline, click on Enable.

- When you’re done enabling all your repositories, click on Done.