Nginx Dockerfile
This repository contains Dockerfile of Nginx for Docker's automated build published to the public Docker Hub Registry.

Base Docker Image
dockerfile/ubuntu
Installation
Install Docker.

Download automated build from public Docker Hub Registry: docker pull dockerfile/nginx

(alternatively, you can build an image from Dockerfile: docker build -t="dockerfile/nginx" github.com/dockerfile/nginx)

Usage
docker run -d -p 80:80 dockerfile/nginx
Attach persistent/shared directories
docker run -d -p 80:80 -v <sites-enabled-dir>:/etc/nginx/conf.d -v <certs-dir>:/etc/nginx/certs -v <log-dir>:/var/log/nginx -v <html-dir>:/var/www/html dockerfile/nginx
