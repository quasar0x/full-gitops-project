# Minimalist Time-Telling Python App

This is a minimalist Python application that simply tells you the current time. Alongside that, the project uses a few DevOps tools to manage its deployment and infrastructure.

## Key Tools & Setup

- **Python**: The core of the app, used to print out the current time.
- **Terraform**: Used to bootstrap the Minikube Kubernetes cluster where the app runs.
- **Argo CD**: Employed for GitOps continuous deployment, ensuring the cluster stays up-to-date with the latest configurations.
- **GitHub Actions**: Handles the CI pipeline for testing and integration.
- **Helm**: Used for managing Kubernetes packages and making sure Argo CD can update the cluster smoothly.

## How It Works

1. **Run the App**: The Python script simply prints the current time.
2. **Deploy with Minikube**: Use Terraform to spin up a Minikube cluster.
3. **Continuous Deployment**: Argo CD listens to changes and deploys them using Helm charts.
4. **CI with GitHub Actions**: Automated tests and builds run through GitHub Actions.
