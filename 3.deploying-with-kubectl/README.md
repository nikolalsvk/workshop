# Deploying to Kubernetes can be done in many many ways. Below you can see some examples:
kubectl apply -f ./my-manifest.yaml            # create resource(s)
kubectl apply -f ./my1.yaml -f ./my2.yaml      # create from multiple files
kubectl apply -f ./dir                         # create resource(s) in all manifest files in dir
kubectl apply -f https://git.io/vPieo          # create resource(s) from url
kubectl create deployment nginx --image=nginx  # start a single instance of nginx


# Lets try this out. I have added some example definitions in this directory. First lets deploy a pod.
kubectl create -f my-pod.yaml
kubectl get pods
kubectl describe my-pod
kubectl delete my-pod

# To delete your container:
kubectl delete -f my-pod.yaml

# Create a deployment:
kubeclt create -f nginx.yaml

# Scale the deployment - open the nginx.yaml and modify the "replicas: 1" line. Save the file and run
kubectl apply -f nginx.yaml
kubectl get pods 

# Another way to scale the deployment is to edit it directly in kubernetes
kubectl edit deployment nginx

# Deploy a service visible from the world:
kubectl create -f nginx-exposed.yaml

# Find the address at which it will be available:
kubectl get svc

# Then look at the EXTERNAL-IP column

