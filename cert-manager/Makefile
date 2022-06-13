build:
	helm template cert-manager --namespace=cert-manager \
		--create-namespace --version v1.8.0 \
		--set installCRDs=true jetstack/cert-manager \
		> cert-manager.yaml
.PHONY: build

update:
	helm repo update
	helm search repo jetstack
.PHONY: update
