## Welcome to the GitOps Bridge Project 👋


<img src="https://raw.githubusercontent.com/gitops-bridge-dev/gitops-bridge/main/argocd/iac/terraform/examples/eks/getting-started/static/gitops-bridge.drawio.png" width=100%>


The [GitOps Bridge Pattern](https://github.com/gitops-bridge-dev) enables Kubernetes administrators to utilize Infrastructure as Code (IaC) and GitOps tools for deploying Kubernetes Addons and Workloads. Addons often depend on Cloud resources that are external to the cluster. The configuration metadata for these external resources is required by the Addons' Helm charts. While IaC is used to create these cloud resources, it is not used to install the Helm charts. Instead, the IaC tool stores this metadata either within GitOps resources in the cluster or in a Git repository. The GitOps tool then extracts these metadata values and passes them to the Helm chart during the Addon installation process. This mechanism forms the bridge between IaC and GitOps, hence the term "GitOps Bridge."

Try out the [Getting Started](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/getting-started) example.

Aditonal examples available on the [GitOps Bridge Pattern](https://github.com/gitops-bridge-dev):
- [argocd-ingress](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/argocd-ingress)
- [aws-secrets-manager](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/aws-secrets-manager)
- [crossplane](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/crossplane)
- [external-secrets](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/external-secrets)
- [multi-cluster/distributed](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/multi-cluster/distributed)
- [multi-cluster/hub-spoke](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/multi-cluster/hub-spoke)
- [multi-cluster/hub-spoke-shared](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/multi-cluster/hub-spoke-shared)
- [private-git](https://github.com/gitops-bridge-dev/gitops-bridge/tree/main/argocd/iac/terraform/examples/eks/private-git)


