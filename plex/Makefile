build:
	helm3 template radarr --namespace=plex billimek/radarr \
		-f radarr-config.yaml \
		> radarr.yaml
	helm3 template sonarr --namespace=plex billimek/sonarr \
		-f sonarr-config.yaml \
		> sonarr.yaml
.PHONY: build

update:
	helm3 repo update
	helm3 search repo billimek
.PHONY: update
