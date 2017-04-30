# MongoDB Dockerfile

A Dockerfile that produces a Docker Image for [MongoDB](http://www.mongodb.org/).


## Usage

### Build the image

To create the image `bernardosecades/mongodb`, execute the following command on the `docker-mongodb` folder:

```
$ docker build --tag bernardosecades/mongodb .
```

### Run the image

To run the image and bind to host port 27017:

```
$ docker run -p 27017:27017 --name mongo_instance_001 -d bernardosecades/mongodb
```

Get container ID:

```
$ docker ps -a
```

Check mongodb logs:

```
$ docker logs <CONTAINER_ID>
```

Run shell mongodb:

`docker exec -it <CONTAINER_ID> <command>

```
$ docker exec -it <CONTAINER_ID> mongo
```

Or

```
$ docker exec -it <CONTAINER_ID> mongo admin
```
