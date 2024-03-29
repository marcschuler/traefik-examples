# Traefik Examples
A few practical examples for traefik reverse proxy.
Every folder contains an example which showcases one
specific usecase for traefik.

You should have a roudimentary understanding of how
docker, traefik or reverse proxies in general work.
This is not a tutorial, this is a practical showcase
for common usecases to try out locally.

## How To Run
Just clone this repository (or copy any docker-compose.yml) and
run it via `docker-compose up`.

Additionally sometimes there are a few tasks, which will offer you to deepen your
understanding of traefik by tinkering the examples. I will offer no solutions...

## Examples

### 01 Basic
A basic whoami webserver running on http://whoami.localhost

### 02 Dashboards
Show the traefik dashboard and run two services on the same domain, separated by path

### 03 Authentication
Use traefik middlewares to force an HTTP basic authentication for your services

### 04 Subdomains
Create services that listen to different subdomains

### 05 HTTPS with Let's Encrypt
Use Let's Encrypt to automatically generate HTTPS certificates for you

### 06 Networks and multiple docker-compose files
Use traefik for services defined in other docker-compose files using docker networks