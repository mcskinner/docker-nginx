## nginx

This repository contains a **Dockerfile** for a minimal installation of the
[NGINX](http://nginx.org/en/) HTTP server.

### Base Docker Image

* [ubuntu:14.04](https://hub.docker.com/_/ubuntu/)

### Usage

    # Serve the NGINX boilerplate content.
    docker run -d -p 80:80 mcskinner/nginx

    # Serve your own site.
    docker run -d -p 80:80 \
      -v $(pwd)/example/sites-enabled:/etc/nginx/sites-enabled \
      -v $(pwd)/example/html:/var/www/html \
      mcskinner/nginx
