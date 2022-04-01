```yml
version: "3.1"
services:
#--------------------------------------------------------------------------------------------#
#                                 Ghost - Easy content management                            #
#--------------------------------------------------------------------------------------------#
  ghost:
    image: ghost:alpine
    restart: unless-stopped
    ports:
      - '8010:2368'
    environment:
      database__client: mysql
      database__connection__host: db
      database__connection__user: root
      database__connection__password: password
      database__connection__database: ghost
      # This URL *has* to be the url you are using to connect. (Eg. Testing environments will most likely need localhost:8080).
      url: https://example.com
    volumes:
      - '/data/docker/blog/ghost/content:/var/lib/ghost/content'

  db:
    # Change to mysql:8.0 for better Amd64 support.
    image: mysql:8.0-oracle
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: password
    volumes:
      - '/data/docker/blog/db:/var/lib/mysql'
```
