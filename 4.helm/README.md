# What is helm?

Helm is the first application package manager running atop Kubernetes. It allows describing the application structure through convenient helm-charts and managing it with simple commands.

# What are charts?
Helm uses a packaging format called charts. A chart is a collection of files that describe a related set of Kubernetes resources. A single chart might be used to deploy something simple, like a memcached pod, or something complex, like a full web app stack with HTTP servers, databases, caches, and so on.


# Installing helm
# I have already deployed helm in the cluster so you only need to do:
https://helm.sh/docs/using_helm/#installing-helm

# Init our helm
helm init --client-only

# Main helm chart repository:
https://github.com/helm/charts/tree/master/stable

# Lets look at an example chart
https://github.com/helm/charts/tree/master/stable/rabbitmq

# Installing a chart:
helm install --name my-name stable/rabbitmq

# Installing a chart and passing parameters at run time
helm install --name my-name --set rabbitmq.username=admin,rabbitmq.password=secretpassword,rabbitmq.erlangCookie=secretcookie stable/rabbitmq

# List helm charts:
helm list

# Delete a deployed chart:
helm delete my-name --purge

# Download helm chart locally:
helm fetch stable/rabbimq

# Install helm chart from local folder:
helm install --name my-name ./my-folder

# Feel free to select some of the helm chart and deploy them in the cluster :)
# Some examples:
https://github.com/helm/charts/tree/master/stable/consul
https://github.com/helm/charts/tree/master/stable/influxdb
