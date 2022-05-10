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
            - '7012:8080'
        image: jgraph/drawio
```
