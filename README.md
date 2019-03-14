# traefik.wordpress

This directory contains everything you need to easily set up a wordpress site with Traefik. Of course, everything is from Docker.

This directory explains how to set up Traefik, with OVH DNS. It's very easy.

##	DO NOT FORGET TO CONFIGURE YOUR OVH DNS BEFORE STARTING INSTALLION



# TRAEFIK WITH OVH

Link : https://nofreedisk.space/2018/09/15/how-to-make-a-dns-record-with-ovh-and-traefik/

## Do what is necessary to run with this repo

First:

	Create docker network proxy
	--> docker network create --attachable proxy

	Check link above to create an application on EU api-ovh.

	Then, modify with apporiate values files docker-compose.yml && traefik/toml/traefik.toml

	Also, do not FORGET to check your configuration

	And, finally, exec docker-compose command
	--> docker-compose up -d

Second:

	Acces to your site with "https://stats.mywebsite.com" and "https://mywebsite.com"
	
