# Docker Network

Docker networking allows containers to communicate with each other and external systems.

## List Networks

```bash
docker network ls
```

## Create Network

```bash
docker network create mynetwork
```

## Run Containers in a Network

```bash
docker run -d --name db --network=mynetwork postgres
docker run -d --name api --network=mynetwork myapi
```

## Remove Network

```bash
docker network rm mynetwork
```
