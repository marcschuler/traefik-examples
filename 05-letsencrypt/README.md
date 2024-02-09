# HTTPS with Lets Encrypt
In this section we use HTTPS to encrypt our communication.


## How To
Try to open http://webserver.localhost or https://webserver.localhost and
ignore the warnings about self signed certificates.

If you use the http port you will be redirected to the https port.
Or in more detail: The entrypoint 'web' on port 80 will redirect to
the entrypoint 'websecure' on port 443 which is set up to use lets encrypt.

### Certificates
Currently the certificates are self signed because lets encrypt does
not sign certificates for domain you do not own or local hostnames like `localhost`.
If you have a domain: Great! Replace the host and traefik will automatically
create and validate all required certificates and store them in the letsencrypt folder.

## Tasks
* Own a domain and try to get real certificates from lets encrypt
* Remove the redirection from http to https and disable https for the httpd service