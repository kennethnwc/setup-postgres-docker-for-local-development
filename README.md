# setup-postgres-docker-for-local-development

## Steps:
Get the postgres images
```bash
docker pull postgres
```
Show the docker images
```bash
docker images
```
Create local volume for docker postgres to mount on
```bash
mkdir ${HOME}/postgres-data/

docker run -d --name postgres-test -e POSTGRES_PASSWORD=12345 -v ${HOME}/postgres-data/:/var/lib/postgresql/data -p 5432:5432 postgres

```

Enter postgres
```bash
docker exec -it postgres-test bash
```
In the container bash now. 
Connec to database
```bash
psql -h localhost -U postgres
```
