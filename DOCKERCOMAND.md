# 🐳 Running Containers with Docker

## 🐧 Ubuntu in Docker

```bash
docker run -it ubuntu bash
```

🔹 This command runs an interactive Ubuntu container with a Bash shell.

---

## 🌐 Nginx Web Server

```bash
docker run -d -p 8080:80 nginx
```

🔹 This launches an Nginx web server in detached mode and maps port `8080` on your machine to port `80` in the container.

---

## 🔍 Manage Running Containers

### View running containers:
```bash
docker ps
```

### Stop a container:
```bash
docker stop <CONTAINER_ID>
```

### Remove a container:
```bash
docker rm <CONTAINER_ID>
```

ℹ️ Replace `<CONTAINER_ID>` with the actual container ID shown by `docker ps`.
