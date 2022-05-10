```yml
version: "3.3"
services:
#--------------------------------------------------------------------------------------------#
#                   File Browser - Easy file management in your browser                      #
#--------------------------------------------------------------------------------------------#
  filebrowser:
    container_name: filebrowser
    image: filebrowser/filebrowser:latest
    restart: unless-stopped
    volumes:
      - '/:/srv'
      - '/data/docker/filebrowser/settings.json:/config/settings.json'
      - '/data/docker/filebrowser/filebrowser.db:/database/filebrowser.db'
    ports:
      - '8001:80'
```
