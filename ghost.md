```yml
version: '3.1'

services:

  ghost:
    image: ghost:alpine
    restart: always
    ports:
      - 8010:2368
    environment:
      # see https://ghost.org/docs/config/#configuration-options
      database__client: mysql
      database__connection__host: db
      database__connection__user: root
      database__connection__password: password
      database__connection__database: ghost
      # this url value is just an example, and is likely wrong for your environment!
      url: https://example.com
      # contrary to the default mentioned in the linked documentation, this image defaults to NODE_ENV=production (so development mode needs to be explicitly specified if desired)
      #NODE_ENV: development
    volumes:
      - /data/docker/blog/ghost/content:/var/lib/ghost/content

  db:
    image: mysql:8.0-oracle
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: password
    volumes:
      - /data/docker/blog/db:/var/lib/mysql
```
