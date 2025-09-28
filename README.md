
<h2 align="center">
  Statuscool
</h2>

<p align="center">
Easily deploy a status page and start monitoring endpoints in seconds
</p>

## Origin
Statuscool is a fork of [Statusnook](https://github.com/goksan/Statusnook) but with more visual improvements

## Deployment paths

#### DockerCLI
```
docker run -d -p 80:80 -v statuscool-data:/app/statuscool-data --restart always ghcr.io/airoflare/statuscool:latest
```

#### Docker Compose.yaml

```
services:
  statuscool:
    image: ghcr.io/airoflare/statuscool:latest
    container_name: statuscool
    volumes:
      - statuscool-data:/app/statuscool-data
    ports:
      - 80:80
      
volumes:
  statuscool-data:
```

```
docker compose up
```

#### Coolify compose

```
services:
  statuscool:
    image: ghcr.io/airoflare/statuscool:latest
    volumes:
      - statuscool-data:/app/statuscool-data
    environment:
      - SERVICE_URL_STATUSCOOL_80
```


