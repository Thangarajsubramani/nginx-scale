# Nginx auto scale with load balancing and service discovery

Nginx image based on Alpine linux (6 MB) and auto scale Nginx containers with load balancing(HA) and service discovery

## Prerequisites

* [docker](https://docs.docker.com/installation/mac)
* [docker compose](https://docs.docker.com/compose/install)

## Setup

    docker-compose up -d
    open http://localhost:80

## Scale

    docker-compose scale web=5
