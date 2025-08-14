# java-bank
Bank app for yandex practicum

## Старт приложения

bash run-local.sh

## Старт тестов

bash run-test.sh

## Создание контейнеров и запуск

bash run-docker.sh

## Содержимое файла .env ()

```
BASE_URL=http://localhost:8080

KUBECONFIG_PATH=
GHCR_TOKEN=
GITHUB_USERNAME=
GITHUB_TOKEN=
GITHUB_REPOSITORY=
DOCKER_REGISTRY=
DB_PASSWORD=

KEYCLOAK_ADMIN=
KEYCLOAK_ADMIN_PASSWORD=
KEYCLOAK_URL=
OAUTH2_REALM=

POSTGRES_DB=
POSTGRES_USER=
POSTGRES_PASSWORD=
POSTGRES_PORT=
POSTGRES_HOST=
ACCOUNT_SERVICE_POSTGRES_DB=

KC_HOSTNAME=
KC_PORT=
KC_HTTP_ENABLED=true
KC_PROXY=edge
KC_DB=
KC_DB_USERNAME=
KC_DB_PASSWORD=
KC_DB_URL=
```