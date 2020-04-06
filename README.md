# GitOps for bigli.io k3s hosting

## Repo structure

* Each subdirectory is a namespace
* `_apps` is the meta directory for Argo CD apps

## Usage

### Argo CD

#### Access

Either

`sudo -E kubefwd svc -n argocd` and then https://argocd-server/

or

`kubectl port-forward svc/argocd-server -n argocd 8080:443` and
then https://localhost:8080/

#### CLI

* `argocd login argocd-server`
* `argocd app list`
* `argocd app sync <name>`

### Kubeseal (Sealed Secrets)

See README of apps. Basically:

## Bootstrap GitOps

After installing k3s, do:

```
# install Argo CD
kubectl create ns argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl get pods -n argocd -l app.kubernetes.io/name=argocd-server -o name | cut -d'/' -f 2
argocd login argocd-server

# Instantiate Argo Root App
kubectl apply -f _apps/apps.yaml

# Let Argo CD do it's job
argocd app sync apps
argocd app sync sealed-secrets
argocd app sync -l app.kubernetes.io/instance=apps
