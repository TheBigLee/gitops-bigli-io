build:
	helm template influxdb --namespace=influxdb influxdata/influxdb \
		-f influx-config.yaml \
		> influxdb.yaml
.PHONY: build

update:
	helm repo update
	helm search repo influxdb
.PHONY: update
