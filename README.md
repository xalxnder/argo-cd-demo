# Overview

This project uses GitOps principles to manage and deploy a web application to a Kubernetes cluster. The application deployment is managed by Argo CD, and changes trigger an automatic deployment.

## What is GitOps
GitOps is a set of practices to manage infrastructure and application configurations using Git as the single source of truth. By leveraging Git workflows, GitOps enables teams to use version control for defining and deploying system architecture and operational procedures, ensuring a declarative and automated approach to infrastructure management. 

### How Does Argo CD Implement These Practices?

In summary Argo CD works as GitOps controller that pulls automatically updates (principle 3) from manifests stored in Git (principle 2) that describe Kubernetes objects in a declarative manner (principle 1). The syncing process between Git and cluster is happening at regular intervals and works both ways so if you understand the principles of GitOps you can understand the decisions behind Argo CD. The GitOps principles are explained at opengitops.dev. In summary Argo CD works as GitOps controller that pulls automatically updates (principle 3) from manifests stored in Git (principle 2) that describe Kubernetes objects in a declarative manner (principle 1). The syncing process between Git and cluster is happening at regular intervals and works both ways
