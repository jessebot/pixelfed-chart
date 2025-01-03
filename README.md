# Pixelfed helm chart
<a href="https://github.com/small-hack/pixelfed-chart/releases"><img src="https://img.shields.io/github/v/release/small-hack/pixelfed-chart?style=plastic&labelColor=blue&color=green&logo=GitHub&logoColor=white"></a><br />

A helm chart to setup [Pixelfed](https://pixelfed.org/). Uses matt's docker [image](ghcr.io/mattlqx/docker-pixelfed) for now. This is still in a testing phase and may not be stable.

## Features

- includes subcharts for valkey (redis) and postgresql (database)
- helm parameter docs autogenerated via helm-docs
- use existing Secrets for valkey, postgresql, and smtp
- RenovateBot keeps the subcharts and docker image up to date

## TLDR

```bash
# add the chart repo to your helm repos
helm repo add pixelfed https://small-hack.github.io/pixelfed-chart

# download the values.yaml and edit it with your own values such as YOUR hostname
helm show values pixelfed/pixelfed > values.yaml

# install the chart
helm install --namespace pixelfed --create-namespace pixelfed/pixelfed --values values.yaml
```
