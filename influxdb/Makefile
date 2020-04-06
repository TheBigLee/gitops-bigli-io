build:
	helm3 template influxdb --namespace=influxdb influxdata/influxdb \
		-f influx-config.yaml \
		> influxdb.yaml
.PHONY: build

update:
	helm3 repo update
	helm3 search repo influxdb
.PHONY: update
