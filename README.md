# task-tracking-app-gitops

GitOps manifests for the task tracking application.

## Layout

- `applications/`: Argo CD `Application` resources for dev, UAT, and production.
- `base/`: Shared application Kubernetes manifests for frontend, backend, database, services, ingress, and namespaces.
- `monitoring/base/`: Shared monitoring and logging manifests for Prometheus, Grafana, Fluentd, Elasticsearch, and Kibana.
- `overlays/`: Environment-specific Kustomize overlays and image repositories.

## Apply an Argo CD application

```bash
kubectl apply -f applications/task-tracking-app-dev.yaml
```

Replace `dev` with `uat` or `production` for the other environments.
