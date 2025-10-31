# Docker-Test
## Section 1: Docker Run & Containers
  
 Q.1 - c) The container exited because no foreground process was running

 Q.2 - b) The second command will fail due to port conflict

 Q.1 - b) Exited

 Q.1 - b) --rm

 Q.2 - a) Yes

 Q.1 - b) ENTRYPOINT ignores additional arguments, CMD overrides them

 ## Section 2: Dockerfile

 Q.1 - c) WORKDIR

 Q.2 - a) Yes

 Q.1 - c) 

 Q.1 - c) Remove files from built images

 Q.2 - c) Only the last one takes effect

 Q.3 - b) 2

 ## Section 3: Docker Networks

 Q.1 - b) bridge, none, host

 Q.2 - a) bridge

 Q.3 - a) Yes

 Q.1 - a) bridge

 Q.1 - c) docker network connect

 Q.2 - c) Only if ports are published

 ## Section 4: Docker Compose

 Q.1 - a) The name of the current directory

 Q.2 - a) Controls startup order only

 Q.3 -  d) Compose requires manual container removal

 Q.4 - b) docker-compose ls

 Q.5 - b) Creates <project>_default network

 Q.6 - b) Shared among all containers

 ## Section 5: Docker Volumes

 Q.1 - a) Named volume

 Q.2 - b) No

 Q.1 - c) Bind mount can map to any host path, named volume is managed by Docker

 Q.2 - a) docker volume prune

 Q.3 - b) Remains on the host

 Q.4 - b) myvol will appear immediately

 ## Practical Task

 ### Create Two Custom Bridge Networks

          docker network create mynet1
          docker network create mynet2

 ### Run Containers in Separate Networks

          docker run -d --name P1 --network mynet1 nginx
          docker run -d --name P2 --network mynet2 nginx

 ### Install ping Command

          docker exec -it b24 /bin/bash And apt update -y ,                        apt install -y iputils-ping

 ### Connect One Container to Both Networks
           docker network connect mynet2 P1

 ### Verify Communication

          docker exec P2 ping P1
         




 ### 