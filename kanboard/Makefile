build:
	helm template kanboard --namespace=kanboard k8s-at-home/kanboard \
		-f kanboard-config.yaml \
		> kanboard.yaml
.PHONY: build

update:
	helm repo update
	helm search repo k8s-at-home
.PHONY: update
