```yml
version: "3.3"
services:
#--------------------------------------------------------------------------------------------#
#                                Jellyfin - Your own media system                            #
#--------------------------------------------------------------------------------------------#
  nginx:
    image: "linuxserver/jellyfin:latest"
    restart: unless-stopped
    ports:
      - "1900:1900/tcp"
      - "8096:8096/tcp"
      - "7359:7359/udp"
    volumes:
      - "/data/docker/jellyfin:/config"
      - "/data/nas/media/shows:/data/shows"
      - "/data/nas/CD_DVD/DVD:/data/dvd"
      - "/data/nas/media/movies:/data/movies"
```
