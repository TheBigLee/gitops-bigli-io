build:
	helm3 template graphs --namespace=graphs stable/grafana \
		-f grafana-config.yaml \
		> grafana.yaml
.PHONY: build

update:
	helm3 repo update
	helm3 search repo grafana
.PHONY: update
