# Docker
Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers. 


### Basic

- docker-compose up | Start up a docker-compose.yaml container

### Starting
- docker container start {Name} | Tab over after start to get a list of all contianers
- docker container stats | Shows System Resource Usage
- docker container list | Show all running containers 
- 
### Information Grabbing
- docker network list | Show all networks
- docker ps | -q for just ID numbers - Shows all dockers running and basic stats


### Restarting all Docker Containers on reboot unless manually stopped. 
docker update --restart unless-stopped $(docker ps -q) 
 

https://docs.docker.com/config/containers/start-containers-automatically/
