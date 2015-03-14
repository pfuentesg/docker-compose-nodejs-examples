# Nginx + Node + Docker

An example of how to dockerize multiple node apps with an nginx proxy in front.

## Installation

Read examples root [README.md](https://github.com/guumaster/docker-compose-nodejs-examples/blob/master/README.md).

## Usage

 Add local routing to your `/etc/hosts` file: 

    127.0.0.1 server1.local
    127.0.0.1 server2.local

 Clone the repo and run docker-compose (if you are running it for the first time, go get a coffee)
 
```sh 
    docker-compose up -d
```

 The first time, it will download all the docker layers, then you will see message below,

     Recreating nginxexample_server1_1...
     Recreating nginxexample_server2_1...
     Recreating nginxexample_nginx_1...



## Test

You can test both urls `http://server1.local` and `http://server2.local` with your browser, curl or [httpie](http://httpie.org/)


```sh 
$> http server1.local

# it will show:
HTTP/1.1 200 OK
Connection: keep-alive
Content-Length: 556
Content-Type: application/json
Date: Sat, 14 Mar 2015 08:19:16 GMT
Server: nginx/1.6.2

{
    "headers": {
        "accept": "*/*", 
        "accept-encoding": "gzip, deflate", 
        "connection": "close", 
        "host": "server1.local", 
        "user-agent": "HTTPie/0.8.0", 
        "x-forwarded-for": "172.17.42.1", 
        "x-real-ip": "172.17.42.1"
    }, 
    "ip": "172.17.42.1", 
    "meta": {
        "delay": 0, 
        "serverName": "server1", 
        "status": 200, 
        "uptime": "3 minutes ago"
    }, 
    "method": "GET", 
    "query": {}, 
    "url": {
        "auth": null, 
        "hash": null, 
        "host": "server1.local", 
        "hostname": "server1.local", 
        "href": "http://server1.local/echo/test", 
        "path": "/echo/test", 
        "pathname": "/echo/test", 
        "port": null, 
        "protocol": "http:", 
        "query": null, 
        "search": null, 
        "slashes": true
    }
}
```

```sh 
$> http server2.local

# it will show:
HTTP/1.1 200 OK
Connection: keep-alive
Content-Length: 559
Content-Type: application/json
Date: Sat, 14 Mar 2015 08:19:55 GMT
Server: nginx/1.6.2

{
    "headers": {
        "accept": "*/*", 
        "accept-encoding": "gzip, deflate", 
        "connection": "close", 
        "host": "server2.local", 
        "user-agent": "HTTPie/0.8.0", 
        "x-forwarded-for": "172.17.42.1", 
        "x-real-ip": "172.17.42.1"
    }, 
    "ip": "172.17.42.1", 
    "meta": {
        "delay": 0, 
        "serverName": "server2", 
        "status": 200, 
        "uptime": "3 minutes ago"
    }, 
    "method": "GET", 
    "query": {}, 
    "url": {
        "auth": null, 
        "hash": null, 
        "host": "server2.local", 
        "hostname": "server2.local", 
        "href": "http://server2.local/echo/test2", 
        "path": "/echo/test2", 
        "pathname": "/echo/test2", 
        "port": null, 
        "protocol": "http:", 
        "query": null, 
        "search": null, 
        "slashes": true
    }
}

``` 

