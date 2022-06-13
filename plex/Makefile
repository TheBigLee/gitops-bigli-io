build:
	helm template radarr --namespace=plex k8s-at-home/radarr \
		-f radarr-config.yaml \
		> radarr.yaml
	helm template sonarr --namespace=plex k8s-at-home/sonarr \
		-f sonarr-config.yaml \
		> sonarr.yaml
.PHONY: build

update:
	helm repo update
	helm search repo k8s-at-home
.PHONY: update
