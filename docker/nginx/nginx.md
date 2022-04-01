```yml
version: "3.3"
services:
#--------------------------------------------------------------------------------------------#
#               Nginx - Advanced Load Balancer, Web Server, & Reverse Proxy                  #
#--------------------------------------------------------------------------------------------#
  nginx:
    image: "linuxserver/nginx:latest"
    restart: unless-stopped
    ports:
      - "7001:80"
      - "7002:443"
    environment:
      PUID: 1000
      PGID: 1000
      TZ: "Europe/Amsterdam"
    volumes:
      - "/data/docker/nginx/sitename:/config"
```
