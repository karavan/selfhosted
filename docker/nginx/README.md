I'm using a custom configuration for nginx. You can find the config file in `config > nginx > site-confs`.

```yml
server {
    listen 80 default_server;

    listen 443 ssl;

    root /config/www/walkx.org/public;
    index index.html index.htm index.php;

    server_name _;


    ssl_certificate /config/keys/cert.crt;
    ssl_certificate_key /config/keys/cert.key;

    client_max_body_size 0;

    location / {
        try_files $uri $uri/ =404;
    }

    error_page 404 /404.html;
    location = /404.html {
        root /config/www/walkx.org/public;
        internal;
    }

    location ~ ^(.+\.php)(.*)$ {
        fastcgi_split_path_info ^(.+\.php)(.*)$;
        fastcgi_pass 127.0.0.1:9000;
        fastcgi_index index.php;
        include /etc/nginx/fastcgi_params;
    }
}

```
