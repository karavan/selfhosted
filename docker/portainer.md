```sh
#--------------------------------------------------------------------------------------------#
#                         Portainer - Easily manage docker containers                        #
#--------------------------------------------------------------------------------------------#
docker volume create portainer_data

docker run -d -p 9000:8000 -p 9443:9443 --name portainer \
    --restart=always \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v portainer:/data \
    portainer/portainer-ce:latest
```
