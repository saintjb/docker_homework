# Instructions
## Create network
```
docker network create -d bridge --subnet 192.168.5.0/24 --ip-range 192.168.5.0/24 djangontw
```
## Create volume to store data
```
docker volume create postgr
```
## Run PostgreSQL container
```
docker run -d --name db  --net djangontw --ip 192.168.5.3 -e POSTGRES_USER=django -e POSTGRES_DB=django -e POSTGRES_PASSWORD=django-v postgr:/var/lib/postgresql/data postgresql:14.2-alpine
```
## Build an image
```
docker build -t backend_app .
```
## Run container 
```
docker run -d -p 8000:8000 --name django_app --net djangontw --ip=192.168.5.2  backend_app
```