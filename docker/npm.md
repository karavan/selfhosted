```yml
version: "3"
services:
#--------------------------------------------------------------------------------------------#
#                Nginx Proxy Manager - Expose your services easily and securely              #
#--------------------------------------------------------------------------------------------#
  app:
    image: 'jc21/nginx-proxy-manager:latest'
    restart: unless-stopped
    ports:
    # Do NOT change these ports! Port forward 80 and 443 in your router.
      - '80:80'
      - '443:443'
      - '81:81'
      # - '21:21' # FTP
    volumes:
      - '/data/docker/npm/data:/data'
      - '/data/docker/npm/letsencrypt:/etc/letsencrypt'
```
