# Docker Compose

Docker Compose simplifies running multi-container applications using a YAML configuration file.

## Basic Example

```yaml
version: "3.9"

services:
  web:
    image: nginx
    ports:
      - "8080:80"

  db:
    image: postgres:16
    environment:
      POSTGRES_USER: admin
      POSTGRES_PASSWORD: pass
```

## Start Services

```bash
docker compose up -d
```

## Stop Services

```bash
docker compose down
```

## Rebuild

```bash
docker compose up -d --build
```

## View Logs

```bash
docker compose logs -f
```
