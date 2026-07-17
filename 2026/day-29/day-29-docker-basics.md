# Day 29 - Introduction to Docker

## What is Docker?

Docker is an open-source platform that allows developers to package applications and all their dependencies into lightweight containers. These containers can run consistently on any machine.

---

## What is a Container?

A container is a lightweight package that contains:

- Application code
- Runtime
- Libraries
- Dependencies
- Configuration files

Containers ensure that applications run the same way everywhere.

### Why do we need Containers?

- Consistent environment
- Faster deployment
- Lightweight
- Portable
- Easy scaling
- Better resource utilization

---

# Containers vs Virtual Machines

| Containers | Virtual Machines |
|------------|------------------|
| Lightweight | Heavy |
| Share host OS kernel | Each VM has its own OS |
| Fast startup | Slow startup |
| Low memory usage | High memory usage |
| Portable | Less portable |
| Better performance | More overhead |

---

# Docker Architecture

Docker consists of four main components:

## 1. Docker Client

The Docker Client is where users type Docker commands.

Example:

```bash
docker run nginx
```

---

## 2. Docker Daemon

The Docker Daemon receives commands from the Docker Client.

It is responsible for:

- Building Images
- Running Containers
- Managing Networks
- Managing Volumes

---

## 3. Docker Images

Images are read-only templates used to create containers.

Example:

- nginx
- ubuntu
- mysql

---

## 4. Docker Containers

Containers are running instances of Docker Images.

Example:

Ubuntu Image
↓

Ubuntu Container

---

## 5. Docker Registry

Docker Registry stores Docker Images.

The default registry is:

Docker Hub

---

# Docker Architecture Diagram

                Docker User
                     |
                     |
             docker run nginx
                     |
              Docker Client
                     |
              Docker Daemon
           /        |        \
      Images   Containers   Network
                     |
               Docker Hub

---

# Docker Installation

Docker Desktop was installed successfully.

Verification command:

```bash
docker --version
```

Example Output

```
Docker version xx.xx.xx
```

---

# Running Hello World

Command

```bash
docker run hello-world
```

Result

- Docker downloaded the image.
- Created a container.
- Ran the container.
- Displayed the Hello World message.
- Exited successfully.

---

# Running Nginx Container

Command

```bash
docker run -d -p 8080:80 --name mynginx nginx
```

Browser

```
http://localhost:8080
```

The Nginx welcome page was displayed successfully.

---

# Running Ubuntu Container

Command

```bash
docker run -it ubuntu bash
```

Inside Ubuntu

Commands used

```bash
pwd
ls
whoami
hostname
cat /etc/os-release
```

Exit

```bash
exit
```

---

# List Running Containers

```bash
docker ps
```

---

# List All Containers

```bash
docker ps -a
```

---

# Stop Container

```bash
docker stop mynginx
```

---

# Remove Container

```bash
docker rm mynginx
```

---

# Detached Mode

Command

```bash
docker run -d nginx
```

Detached mode runs the container in the background.

---

# Custom Name

```bash
docker run --name myubuntu ubuntu
```

---

# Port Mapping

```bash
docker run -d -p 8080:80 nginx
```

Host Port:

8080

Container Port:

80

---

# View Logs

```bash
docker logs mynginx
```

---

# Execute Command Inside Running Container

```bash
docker exec -it mynginx bash
```

Example Commands

```bash
pwd
ls
hostname
```

Exit

```bash
exit
```

---

# Conclusion

Today I learned:

- What Docker is
- What Containers are
- Docker Architecture
- Docker Images
- Docker Hub
- Docker Client
- Docker Daemon
- Running Containers
- Nginx Container
- Ubuntu Container
- Docker Logs
- Docker Exec
- Docker Port Mapping
