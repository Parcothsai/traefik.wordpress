# traefik.wordpress

This directory contains everything you need to easily set up a wordpress site with Traefik. Of course, everything is from Docker.

This directory explains how to set up Traefik, with OVH DNS. It's very easy.

##	DO NOT FORGET TO CONFIGURE YOUR OVH DNS BEFORE STARTING INSTALLION



# TRAEFIK WITH OVH

Link : https://nofreedisk.space/2018/09/15/how-to-make-a-dns-record-with-ovh-and-traefik/

First step:

	Log in to https://eu.api.ovh.com/createApp/ with ovh credentials and create an app. Name it Traefik ( the name of   	application does not matter)
	
	Then, create keys. You will have two keys, one for the application, the other for the secret. DON'T LOSE THESE KEYS !!
	
	After that, you have to execute a curl command ( change https://mysite.com with YOUR url site ):
	
	curl \
	-XPOST \
	-H"X-Ovh-Application: REPLACE BY YOUR OVH APPLICATION KEY " \
	-H "Content-type: application/json" \
	https://eu.api.ovh.com/1.0/auth/credential -d '{
	"accessRules": [
	{
	"method": "GET",
	"path": "/*"
	},
	{
	"method": "POST",
	"path": "/*"
	},
	{
	"method": "PUT",
	"path": "/*"
	},
	{
	"method": "DELETE",
	"path": "/*"
	}
	],
	"redirection": "https://mysite.com/"
	}'
	
	Once it's done, you will have an url in the response. IT'S your consumer key. Go to the url, and connect with your ovh
	
	
	id and set UNLIMITED validity. 
	
	
	
# DO NOT LOSE YOUR KEYS AND DON'T PUBLISH THEM
	
	
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
	
