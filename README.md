# flaskBoxCloud

# flaskBoxCloud

## DOCKER COMMANDS

### Build Image
```bash
docker build -t flaskboxcloud-app .

```
# Run Container on Different Port
```bash
docker run -d -p 9090:80 --name flaskboxcloud-container flaskboxcloud-app

```

# Volume
```bash
docker volume create flaskbox-data
docker run -d -p 9091:80 --name flaskbox-vol -v flaskbox-data:/data flaskboxcloud-app
```

# Network

```bash
docker network create flaskbox-net
docker run -d --name flaskbox-net-container --network flaskbox-net flaskboxcloud-app
```

# Push to DockerHub

docker tag flaskboxcloud-app student9008/flaskboxcloud-app:latest
docker push student9008/flaskboxcloud-app:latest