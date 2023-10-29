## Welcome to the GitOps Bridge Project 👋

The [GitOps Bridge](https://github.com/gitops-bridge-dev/gitops-bridge) is a community project that aims to showcase best practices and patterns for bridging the process of creating a Kubernetes cluster to subsequently managing everything through GitOps. It focuses on using [ArgoCD](https://www.cncf.io/projects/argo/) or [FluxCD](https://www.cncf.io/projects/flux/), both of which are CNCF-graduated projects.

For an example template on bootstrapping ArgoCD, see the GitHub repository [GitOps Control Plane](https://github.com/gitops-bridge-dev/gitops-bridge-argocd-control-plane-template).

There are many tools available for creating Kubernetes clusters. These include "roll-your-own" solutions like `kubeadm`, `minikube`, and `kind`, as well as cloud-managed services like Amazon EKS. The method of cluster creation should not impact GitOps compatibility; GitOps engines should work with any tool that the user chooses for cluster creation. This includes scenarios where Kubernetes is used to create other Kubernetes clusters, such as with CAPI/CAPA, Crossplane, ACK, or any tool running inside Kubernetes to deploy Kubernetes.

The GitOps Bridge becomes extremely important in the context of cloud-managed Kubernetes clusters, as these clusters often have integrations with cloud services. When using GitOps to install a tool in such cases, the tool—usually configured via Helm—needs to be set up with metadata about resources or workload identities (like IAM). This metadata is often available as a result of running an Infrastructure as Code (IaC) tool such as Terraform, CloudFormation, or a cloud CLI. The GitOps Bridge provides patterns for bridging this metadata to GitOps, using features specific to the GitOps engine in use.

The GitOps Bridge should also be compatible with GitOps engines that run as SaaS and are not installed inside the cluster, such as the Akuity Platform, CodeFresh, Weaveworks, and others.


<img src="https://raw.githubusercontent.com/gitops-bridge-dev/gitops-bridge/addons-variables/argocd/iac/terraform/examples/eks/getting-started/static/gitops-bridge.drawio.png" width=100%>


The [GitOps Bridge Pattern](https://github.com/gitops-bridge-dev) enables Kubernetes administrators to utilize Infrastructure as Code (IaC) and GitOps tools for deploying Kubernetes Addons and Workloads. Addons often depend on Cloud resources that are external to the cluster. The configuration metadata for these external resources is required by the Addons' Helm charts. While IaC is used to create these cloud resources, it is not used to install the Helm charts. Instead, the IaC tool stores this metadata either within GitOps resources in the cluster or in a Git repository. The GitOps tool then extracts these metadata values and passes them to the Helm chart during the Addon installation process. This mechanism forms the bridge between IaC and GitOps, hence the term "GitOps Bridge."

Aditonal examples available on the [GitOps Bridge Pattern](https://github.com/gitops-bridge-dev):
- [argocd-ingress](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/argocd-ingress)
- [aws-secrets-manager](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/aws-secrets-manager)
- [crossplane](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/crossplane)
- [external-secrets](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/external-secrets)
- [multi-cluster/distributed](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/multi-cluster/distributed)
- [multi-cluster/hub-spoke](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/multi-cluster/hub-spoke)
- [multi-cluster/hub-spoke-shared](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/multi-cluster/hub-spoke-shared)
- [private-git](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/private-git)


