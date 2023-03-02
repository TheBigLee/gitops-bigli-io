# K8up installation

## Edit credentials

```
vim ../../gitops-bigli-io-private/k8up/global-backup-secret.yaml
kubeseal --controller-namespace sealed-secrets -o yaml -n k8up < ../../gitops-bigli-io-private/k8up/global-backup-secret.yaml > global-backup-secret.yaml
```
