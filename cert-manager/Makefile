build:
	helm template cert-manager --namespace=cert-manager \
		--version v1.13.2 \
		--set installCRDs=true jetstack/cert-manager \
		> cert-manager.yaml
.PHONY: build

update:
	helm repo update
	helm search repo jetstack
.PHONY: update
