<p align = "center" >
  <h3 align = "center" > Selfhosted </h3>

  <p align = "center" >
    Configuration files for my selfhosted services.
 <br/>
    <a href = "#what-am-i-hosting" > <strong > Take a look at some of my instances »</strong> </a>
</p>

## Table of Contents
- [Table of Contents](#table-of-contents)
- [What's hosting my services?](#whats-hosting-my-services)
  - [Storage](#storage)
  - [Software](#software)
- [Network Setup](#network-setup)
- [What am I hosting?](#what-am-i-hosting)


## What's hosting my services?
I'm currently hosting all of my services on a [Raspberry Pi 4B 8GB](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/?variant=raspberry-pi-4-model-b-8gb).

### Storage
- [1TB External SSD via USB](https://www.amazon.de/-/en/ElementsTM-External-Drive-Interface-Speed/dp/B097TTZD48)
- [Synology DS212](https://www.synology.com/en-global/support/download/DS212?version=6.2#docs)

### Software
- [RaspiOS Lite Arm64 22.01](https://downloads.raspberrypi.org/raspios_lite_arm64/images/)
- [Docker](https://www.docker.com/)

## Network Setup
![Network Diagram](/network-diagram.png)

## What am I hosting?
Find docker-compose files for all of these services in the docker folder.
- [ArchiveBox](https://github.com/ArchiveBox/ArchiveBox) - [(archives.walkx.org)](https://archives.walkx.org)
- [Dozzle](https://github.com/amir20/dozzle)
- [Filebrowser](https://github.com/filebrowser/filebrowser)
- [Ghost](https://ghost.org) - [(blog.walkx.org)](https://blog.walkx.org)
- [Jellyfin](https://github.com/jellyfin/jellyfin)
- [Libreddit](https://github.com/spikecodes/libreddit) - [(r.walkx.org)](https://r.walkx.org)
- [Navidrome](https://github.com/navidrome/navidrome)
- [Nginx](https://github.com/nginxinc/docker-nginx) - [(walkx.org)](https://walkx.org)
- [Nginx Proxy Manager](https://github.com/NginxProxyManager/nginx-proxy-manager)
- [Portainer](https://github.com/portainer/portainer)
- [Uptime Kuma](https://github.com/louislam/uptime-kuma) - [(up.walkx.org)](https://up.walkx.org)
- [Watchtower](https://github.com/containrrr/watchtower)
- More in the future...
