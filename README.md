# game-2048
2048 Game Kubernetes deployment

## Install `kubectl`:
```shell
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/arm64/kubectl"
```

## Get Kubeconfig
```shell
CLUSTER_NAME=
REGION=
aws eks update-kubeconfig --name $CLUSTER_NAME --region $REGION --kubeconfig kubeconfig 
```

## Deploy manifests
```shell
export KUBECONFIG=kubeconfig
kubectl apply -f deployment.yaml
```

## Get Load Balancer
```shell
kubectl get svc -l app=game-2048
```