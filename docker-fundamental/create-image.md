# Creating Docker Images

A Docker image is a packaged, read-only blueprint that contains everything needed to run an application: OS layer, dependencies, configuration, and the application itself. This document explains how to create an image using the correct and recommended methods.

---

## 1. What Does "Create Image" Mean?

Creating an image means building a reusable, versioned artifact that can later be run as one or many containers.

An image contains:
- Base operating system layer (e.g., alpine, ubuntu)
- Application source code
- Dependencies (npm install, pip install, go build, etc.)
- Configuration
- Default command to run

---

## 2. Creating an Image Using a Dockerfile (Recommended)

The **standard, reproducible, and production‑safe** method to create an image is with a `Dockerfile`.

### Example Dockerfile

```dockerfile
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3000
CMD ["npm", "start"]
```

### Build Command

Run this in the same folder as the Dockerfile:

```bash
docker build -t myapp:1.0 .
```

### What Happens During Build?

Docker will:
1. Read the Dockerfile line-by-line  
2. Create a new **layer** for each instruction  
3. Cache layers for faster rebuilds  
4. Produce a final, read‑only image  

You can verify the image:

```bash
docker images
```

---

## 3. Creating an Image by Committing a Container (Not Recommended)

This is a quick‑and‑dirty method—useful for experiments only.

### Steps

1. Start a container manually:
```bash
docker run -it ubuntu bash
```

2. Make changes inside the container (install packages, config, etc.)

3. Commit the container into an image:
```bash
docker commit <container_id> myimage:latest
```

> ⚠️ This method is **not reproducible** and should not be used for production.

---

## 4. Tagging an Image

Images can be tagged for versioning or pushing to registries:

```bash
docker tag myapp:1.0 myrepo/myapp:1.0
```

---

## 5. Pushing an Image to a Registry

To share or store an image:

```bash
docker push myrepo/myapp:1.0
```

Examples of registries:
- Docker Hub
- GitHub Container Registry
- GitLab Registry
- AWS ECR
- GCP Artifact Registry

---

## Summary

- **Dockerfile** is the correct way to create images  
- Images are read-only blueprints used to run containers  
- Each Dockerfile instruction creates a layer  
- `docker commit` exists but should only be used for testing  
- Once built, images can be tagged and pushed to registries  

