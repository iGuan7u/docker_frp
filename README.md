# docker_frp

# Frps

Simply an docker image about [frps](https://github.com/fatedier/frp). Version: 0.37.0

## Configure

This image will load `frps.ini` configure from `/data` folder within docker container, you can mount it with custom folder path.

[Docker-compose](https://docs.docker.com/compose/) is recommended to use with this docker image.

Docker-compose file configure:

```yaml
version: "3"
services:
  frps:
    image: iguan7u/frps
    volumes:
      - ./conf:/data                      // mount conf folder into docker container
    network_mode: "host"
    container_name: container_frps
    restart: always
```