
# Scope

The purpose of this module is to simulate out of data conditions for testing
a set of zero rated domains.

This is achieved by allowing accessing to specific domains (Zero Rated) by a 
browser while denying access to all other domains.

## Prerequisites

  - Docker compose 2.0
  - Port 8888 is used by default - alternatively, edit the docker-compose.yml

## Whitelist domains

Simply add the domain to the "filter" file and re-start the proxy.


## Start the proxy

  docker-compose up

## Configure Firefox to use the proxy

 - Burger menu > Settings > General > Search for "proxy" > Click on "Settings"
 - Select "Manual proxy configuration"
 - Proxy : 127.0.0.1 / Port 8888
 - Check "Also use this proxy for FTP and HTTPS"
 - Hit OK

The browser should only allow  traffic to the domains listed in "filter" file.
