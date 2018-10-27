# Docker-SS

FSP Network Gen2 Server Infrastructure - SS libev

![Docker Automated build](https://img.shields.io/docker/automated/fspnetwork/ss.svg?style=flat-square)
![Docker Build Status](https://img.shields.io/docker/build/fspnetwork/ss.svg?style=flat-square)
![GitHub](https://img.shields.io/github/license/fastsp/docker-sslibev.svg?style=flat-square)

![Shadowsocks-libev](https://img.shields.io/badge/ss--libev-3.2.0-blue.svg)

A docker image for [shadowsocks-libev](https://github.com/shadowsocks/shadowsocks-libev) server

### Download from Docker Hub 

    docker pull fspnetwork/ss

### Usage

    docker run -p 443:443 -p 443:443/udp --rm -it fspnetwork/ss


or running as a service

    docker run -d --restart=always -e "SS_PORT=443" -e "SS_PASSWORD=123456" -e "SS_METHOD=chacha20" -e "SS_TIMEOUT=600" -p 443:443 -p 443:443/udp --name ssserver fspnetwork/ss

### Default configuration in environment variables

    SS_PORT     443
    
    SS_PASSWORD 123456
    
    SS_METHOD   chacha20

    SS_TIMEOUT  600

based [shadowsocks-docker](https://github.com/hangim/shadowsocks-docker)