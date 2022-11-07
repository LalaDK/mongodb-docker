# MongoDB via Docker

## Create storage directory for MongoDB
```sh
sudo mkdir -p /data/mongodb
```

## Create Docker container for MongoDB
```sh
docker run --name mongodb -d -v /data/mongodb:/data/db -p 27017:27017 mongo
```

## Restore database
```sh
docker cp /path/to/dump/ CONTAINER_ID:/dump
docker exec -i CONTAINER_ID /usr/bin/mongorestore /dump/
```

# Stop/start/restart MongoDB
```sh
docker stop mongodb
docker start mongodb
docker restart mongodb
```
