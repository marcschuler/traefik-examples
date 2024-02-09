# 01 Basic 'Who am I?'
This is a simple example which shows how to integrate start traefik
with a basic whoami server. It also includes basic routing for our
little service.

## How To
The service is accessible via http://whoami.localhost

If you enter another URL which isn't defined in the traefik routing
it will simply return an "404 page not found", for example at
http://test.localhost or http://potato.localhost

## Tasks
* Try to change the URL. Make the service accessible via http://potato.localhost