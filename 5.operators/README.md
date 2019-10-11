# What is an operator
https://kubernetes.io/docs/concepts/extend-kubernetes/operator/

Operators are software extensions to Kubernetes that make use of custom resources to manage applications and their components. Operators follow Kubernetes principles, notably the control loop. 

The Operator pattern aims to capture the key aim of a human operator who is managing a service or set of services. Human operators who look after specific applications and services have deep knowledge of how the system ought to behave, how to deploy it, and how to react if there are problems.

People who run workloads on Kubernetes often like to use automation to take care of repeatable tasks. The Operator pattern captures how you can write code to automate a task beyond what Kubernetes itself provides.


# Kafka opetaror
https://operatorhub.io/operator/strimzi-kafka-operator

# Prometheus operator
https://github.com/coreos/prometheus-operator

# Many many more operators are available:
https://operatorhub.io/

# Prometheus operator helm chart
https://github.com/helm/charts/tree/master/stable/prometheus-operator

# Deploying prometheus operator:
helm install --name my-prometheus stable/prometheus-operator

# Edit the grafana service to expose it to the world:
kubectl edit svc my-grafan-svc

# Change the type to
LoadBalancer

# Give it a couple of minutes for the LB to be provisioned and open it in your browser
# Default login credentials:
admin
prom-operator
