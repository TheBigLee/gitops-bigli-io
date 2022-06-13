build:
	helm template graphs --namespace=graphs grafana/grafana \
		-f grafana-config.yaml \
		> grafana.yaml
.PHONY: build

update:
	helm repo update
	helm search repo grafana
.PHONY: update
