# Running Images as Containers

Once an image is available locally, you can run it as a container.

## Basic `docker run`

```bash
docker run <image_name>
```

Creates and starts a new container from the specified image.

### Example

```bash
docker run ubuntu
```

This runs the Ubuntu image. Without extra flags, it will exit quickly since no interactive shell is attached.

## Detached Mode (`-d`)

```bash
docker run -d nginx
```

Runs the container in the background.

## Port Mapping (`-p`)

```bash
docker run -d -p 8080:80 nginx
```

Maps port `8080` on the host to port `80` in the container, accessible via:

`http://localhost:8080`

## Naming Containers (`--name`)

```bash
docker run -d --name webserver nginx
```

Assigns a custom name to the container.

## Interactive Terminal (`-it`)

```bash
docker run -it ubuntu bash
```

Starts an interactive Bash shell inside the container.

## Listing Containers

```bash
docker ps       # running containers
docker ps -a    # all containers
```

## Complete Example

```bash
docker pull nginx
docker run -d -p 8080:80 --name mynginx nginx
docker ps
```

Open in browser: `http://localhost:8080`
