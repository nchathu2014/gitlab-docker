# GitLab Server Run in a Docker Container
This document support abpout the steps that run GitLab server in a Docker container

STEP 1: Install and start docker engine
If you are hosted in Windows you can install docker for windows and through that GUI, you can start up the Docker 

If you are not in windows environment you cvan follow the following steps,

```
yum install docker

systemctl start docker

systemctl enable docker

systemctl status docker
```

STEP 2: Pull and run GitLab docker image
```
docker run -d --hostname gitlab.example.com \
-p 443:443 -p 80:80 -p 2222:22 \
--name gitlab-nuwan \
--restart unless-stopped \
--volume /storage/gitlab/config:/etc/gitlab \
--volume /storage/gitlab/logs:/var/log/gitlab \
--volume /storage/gitlab/data:/var/opt/gitlab \
gitlab/gitlab-ce:latest
```
Since docker gitlab docker container running in detached mode, we can see the logs and undersnad what running behind as follows,
```
docker ps

docker logs <CONTAINER-ID> -f
```

STEP 3:

STEP 4:

STEP 4:

