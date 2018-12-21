# Rancher Logging

* Installs [Fluentd](https://www.fluentd.org/) log forwarder.

## TL;DR;

```console
$ helm install rancher-logging
```

## Introduction

This chart bootstraps a [Fluentd](https://www.fluentd.org/) daemonset and a [Log-Aggregator](https://github.com/rancher/log-aggregator) flexvolume on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.
It's use for sends logs to log target config in rancher.

## Prerequisites

- Kubernetes 1.6+ with Beta APIs enabled

## Installing the Chart

To install the chart with the release name `my-release`:

```console
$ helm install --name my-release rancher-logging
```

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example,

```console
$ helm install --name my-release \
    rancher-logging
```

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart. For example,

```console
$ helm install --name my-release -f values.yaml rancher-logging
```

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
$ helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.