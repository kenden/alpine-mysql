# alpine-mysql

A docker image of mysql based on the alpine docker image.

Get the image from [dockerhub](https://hub.docker.com/r/wangxian/alpine-mysql/).

# Build image
```
docker build -t wangxian/alpine-mysql .
```

# Usage
```
docker run -it --name mysql -p 3306:3306 -v $(pwd):/app -e MYSQL_DATABASE=admin -e MYSQL_USER=tony -e MYSQL_PASSWORD=dpa\*12d -e MYSQL_ROOT_PASSWORD=111111 wangxian/alpine-mysql
```

It will create a new db, and set mysql root password(default is 111111)


NOTE: If you don't mount the volume into folder /app with `-v $(pwd):/app`, then the mysql data will stay inside the docker container.
