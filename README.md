# full-cycle-2.0-kubernetes

Files I produced during the Kubernetes classes of my [Microservices Full Cycle 3.0 course](https://drive.google.com/file/d/1bJnFxQPKgSsI30sCvW-KzYK4V5JWzgSs/view?usp=share_link).

# Stress test

```sh
kubectl run -it fortio --rm --image=fortio/fortio -- load -qps 800 -t 120s -c 70 "http://goserver/healthz"
```

# Ingress controller

https://kubernetes.github.io/ingress-nginx/deploy/#using-helm

```sh
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update

helm install ingress-nginx ingress-nginx/ingress-nginx
```

# Cert manager

https://cert-manager.io/docs/installation/kubernetes/

```sh
kubectl apply -f https://github.com/jetstack/cert-manager/releases/download/v1.4.0/cert-manager.yaml
```

# Utils

```sh
kubectl config get-contexts # List clusters
kubectl config use-context kind-fullcycle # Switch to cluster 'kind-fullcycle'
kubectl api-resources # List k8s objects and their api version (Ex.: deployments apps/v1 Deployment)
```
