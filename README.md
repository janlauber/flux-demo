# flux-demo

Flux demo repository

## Prerequisites

* [Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
* [MiniKube](https://kubernetes.io/docs/tasks/tools/install-minikube/)
* [Flux](https://docs.fluxcd.io/en/latest/tutorials/get-started.html)
* [Kustomize](https://kubernetes-sigs.github.io/kustomize/installation/)

## Setup

### Start MiniKube

```bash
minikube start
```

### Github

Create a Github personal access token with the administration permissions.

```bash
export GITHUB_TOKEN=<gh-token>
```

### Install Flux

```bash
flux bootstrap github \
  --owner=janlauber \
  --repository=flux-demo \
  --branch=main \
  --path=./clusters/demo \
  --personal
```

### Check Flux

```bash
flux check
```

### Check Flux logs

```bash
flux logs
```

### Check Flux kustomizations

```bash
flux get kustomizations
```
