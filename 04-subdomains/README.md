# 04 Subdomains
In this section we create two services with different subdomains.

## How To
Try to open http://whoami.localhost and http://webserver.localhost

### Service Naming
Remember that a server name must be unique or else both duplicate
service won't work. In this case we conveniently named our services `whoami` and `httpd`

```shell
   traefik.http.routers.httpd.rule=Host(`webserver.localhost`)
   traefik.http.routers.whoami.rule=Host(`whoami.localhost`)
```

## Tasks
* Rename the httpd service to `potato`. Change to host to `potato.localhost`
* Create another httpd server that listens to `carrot.localhost`
* Secure the carrot httpd server with basic authentication (see 03-authentication)
* Debug two hours why your services won't work only to discover 
that you copy-pasted the labels from another service but didn't 
change the service name. Then: Cry...