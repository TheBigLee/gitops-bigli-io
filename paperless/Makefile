build:
	helm template paperless-redis --namespace=paperless bitnami/redis \
		-f redis-config.yaml \
		> redis.yaml
	helm template paperless-postgresql --namespace=paperless bitnami/postgresql \
		-f postgresql-config.yaml \
		> postgresql.yaml
.PHONY: build

update:
	helm repo update
	helm search repo k8s-at-home
.PHONY: update
