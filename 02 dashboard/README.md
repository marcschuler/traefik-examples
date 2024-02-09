# 02 Dashboard
This examples illustrates how you can use the dashboard and use two services on the same domain, separating them by path.

## How To
The 'who am I' service from the last example is available via http://localhost

The treafik dashboard is available on the some 'domain' but only if
the path is prefixed with `/dashboard/` or `/api`. You can visit the dashboard at 
http://localhost/dashboard/

## Tasks
* View the HTTP routers and HTTP services on the dashboard. Can you find the definitions for the whoami service?
* 