```yml
version: "3"
services:
#--------------------------------------------------------------------------------------------# 
#                                  PicoShare - Easy file sharing                             #
#--------------------------------------------------------------------------------------------#
  dozzle:
    container_name: picoshare
    image: mtlynch/picoshare
    restart: unless-stopped
    volumes:
      - '/data/nas/shared-files:/data'
    environment:
      - PORT=3001
      - PS_SHARED_SECRET=YourPasswordHere
    ports:
      - 8006:3001
```
