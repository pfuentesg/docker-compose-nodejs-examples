# Docker-compose and NodeJS examples

## Requirements

 * installed [docker](https://docs.docker.com/installation/)
 * installed [docker-compose](https://docs.docker.com/compose/install/)
 * installed [httpie](http://httpie.org/) (optional)


## usage

    git clone https://github.com/guumaster/docker-compose-nodejs-examples.git
    cd docker-compose-nodejs-examples
    cd <choosed-example>
    docker-compose up -d

## Examples

### Nginx and two simple node echo server

Two simple node servers behind nginx. See [nginx-example](https://github.com/guumaster/docker-compose-nodejs-examples/tree/master/nginx-example)

### Elasticsearch + Mongoose 

Dockerized ELK stack + MongoDB. A demo app with mongoose and mongoosastic plugin to show Elasticsearch geospatial capacities. See [mongoose-elasticsearch-geosearch](https://github.com/guumaster/mongoose-elasticsearch-geosearch.git)

### Express app + Elasticsearch

A book app with Elasticsearch and kibana dashboard. See [bookdbtastic](https://github.com/guumaster/bookdbtastic.git)


## Maintainer

Guumaster

* Email: <guuweb@gmail.com>
* Twitter: [@guumaster](https://twitter.com/guumaster)


## Reference

More resources on Node and Docker

* [docker-compose-nodejs-examples](https://github.com/b00giZm/docker-compose-nodejs-examples)
