```yml
version: "3"
services:
#--------------------------------------------------------------------------------------------#
#                             Dashdot - A modern server stat dashboard                       #
#--------------------------------------------------------------------------------------------#
  dozzle:
    container_name: Dashdot
    image: mauricenino/dashdot:latest
    ports:
      - '8002:8080'
    restart: unless-stopped
    environment:
      DASHDOT_OVERRIDE_DISTRO: Ubuntu
    privileged: true
```
