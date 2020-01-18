# Shell Snippets

## How to check whether Wayland or X11 is being used
```
$ echo $XDG_SESSION_TYPE
x11
```

## Share X11 socket with docker container
Docker container user must have same UID and GID as host user.
```
$ docker run -it --rm --name ubuntu -e DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -d aleksgidenko/code-dev-ubuntu
```
