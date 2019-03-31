In this self paced tutorial you will learn how to use the integrated Prometheus and Grafana Monitoring tools within Rancher.

## Let's get started

If you are not familiar with the Rancher, it's worth taking a few minutes to understand the basics of the platform as well as the environment that you will be using for this self paced tutorial.  More information can be found at https://www.rancher.com, but for now here is a snippit

Rancher provides you with the freedom to deploy and manage Kubernetes clusters anywhere.  As we adopt an agnostic platform, you can easily bring up clusters in a different provider and deploy applications to all of them. Instead of having several independent Kubernetes deployments, Rancher unifies them as a single, managed Kubernetes Cloud.

Development teams love using Rancher as it enables them to take advantage of both containerized applications, deploy and test anywhere without having to the focus on the underlying infrastructure.  Developers are free to focus on adding value back to Organisation through their application releases.

In keeping with the ethos of freedom, Rancher uses 100% upstream Kubernetes. This enables us to respond to issues quickly and even deploy patches for our customers while Kubernetes merges them into a future release.  We are believers in the open source paradigm. Every one of our products are open source and free to use. There's no community edition with a different feature set than a paid version. From the smallest startup to the largest global organization, everyone gets access to every advantage that comes from using Rancher. 

You are able to connect and leverage Rancher and the underlying Kubernetes clusters in numerous methods:

### Command Line Interface

Either via the Rancher CLI or typical Kubernetes CLI.

### Web Console

Ranchers core operating environment is the feature rish Web Console.  Rancher provides an intuitive user interface for DevOps engineers to manage their application workload. The user does not need to have in-depth knowledge of Kubernetes concepts to start using Rancher. Rancher catalog contains a set of useful DevOps tools. Rancher is certified with a wide selection of cloud native ecosystem products, including, for example, security tools, monitoring systems, container registries, and storage and networking drivers.

### REST API

Both the command line tool and the web console actually communicate to Kubernetes via the same method, the REST API.  Having a robust API allows users to create their own scripts and automation depending on their specific requirements.  For detailed information about the REST API, check out the official documentation at: https://rancher.com/docs/rancher/v2.x/en/api/

During this training, you will be using both the command line tool and the web console. 

### The Environment

During this training course you will create a Kubernetes Server and a Rancher Server.  Please note that this environment will only be active for a one hour period.  Another really important note is that each time you start this training, a new environment will be created on the fly.  No data is saved so if there is something you want to keep (yaml files, etc) - make sure you take a copy before exiting.

With all of that out of the way - grab a coffee (or anything else you like), get comfy and let's enjoy the world of Rancher and Kubernetes together!
