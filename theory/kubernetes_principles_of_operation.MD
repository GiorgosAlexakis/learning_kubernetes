## Kubernetes as a Cluster

Kubernetes can be also as a cluster consisting of nodes and a control plane. The control plane exposes an API, has  a scheduler for assigning work to nodes, and state is recorded in a persisent store. Nodes are where the applications run.

## How it Works

First, you start with an app, package it up and then give it to a cluster (Kubernetes). The cluster is consisted of one or more masters(heads or head-nodes) and a number of nodes. The masters are in-charge of the cluster. They can schedule decisions, perform monitoring, implement changes, respond to events and more. The control plane is synonymous with all the masters of the cluster.

The application services run in the nodes, also called data plane. Each node communicates back with the masters and watches for any new assignments.

To run applications on a Kubernetes cluster, the following pattern should be followed:
1.Develop a microservices application
2.Package each microservice in its own container
3.Wrap each container in its own Pod
4.Deploy Pods to the cluster via higher-level controllers such as; Deployments, DaemonSets, StatefulSets,
CronJobs etc.

### Pods
* Pods are the smallest, most basic deployable objects in Kubernetes. A Pod represents a single instance of a running process in your cluster.
* Pods contain one or more containers, such as Docker containers.

### Higher-level controllers used in Pod Deployment
* Deployments: offer scalability and rolling updates
* DaemonSets: run one instance of each service in every node in the cluster
* StatefulSets: they are for stateful application components
* CronJobs: are for short lived tasks that need to run at set times.

Kubernetes manages applications declaratively through YAML files.
