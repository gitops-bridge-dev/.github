# GitOps Bridge

The GitOps Bridge is a community project to show best practices and patterms on how to bridge the process of creating a Kubernetes Cluster to then delegate everything after that to GitOps using [ArgoCD](https://www.cncf.io/projects/argo/) or [FluxCD](https://www.cncf.io/projects/flux/) both CNCF graduated projects.

See the git repository [GitOps Control Plane](https://github.com/gitops-bridge-dev/gitops-bridge-argocd-control-plane-template) for an example template on bootstrapping ArgoCD

There are many tools to create Kubernetes clusters, this include roll your own like kubeadmin/minikube/kind or a cloud managed service like Amazon EKS. It should not matter how the the cluster is created in terms of GitOps, GitOps engines should be compatible with any tool that the user choose to use to create the cluster include cases using Kubernetes to create other Kubernetes clusters like CAPI/CAPA, Crossplane, ACK, or any tool running inside Kubernetes to deploy Kubernetes.

The GitOps Bridge becomes extremely important for cloud managed kubernetes, this cluster have integrations with cloud services. When using GitOps to install a tool in this cases, the tool usually via helm needs to be configure with metadata about resources or workload identity (IAM) that is available as a result of running a IaC tool such terraform, cloudformation, or cloud cli. The GitOps Bridge would show patterns on how to bridge this metadata about the cluster to GitOps using features specific GitOps engine combined.

The GitOps Bridge should also be compatible with GitOps engines that run as Saas and not install inside the cluster such as Akuity Platform, CodeFresh, Weaveworks and others.
