# Redis UI on Kubernetes

## Install

### 1. Create nginx credential using htpasswd
```bash
$ htpasswd -c auth <yourusername>
```

### 2. Created a secret having user and password hashed

```bash
$ kubectl create secret generic basic-auth-for-redisinsight --from-file=auth --namespace=redisinsight
```
### 3. Apply the manifest
```bash
$ kubectl apply -f redisinsight.yaml
```

### Reference
https://fahadahammed.medium.com/how-to-deploy-redisinsight-in-eks-and-access-via-ingress-nginx-3e4daf5008e0