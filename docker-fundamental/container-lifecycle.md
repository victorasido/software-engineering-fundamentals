# Docker Container Lifecycle

A Docker container goes through several stages:
1. Create
2. Start
3. Run
4. Stop
5. Restart
6. Pause / Unpause
7. Kill
8. Remove (Delete)

## Create 

```bash
docker create --name mycontainer ubuntu
```

## Start

```bash
docker start mycontainer
```

## Run (Create + Start)

```bash
docker run --name mycontainer ubuntu
```

## Stop

```bash
docker stop mycontainer
```

## Restart

```bash
docker restart mycontainer
```

## Pause / Unpause

```bash
docker pause mycontainer
docker unpause mycontainer
```

## Kill

```bash
docker kill mycontainer
```

## Remove

```bash
docker rm mycontainer
# or force remove
docker rm -f mycontainer
```

## Summary Table

| Stage   | Command          | Description                          |
|---------|------------------|--------------------------------------|
| Create  | `docker create`  | Create container without starting it |
| Start   | `docker start`   | Start existing container             |
| Run     | `docker run`     | Create + start container             |
| Stop    | `docker stop`    | Graceful stop                        |
| Restart | `docker restart` | Stop then start                      |
| Pause   | `docker pause`   | Freeze processes                     |
| Unpause | `docker unpause` | Resume processes                     |
| Kill    | `docker kill`    | Force stop                           |
| Remove  | `docker rm`      | Delete container                     |
