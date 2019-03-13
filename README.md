# wordpress_traefik

This directory contains everything you need to easily set up a wordpress site with Traefik. Of course, everything is from Docker.


# TRAEFIK WITH OVH

Link : https://nofreedisk.space/2018/09/15/how-to-make-a-dns-record-with-ovh-and-traefik/

## Necessary to run with this repo

First:

	Create docker network proxy
	--> docker network create --attachable proxy

	Check link above to create an application on EU api-ovh.

	Then, modify with apporiate values files docker-compose.yml && traefik/toml/traefik.toml

	Also, do not FORGET to check your configuration

	And, finally, exec docker-compose command
	--> docker-compose up -d
