### start new container interactively

```
docker container run -it
```

### run additional command in existing container

```
docker container exec -it
```

### Some examples

```
docker container run -it --name proxy nginx bash
```

```
docker container run -it --name ubuntu ubuntu
```

 To exit the shell, simply type

```
exit
```

Back to that container with shell

```
docker container start -ai ubuntu
```

running something on the running container

```
docker container exec -it mysql bash
ps aux
```
