```sh
docker volume create uptime-kuma
docker run -d --restart=always -p 8004:3001 -v /data/docker/uptimekuma:/app/data --name uptime-kuma louislam/uptime-kuma:1
```
