version := 4.4.1
build:
	curl -s -o k8up-crd.yaml https://github.com/k8up-io/k8up/releases/download/k8up-$(version)/k8up-crd.yaml
	helm template k8up --namespace=k8up k8up-io/k8up \
		-f k8up-config.yaml \
		--version $(version) \
		> k8up.yaml
.PHONY: build

update:
	helm repo update
	helm search repo k8up-io
.PHONY: update
