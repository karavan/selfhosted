```yml
version: "3"
services:
#--------------------------------------------------------------------------------------------# 
#                                 Dozzle - Real-time Docker Log Viewer                       #
#--------------------------------------------------------------------------------------------#
  dozzle:
    container_name: dozzle
    image: amir20/dozzle:latest
    restart: always
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
    ports:
      - 8006:8080
```
