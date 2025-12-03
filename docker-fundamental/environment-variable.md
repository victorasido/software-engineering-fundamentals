# Environment Variables in Docker Containers

Environment variables allow you to configure a container without hardcoding values inside the image.

## Passing Variables with `-e`

```bash
docker run -e DB_USER=admin -e DB_PASS=secret ubuntu env
```

## Using a `.env` File

Example `.env`:

```text
DB_USER=admin
DB_PASS=secret
```

Run with:

```bash
docker run --env-file .env ubuntu env
```

## Viewing Environment Variables

```bash
docker exec myapp printenv
```
