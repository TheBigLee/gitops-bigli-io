build:
	helm template mongodb --namespace=unifi \
		oci://registry-1.docker.io/bitnamicharts/mongodb \
		-f mongodb-config.yaml \
		> mongodb.yaml
.PHONY: build

update:
	helm repo update
	helm search repo jetstack
.PHONY: update
