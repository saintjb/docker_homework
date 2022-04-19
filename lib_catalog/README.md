# Instructions
## Create network
```
docker network create -d bridge --subnet 192.168.5.0/24 --ip-range 192.168.5.0/24 djangontw
```
## Run PostgreSQL container
```
docker run -d --name db  --net djangontw --ip 192.168.5.3 -e POSTGRES_USER=django -e POSTGRES_DB=django -e POSTGRES_PASSWORD=django postgres:14.2-alpine
```
## Build an image
```
docker build -t backend .
```
## Run container 
```
docker run -d -p 8000:8000 --name django_app --net djangontw --ip=192.168.5.2  backend
```