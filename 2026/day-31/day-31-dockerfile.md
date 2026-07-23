\# Day 31 – Dockerfile: Build Your Own Images



\## Objective



Learn how to create custom Docker images using Dockerfiles and understand Dockerfile instructions.



\---



\# Task 1 – Your First Dockerfile



\### Dockerfile



```dockerfile

FROM ubuntu



RUN apt-get update \&\& apt-get install -y curl



CMD \["echo", "Hello from my custom image!"]

```



\### Commands Used



```bash

docker build -t my-ubuntu:v1 .

docker run my-ubuntu:v1

docker images

```



\### Output



```

Hello from my custom image!

```



\### What I Learned



\- Created my first Dockerfile

\- Built a custom Docker image

\- Ran a container from the image



\---



\# Task 2 – Dockerfile Instructions



\### Instructions Used



\- FROM

\- RUN

\- COPY

\- WORKDIR

\- EXPOSE

\- CMD



\### Explanation



\- \*\*FROM\*\* → Specifies the base image.

\- \*\*RUN\*\* → Executes commands while building the image.

\- \*\*COPY\*\* → Copies files from host to image.

\- \*\*WORKDIR\*\* → Sets the working directory.

\- \*\*EXPOSE\*\* → Documents the application port.

\- \*\*CMD\*\* → Defines the default command.



\---



\# Task 3 – CMD vs ENTRYPOINT



\## CMD



\- Provides a default command.

\- Can be overridden by passing another command to `docker run`.



Example:



```bash

docker run cmd-demo:v1

```



Output:



```

hello

```



Override:



```bash

docker run cmd-demo:v1 ls

```



\## ENTRYPOINT



\- Defines the main executable.

\- Additional arguments are appended to the ENTRYPOINT.



Example:



```bash

docker run entry-demo:v1 Hello Docker

```



Output:



```

Hello Docker

```



\### CMD vs ENTRYPOINT



| CMD | ENTRYPOINT |

|------|------------|

| Can be overridden | Stays fixed |

| Default command | Main executable |



\---



\# Task 4 – Build a Simple Web App Image



\### Base Image



```

nginx:alpine

```



\### Dockerfile



```dockerfile

FROM nginx:alpine



COPY index.html /usr/share/nginx/html/index.html

```



\### Commands



```bash

docker build -t my-website:v1 .

docker run -d --name mywebsite31 -p 8083:80 my-website:v1

```



\### Result



Successfully hosted a static website using Docker and Nginx.



\---



\# Task 5 – .dockerignore



Contents:



```text

node\_modules

.git

\*.md

.env

```



\### Why use .dockerignore?



\- Reduces build context size.

\- Speeds up image builds.

\- Prevents unnecessary files from entering the image.



\---



\# Task 6 – Build Optimization



\### What I Learned



Docker caches image layers.



If only a later layer changes, Docker reuses previous layers, making rebuilds much faster.



Best Practice:



Place frequently changing instructions near the end of the Dockerfile to maximize cache reuse.



\---



\# Conclusion



Today I learned how to:



\- Write Dockerfiles

\- Build custom Docker images

\- Use Dockerfile instructions

\- Understand CMD vs ENTRYPOINT

\- Create Nginx web images

\- Use .dockerignore

\- Optimize Docker builds using cache



\---



\# Screenshots



\- Docker Build

\- Docker Run

\- Docker Images

\- Dockerfile Demo

\- Website Output

\- CMD Demo

\- ENTRYPOINT Demo

\- .dockerignore Build

\- Docker Cache Build

