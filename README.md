# docker_wp with ports visit.
	$ docker-compose up -d
	then visit http://server-ip:32768

# images used:
	wordpress:latest
	mariadb:latest
		
# no domain run. with expose ports
	$ docker-compose -p wp_v3_ports -f ./docker-compose.yml  up -d  --build --remove-orphans --force-recreate

# V3 with domain: 
	- depends on: https://github.com/guoxiangke/docker-nginx-https.git
	- change domain in the ./docker-compose-v3-domain.yml
	- $ docker-compose -p wp_v3_domain -f ./docker-compose-v3-domain.yml  up -d  --build --remove-orphans --force-recreate
