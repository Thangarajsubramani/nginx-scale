# Nginx containers auto scale with load balancing and service discovery

Nginx image based on Alpine linux version 3.10(6MB).
Orchestrate and Auto scale Nginx containers using docker-compose.
Provide High availability(HA) with load balancing and service discovery using (HAproxy)

## Prerequisites

* [docker](https://docs.docker.com/installation/mac)
* [docker compose](https://docs.docker.com/compose/install)

## Setup

    docker-compose up -d
    open http://localhost:80

## Scale

    docker-compose scale web=5
