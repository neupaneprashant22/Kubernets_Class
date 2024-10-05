# Basics of Kubernetes
# Minikube and Kubernetes Commands used in Class

## Minikube Commands

### Start Minikube
```bash
minikube start
```
Starts a local Kubernetes cluster using Minikube.

### Check Minikube Status
```bash
minikube status
```
Displays the status of the Minikube cluster, including information on nodes and Kubernetes components.

## Kubernetes Commands

### Get Nodes
```bash
kubectl get nodes
```
Displays the nodes available in your Kubernetes cluster.

### Get Pods
```bash
kubectl get pods
```
Shows the list of all running pods in the current namespace.

### Get Services
```bash
kubectl get services
```
Lists all services currently running in your cluster.

### Get Services with Wide Output
```bash
kubectl get services -o wide
```
Displays additional details about the services, including internal/external IP addresses and associated nodes.

### Get Namespaces
```bash
kubectl get namespaces
```
Displays all namespaces currently present in the Kubernetes cluster.

### Get ReplicaSets
```bash
kubectl get replicaset
```
Lists all ReplicaSets that control the number of pod replicas.

### Get Deployments
```bash
kubectl get deployments
```
Lists all deployments, showing the desired and current state of the deployment.

## Deployment Operations

### Create Deployment Help
```bash
kubectl create deployment --help
```
Shows help documentation for creating deployments using `kubectl`.

### Create Nginx Deployment
```bash
kubectl create deployment nginx-deployment --image=nginx
```
Creates a deployment named `nginx-deployment` with the Nginx image.

### Edit Deployment
```bash
kubectl edit deployment nginx-deployment
```
Opens the deployment configuration for editing, allowing you to modify the deployment's properties.

### View Deployment Logs
```bash
kubectl logs nginx-deployment-5b5d98589c-wmnq8
```
Displays the logs for the specified pod in the deployment.

### Execute Commands in Pods
```bash
kubectl exec --help
```
Shows help documentation for executing commands inside a pod.

### Create MongoDB Deployment
```bash
kubectl create deployment mongo-depl --image=mongo
```
Creates a deployment for MongoDB named `mongo-depl`.

### View MongoDB Logs
```bash
kubectl logs mongo-depl-67d7db846c-2p9zt
```
Displays the logs of the MongoDB pod.

### Edit MongoDB Deployment
```bash
kubectl edit deployment mongo-depl
```
Opens the MongoDB deployment configuration for editing.

## Additional Kubernetes Commands

### Access Minikube Dashboard
```bash
minikube dashboard --url
```
Launches the Minikube dashboard in the browser and returns the URL.

### Apply Nginx Deployment from YAML
```bash
kubectl apply -f nginx-deployment.yaml
```
Applies the Nginx deployment configuration defined in `nginx-deployment.yaml`.

### Get Nginx Deployment YAML
```bash
kubectl get deployment nginx-deployment1 -o yaml
```
Displays the YAML configuration of the `nginx-deployment1`.

### Apply Nginx Service from YAML
```bash
kubectl apply -f nginx-service.yaml
```
Applies the Nginx service configuration defined in `nginx-service.yaml`.

### Get Nginx Service URL
```bash
minikube service nginx-service --url
```
Gets the URL of the Nginx service running in the cluster.
