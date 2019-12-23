# Shadowsocks libev

FSP Network Gen2 Server Infrastructure - SSlibev

![Docker Automated build](https://img.shields.io/docker/automated/fspnetwork/ss.svg?style=flat-square)
![Docker Build Status](https://img.shields.io/docker/build/fspnetwork/ss.svg?style=flat-square)
![GitHub](https://img.shields.io/github/license/fspnet/docker-sslibev.svg?style=flat-square)

![Shadowsocks-libev](https://img.shields.io/badge/ss--libev-3.2.4-blue.svg?style=flat-square)

A docker image for [shadowsocks-libev](https://github.com/shadowsocks/shadowsocks-libev) server with [simple-obfs](https://github.com/shadowsocks/simple-obfs) support

### Download from Docker Hub 

    docker pull registry.gitlab.com/fspnetwork/ss

### Usage
```sh
docker run -d --restart=always -e "PASSWORD=value" -p 8388:8388 -p 8388:8388/udp --name ssserver registry.gitlab.com/fspnetwork/ss
```

### Default configuration in environment variables
| Environment | Default |
| - | - |
| SS_PORT | 8388 |
| PASSWORD | ChangeMe!!! |
| SS_METHOD | chacha20-ietf-poly1305 |
| SS_TIMEOUT | 60 |
| DNS_ADDR | 1.1.1.1,1.0.0.1 |
| PLUGIN | obfs-server |
| PLUGIN_OPTS | obfs=tls;fast-open;failover=0.0.0.0:8443 |