# SQL Server 2019 AlwaysOn Groups

## Docker Image

Docker image using Ubuntu 20.04 LTS. When the image is built it will configure update ubuntu with all needed security updates through apt get. 

Using the Microsoft repo for SQL Server Linux it will install SQL Server through apt get.

Once installed it set the configuration through mssql-conf to enable HA.

To build the image use the following commend.

```bash
docker build . -t SQL2019HA:latest

```

## Docker Compose

Docker compose is setup to run three SQL servers with HA enabled. This will use about 8GB of ram on your system remove the third one if you do not want to many SQL Servers running.

### Docker compose commands

```bash
docker-compose up 
```

```bash
docker-compose -d
```

```bash
docker-compose down
```
