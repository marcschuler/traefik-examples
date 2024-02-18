# Networks and multiple docker-compose files
In this section we use networks to allow traefik to 
route via multiple docker-compose files.
Often if you manage multiple services you want to split your docker-compose
file into multiple files to have some kind of structure. In this case you
will have to make sure that every service is in the same network as traefik.


## How To
Run the docker-compose files in the 'services' and 'traefik' folder simultaneously.
You need to create the external network via ` docker network create network-traefik`

Traefik is in the network 'network-traefik' and every service which also is in this
network can communicate.

The whoami service in in this network, you can access it via http://whoami.localhost

The httpd sevice will not be available, as it is not in the same network as traefik.
If you try to access http://webserver.localhost, after a few seconds, traefik
will return 'Gateway Timeout' (with status code 504) as it cannot reach the service

## Tasks
* Make httpd available using networks