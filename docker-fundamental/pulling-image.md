# Pulling Docker Images

Pulling an image is usually the first step when working with Docker. An image contains everything needed to run an application (runtime, libraries, configuration, and filesystem).

## Basic Pull Command

```bash
docker pull <image_name>:<tag>
```

Downloads a specific image (and its tag/version) from a container registry to your local machine.

### Examples

```bash
docker pull nginx:latest
docker pull ubuntu:22.04
docker pull postgres:16
```

## Listing Images

```bash
docker images
```

Displays all images currently stored locally.

```text
REPOSITORY   TAG       IMAGE ID       CREATED        SIZE
nginx        latest    605c77e624dd   2 days ago     188MB
ubuntu       22.04     a1b2c3d4e5f6   1 week ago     77MB
postgres     16        9f8e7d6c5b4a   3 weeks ago    374MB
```
