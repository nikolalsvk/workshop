# Installing Flux
https://docs.fluxcd.io/en/latest/tutorials/get-started-helm.html

# Add the Flux repository:
helm repo add fluxcd https://charts.fluxcd.io

# Apply the Helm Release CRD:
kubectl apply -f https://raw.githubusercontent.com/fluxcd/flux/helm-0.10.1/deploy-helm/flux-helm-release-crd.yaml

# We are ready to setup flux
helm upgrade -i flux \
  --set helmOperator.create=true \
  --set helmOperator.createCRD=false \
  --set git.url=git@github.com:mihail-velikov/workshop-flux.git \
  --set git.pollInterval=1m \
  --set git.label=flux \
  --namespace default \
fluxcd/flux

# Repo which Flux will monitor:
https://github.com/mihail-velikov/workshop-flux.git

# Flux helm operator
https://github.com/fluxcd/helm-operator
https://github.com/fluxcd/helm-operator/blob/master/chart/helm-operator/README.md
helm repo add fluxcd https://charts.fluxcd.io
kubectl apply -f https://raw.githubusercontent.com/fluxcd/helm-operator/master/deploy/flux-helm-release-crd.yaml

