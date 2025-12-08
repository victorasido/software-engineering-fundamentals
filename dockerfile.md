# Dockerfile

## 1. Overview
A Dockerfile is a declarative file that defines the steps required to build a Docker image. It specifies the base image, dependencies, application files, configurations, and the command executed at runtime.

---

## 2. Purpose
- Ensure consistent and reproducible builds  
- Standardize environment setup  
- Automate packaging of applications  
- Reduce manual configuration across environments (development, staging, production)

---

## 3. Core Instructions

### 3.1 FROM
Defines the base image used as the starting layer.

```dockerfile
FROM node:18-alpine
```

### 3.2 WORKDIR
Sets the working directory inside the image.

```dockerdockerfile
WORKDIR /app
```

### 3.3 COPY
Copies files from the host machine into the image.

```dockerfile
COPY package*.json ./
COPY . .
```

### 3.4 RUN
Executes commands during build time (e.g., installing dependencies).

```dockerfile
RUN npm install
```

### 3.5 EXPOSE
Documents the port the container listens on.

```dockerfile
EXPOSE 3000
```

### 3.6 CMD
Specifies the command executed when the container starts.

```dockerfile
CMD ["npm", "start"]
```

---

## 4. Example Dockerfile

```dockerfile
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3000
CMD ["npm", "start"]
```

---

## 5. Building an Image

Use the command below to build the image:

```bash
docker build -t myapp:1.0 .
```

Check available images:

```bash
docker images
```

---

## 6. .dockerignore

Use `.dockerignore` to exclude unnecessary files from the build context.

Example:

```
node_modules
.git
.env
Dockerfile
npm-debug.log
```

Benefits:
- Faster build  
- Smaller image size  
- Prevents accidental inclusion of sensitive files  

---

## 7. Best Practices
1. Use minimal base images such as `alpine`  
2. Place dependency installation steps at the top to maximize caching  
3. Reduce layer count by combining related `RUN` commands  
4. Avoid embedding secrets in the Dockerfile  
5. Use consistent and meaningful image tags  

---

## 8. Summary
- A Dockerfile defines how an image is built  
- Each instruction creates a cached image layer  
- Images are reproducible across environments  
- Build with `docker build` and optimize for efficiency  
