# Midterm Review 

The midterm review was carried out by me (Carlos Enriquez) to ultimately generate a docker-compose application stack
that contains redis, a mini-jupyter notebook with redis installed and portainer. 

The mini-jupyter notebook with redis installed was generated using a dockerfile, and the respective image has been 
loaded to Dockerhub (https://hub.docker.com/r/carloskez/jupyter_redis).

Some important commands used to generate this stack:


### Directories

```
#directories
mkdir ~/review
cd ~/review
mkdir work
mkdir docker

```

### Github init

```
git init
git add README.md
git commit -m "Added the readme"
git remote add origin https://github.com/carlos-a-enriquez/bdp2-midterm.git
git branch -M main
git push -u origin main

```

### Docker build

```
docker build -t jupyter_redis .
```


### Docker compose

```
### fixed the docker-compose.yml file

docker-compose up -d #starting docker compose
docker compose logs -f #checking the docker compose logs
docker-compose down #shutting down container stack

###network debugging
docker network ls #checking network list
docker network inspect <network hash> #checking connected containers to each network
sudo lsof -i -P -n | grep LISTEN #checking open host (VM1) ports
```



