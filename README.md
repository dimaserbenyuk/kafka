# kafka

https://github.com/conduktor/kafka-stack-docker-compose/blob/master/README.md

https://levelup.gitconnected.com/kraft-the-next-generation-kafka-architecture-424e70f8481b

https://levelup.gitconnected.com/kraft-kafka-cluster-with-docker-e79a97d19f2c

https://docs.confluent.io/operator/current/co-troubleshooting.html

https://docs.confluent.io/operator/current/co-prepare.html

```
helm install ingress-nginx ingress-nginx/ingress-nginx \
  --namespace ingress-nginx --create-namespace
```

```
helm install \
  cert-manager jetstack/cert-manager \
  --namespace cert-manager \
  --create-namespace \
  --version v1.14.5 \
  --set installCRDs=true
```

```
The CustomResourceDefinition "kafkas.platform.confluent.io" is invalid: metadata.annotations: Too long: must have at most 262144 bytes
➜  confluent-for-kubernetes git:(k8s) ✗ kubectl apply --server-side=true --force-conflicts -f crds/platform.confluent.io_kafkas.yaml
customresourcedefinition.apiextensions.k8s.io/kafkas.platform.confluent.io serverside-applied
```

helm install confluent-operator confluent-for-kubernetes 


kubectl apply -f crds

minikube addons enable storage-provisioner