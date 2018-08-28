# Helm Charts for Porsche Informatik

[![Build Status](https://travis-ci.org/porscheinformatik/helm-charts.svg?branch=master)](https://travis-ci.org/porscheinformatik/helm-charts)

URL: https://porscheinformatik.github.io/helm-charts/

This is a collection of Helm charts used by Porsche Informatik. All charts can be used in OpenShift and a secured Kubernetes cluster (running containers as non-root).

## Usage

Add the Helm repository:

```bash
helm repo add porscheinformatik https://porscheinformatik.github.io/helm-charts/
helm repo update
```

Install stuff

    helm install porscheinformatik/mongodb

## Charts

- MongoDB
- PostgreSQL
- Rocket.Chat
- MariaDB
- Zanata