```sh
#--------------------------------------------------------------------------------------------#
#                         Portainer - Easily manage docker containers                        #
#--------------------------------------------------------------------------------------------#
docker volume create portainer_data

docker run -d -p 9080:8000 9000:9443 --name portainer \
    --restart=always \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v portainer:/data \
    portainer/portainer-ce:latest
```
