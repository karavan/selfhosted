```yml
version: '3.3'
services:
#--------------------------------------------------------------------------------------------#
#                                   Drawio - Make diagrams easily                            #
#--------------------------------------------------------------------------------------------#
    drawio:
        container_name: drawio
        restart: unless-stopped
        ports:
            - '7011:8080'
        image: jgraph/drawio
```
