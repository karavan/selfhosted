```yml
version: "3"
services:
#--------------------------------------------------------------------------------------------#
#                             Searxng - Search without being tracked.                        #
#--------------------------------------------------------------------------------------------#
  dozzle:
    container_name: searxng
    image: searxng/searxng
    ports:
      - '7030:8080'
    restart: always
    environment:
      - BASE_URL=https://search.walkx.org/
      - INSTANCE_NAME=SearXNG NL
```
