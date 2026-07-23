\# Day 30 – Docker Images \& Container Lifecycle



\## Task 1: Docker Images



\### Images Pulled

\- nginx

\- ubuntu

\- alpine



\### Available Images



| Image | Disk Usage |

|--------|------------|

| nginx | 241 MB |

| ubuntu | 161 MB |

| alpine | 13 MB |



\### Ubuntu vs Alpine



Ubuntu is a complete Linux distribution with many tools, packages, and libraries.



Alpine is a lightweight Linux distribution designed specifically for containers.



Because Alpine contains only essential components, it is much smaller and downloads faster than Ubuntu.



\### Image Inspection



Command Used:



```bash

docker image inspect nginx

```



Information Observed:

\- Image ID

\- Repository Tags

\- Created Date

\- Environment Variables

\- Exposed Ports

\- Entrypoint

\- Default Command

\- Operating System

\- Architecture

\- Image Layers



\### Removed Image



```bash

docker image rm alpine

```



\---



\## Task 2: Image Layers



Command:



```bash

docker image history nginx

```



\### What are Docker Layers?



Docker images are built using multiple read-only layers.



Each instruction in a Dockerfile creates a new layer.



Docker uses layers because:

\- Saves disk space

\- Speeds up image builds

\- Reuses cached layers

\- Makes image downloads faster



Some layers show \*\*0B\*\* because they only store metadata such as:

\- ENV

\- CMD

\- ENTRYPOINT

\- LABEL

\- EXPOSE



\---



\## Task 3: Container Lifecycle



Commands Practiced:



```bash

docker create --name lifecycle-demo nginx

docker start lifecycle-demo

docker pause lifecycle-demo

docker unpause lifecycle-demo

docker stop lifecycle-demo

docker restart lifecycle-demo

docker kill lifecycle-demo

docker rm lifecycle-demo

```



Container states observed:

\- Created

\- Running

\- Paused

\- Stopped

\- Restarted

\- Killed

\- Removed



\---



\## Task 4: Working with Running Containers



Commands Used:



```bash

docker run -d --name nginx-demo -p 8081:80 nginx

docker logs nginx-demo

docker logs -f nginx-demo

docker exec -it nginx-demo bash

docker exec nginx-demo ls /

docker inspect nginx-demo

```



Learned:

\- View container logs

\- Follow real-time logs

\- Execute commands inside a running container

\- Inspect container details

\- Check IP Address

\- Check Port Mapping

\- Check Mount Information



\---



\## Task 5: Cleanup



Commands:



```bash

docker stop $(docker ps -q)

docker container prune -f

docker image prune -a

docker system df

```



Learned:

\- Stop all running containers

\- Remove stopped containers

\- Remove unused images

\- Check Docker disk usage



\---



\## Summary



Today I learned:

\- Difference between Docker Images and Containers

\- Why Alpine is smaller than Ubuntu

\- Docker Image Layers

\- Complete Container Lifecycle

\- Container Logs

\- Docker Inspect

\- Docker Cleanup Commands

