# Мониторинги и логи, ELK-стек

## Переменные окружения в .env

```
POSTGRES_DB=
POSTGRES_USER=
POSTGRES_PASSWORD=
POSTGRES_PORT=
POSTGRES_HOST=

KEYCLOAK_ADMIN=
KEYCLOAK_ADMIN_PASSWORD=
KEYCLOAK_URL=
OAUTH2_REALM=

KC_HOSTNAME=
KC_PORT=
KC_HTTP_ENABLED=true
KC_PROXY=edge
KC_DB=
KC_DB_USERNAME=
KC_DB_PASSWORD=
KC_DB_URL=

ACCOUNT_SERVICE_POSTGRES_DB=

BASE_URL=http://localhost:8080

KUBECONFIG_PATH=
GHCR_TOKEN=
GITHUB_USERNAME=
GITHUB_TOKEN=
GITHUB_REPOSITORY=
DOCKER_REGISTRY=
DB_PASSWORD=
```

## Запуск

```bash
helm repo add bitnami "https://helm-charts.itboon.top/bitnami" --force-update
helm repo add zipkin "https://openzipkin.github.io/zipkin-helm" --force-update
helm repo add elastic https://helm.elastic.co 

cd k8s/charts/
helm upgrade --install practicum-bank . \  
                                  -n dev --create-namespace \  
                                  -f values.yaml \  
                                  -f values-dev.yaml \  
                                  -f secret-values-dev.yaml  

minikube addons enable ingress  
sh ./run-*среда*.sh
```