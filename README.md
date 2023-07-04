# game-2048
2048 Game Kubernetes deployment

## Install `kubectl`:
```shell
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/arm64/kubectl"
```

## Deploy manifests
```shell
kubect lapply -f deployment.yaml
```