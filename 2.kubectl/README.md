# Installing kubectl on your machine
https://kubernetes.io/docs/tasks/tools/install-kubectl/

# Clone this repository
git clone git@github.com:mihail-velikov/workshop.git

# copy the "config" file in ~/.kube/

# After you have setup your connectivity to the cluster it is time to test it. Several kubectl commands are very useful
# This one shows the available nodes in the cluster
kubectl get nodes

# Describe a node
kubectl describe my-node

# List the pods in the current namespace 
kubectl get pods

# Describe a container
kubectl describe pod my-pod

# List namespaces
kubectl get namespaces

# List pods in a particular namespace
kubectl get pods -n kube-system

# Check the logs of a container:
kubectl logs my-pod

# Tail the logs of a container:
kubectl logs -f my-pod


# Kubectl cheat sheet
https://kubernetes.io/docs/reference/kubectl/cheatsheet/
