# Overview

This project uses GitOps principles to manage and deploy a web application to a Kubernetes cluster. The application deployment is managed by Argo CD, and changes trigger an automatic deployment.

## What is GitOps
GitOps is a set of practices to manage infrastructure and application configurations using Git as the single source of truth. By leveraging Git workflows, GitOps enables teams to use version control for defining and deploying system architecture and operational procedures, ensuring a declarative and automated approach to infrastructure management. 

### 4 Principles of GitOps

1. Declarative - A system managed by GitOps must have its desired state expressed declaratively.
2. Versioned and Immutable - Desired state is stored in a way that enforces immutability, versioning and retains a complete version history.
3. Pulled Automatically - Software agents automatically pull the desired state declarations from the source.
4. Continuously Reconciled - Software agents continuously observe actual system state and attempt to apply the desired state.


### How Does Argo CD Implement These Practices?

In summary Argo CD works as GitOps controller that pulls automatically updates (principle 3) from manifests stored in Git (principle 2) that describe Kubernetes objects in a declarative manner (principle 1). The syncing process between Git and cluster is happening at regular intervals and works both ways so if you understand the principles of GitOps you can understand the decisions behind Argo CD. The GitOps principles are explained at opengitops.dev. In summary Argo CD works as GitOps controller that pulls automatically updates (principle 3) from manifests stored in Git (principle 2) that describe Kubernetes objects in a declarative manner (principle 1). The syncing process between Git and cluster is happening at regular intervals and works both ways
