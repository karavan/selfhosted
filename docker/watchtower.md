```yml
version: "3.3"
services:
#--------------------------------------------------------------------------------------------#
#                         Watchtower - Automatic container updates                           #
#--------------------------------------------------------------------------------------------#
    watchtower:
        image: containrrr/watchtower
        restart: always
        environment:
            - watchtower
        volumes:
            - "/var/run/docker.sock:/var/run/docker.sock"
```
