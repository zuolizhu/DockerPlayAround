## Practice

Run a nginx, a mysql and a httpd(apache) server

Run all of them --detached(or -d), name them with --name

nginx should listen on 80:80, httpd on 8080:80, mysql on 3306:3306

When running mysql, use the --environment option(or -e) to pass in MY_SQL_RANDOM_ROOT_PASSWORD=yes

Use docker container logs on mysql to find the random password that created on startup

Clean it all up with docker container stop and docker container rm

Use docker container ls to check the result

## Cheat Sheet

### First part, to create containers:


```
docker container run -d -p 3306:3306 --name db -e MYSQL_RANDOM_ROOT_PASSWORD =yes mysql
```

### To get the password

```
docker container logs db
```

```
docker container run -d --name webserver -p 8080:80 httpd
```

```
docker container run -d --name proxy -p 80:80 nginx
```

```
docker container ls
```

### Second part, to remove all containers

```
docker container stop ID ID ID
```

```
docker container rm ID ID ID
```
