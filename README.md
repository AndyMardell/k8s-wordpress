# K8s WordPress

## Kubernetes

```bash
cp .env.dist .env
minikube start
minikube mount ./custom-theme:/mnt1/custom-theme
kubectl create secret generic secrets --from-env-file=.env
kubectl apply -f deployment.yml
```

To see your deployment progress:

```bash
kubectl get pod
```

To retrieve the URL:

```bash
minikube service list
```

## Docker

As a comparison/referenece, I have added a `docker-compose.yml` file

```bash
cp .env.dist .env
docker-compose up
```
