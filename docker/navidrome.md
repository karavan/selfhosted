```yml
version: "3"
services:
#--------------------------------------------------------------------------------------------#
#                          Navidrome - Your Personal Streaming Service                       #
#--------------------------------------------------------------------------------------------#
  navidrome:
    image: deluan/navidrome:latest
    restart: unless-stopped
    ports:
      - "8002:4533"
    environment:
      ND_SESSIONTIMEOUT: 24h
      ND_SCANSCHEDULE: "@every 24h"
      ND_LOGLEVEL: "info"
      ND_DEFAULTTHEME: "Spotify-ish"
    volumes:
      - "/data/docker/navidrome:/data"
      - "/data/nas/CD_DVD/CD:/music:ro"
```
