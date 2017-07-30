### Installation
```
git clone https://github.com/Ghardo/nginx-php-fpm-docker.git
cd nginx-php-fpm-docker
```
### Configuration
edit the **.env** file
```
### project parent folder
CODE=~/code/www
# the ip of the local dns
DNS=192.168.178.2
```
### Preparation
add 127.0.0.1 to you're nameserver for dns resolving

```
docker-compose build --no-cache
docker-compose create
docker-compose up
```

### Xdebug ide setup
##### PHPSTORM

###### Debug
- set xdebug port to 9001 (conflicts with DBGp Proxy Port)
- set DPGp Proxy Port to 9000
- enable "Can accept external connections"

###### Servers
- set Name to docker
- set Host to docker
- set Port to 80
- set Debugger to xdebug
- enable path mapping
- map server path of the project root to "/src/www/**PROJECTNAME**"

replace **PROJECTNAME** with the name of the folder which include the project
