# Nginx DaemonSet Deployment

This project provides a Kubernetes DaemonSet configuration for deploying Nginx across your cluster. Below are the details for setting up and using this project.

## Project Structure

```
nginx-daemonset
├── k8s
│   ├── daemonset.yaml        # Kubernetes DaemonSet definition for Nginx
│   └── kustomization.yaml     # Kustomize configuration
├── Dockerfile                 # Dockerfile for building the Nginx image
├── Makefile                   # Automation tasks for build and deployment
├── .gitignore                 # Files and directories to ignore in Git
└── README.md                  # Project documentation
```

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd nginx-daemonset
   ```

2. **Build the Docker Image**
   Use the provided `Makefile` to build the Docker image.
   ```bash
   make build
   ```

3. **Deploy to Kubernetes**
   Apply the Kubernetes configurations using `kubectl`.
   ```bash
   kubectl apply -k k8s/
   ```

## Usage

Once deployed, the Nginx DaemonSet will ensure that an Nginx pod runs on each node in your Kubernetes cluster. You can access the Nginx service through the node's IP address on the specified port.

## Additional Information

- Ensure that your Kubernetes cluster is up and running.
- Modify the `k8s/daemonset.yaml` file to customize the Nginx configuration as needed.
- Refer to the `Dockerfile` for details on how the Nginx image is built.

For any issues or contributions, please open an issue or submit a pull request in the repository.