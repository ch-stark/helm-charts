# SonarQube

[SonarQube](https://www.sonarqube.org/) is an open sourced code quality scanning tool.

## Introduction

This chart deploys a SonarQube instance without any database. The database connection can be configured via `sonar.properties`. The application runs a non-root and can therefore be deployed to [OpenShift](https://www.openshift.com/) without special configurations.

## Prerequisites

- Kubernetes 1.7+ or OpenShift Container Platform 3.7+

## Installing the chart:

To install the chart with embedded H2 database and without persistence:

```bash
$ helm install porscheinformatik/sonarqube
```

## Configuration

| Parameter                                   | Description                               | Default                                    |
| ------------------------------------------  | ----------------------------------------  | -------------------------------------------|
| `image.repository`                          | image repository                          | `porscheinformatik/sonarqube`              |
| `image.tag`                                 | `sonarqube` image tag.                    | 6.7.5-alpine                               |
| `image.pullPolicy`                          | Image pull policy                         | `IfNotPresent`                             |
| `service.type`                              | Kubernetes service type                   | `ClusterIP`                                |
| `service.port`                              | Port inside the cluster                   | 80                                         |
| `persistence.enabled`                       | Flag for enabling persistent storage      | false                                      |
| `persistence.storageClass`                  | Storage class to be used                  | "-"                                        |
| `persistence.size`                          | Size of the volume                        | None                                       |
| `route.enabled`                             | Enable OpenShift route                    | false                                      |
| `route.hostname`                            | Host name for the route                   | None                                       |
| `contextPath`                               | The context path of the application       | /                                          |
| `additionalSonarProperties`                 | Array of additional sonar properties in the format key=value | []                      |