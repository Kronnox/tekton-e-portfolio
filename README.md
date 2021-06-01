# tekton-e-portfolio

## Setup Kubernetes

Check cluster connection:
```
kubectl config view
```

Check cluster health:
```
kubectl version
```

## Install Tekton Pipelines

Apply project files:
```
kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml
```

Check status:
```
kubectl get pods --namespace tekton-pipelines --watch
```

## Install Tekton Dashboard

Apply project files:
```
kubectl apply --filename https://github.com/tektoncd/dashboard/releases/latest/download/tekton-dashboard-release.yaml
```

Open proxy:
```
kubectl proxy --port=8080
```

Proxy url:
```
https://localhost:8080/api/v1/namespaces/tekton-pipelines/services/tekton-dashboard:http/proxy/
```

Check status:
```
kubectl get pods --namespace tekton-pipelines --watch
```

## Useful links
23:41

https://tekton.dev/docs/getting-started/<br>
https://tekton.dev/docs/dashboard/<br>
https://hub.tekton.dev<br>

