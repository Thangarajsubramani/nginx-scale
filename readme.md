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

## Scale Up

    docker-compose scale web=5

## Scale Up

    docker-compose scale web=2

## How would this be configured to maximize availability.
```
    docker-compose scale web=5
```

## What loads would this spinup be able to handle. (documentation only)
  ```
   if Available memory 2 GB means . we can spin up count * 50 MB == 2GB -50MB (LB)
   we can use kubernetes to limit the memory and cpu very well. it will help to find out the capacity accurately.
  ```

## How would logging, security be applied. (documentation only)
  ```
   we can not expose /var/run/docker.sock . so we can avoid using kubernetes API to get the Nginx container IP address.
   we can use clair tool as part of CI/CD to scan image layer and identify the security issues. we can create base image and keep updating the patches with that.

  ```
