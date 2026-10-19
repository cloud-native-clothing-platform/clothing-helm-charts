# Clothing Service Helm Chart

Reusable chart for deploying one HTTP service. Defaults are internal-only (ClusterIP) and ingress is disabled.

Validate with `helm lint .` and `helm template catalog . --set image.repository=YOUR_ECR_URI --set image.tag=IMMUTABLE_TAG`. Install with `helm upgrade --install catalog . -n clothing --create-namespace --set image.repository=YOUR_ECR_URI --set image.tag=IMMUTABLE_TAG`.

Review health endpoints, resource sizing, TLS, secrets, autoscaling, and PodDisruptionBudgets before production.
