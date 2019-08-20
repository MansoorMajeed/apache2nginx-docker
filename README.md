# Apache2nginx-docker

A docker image for [Apache2Nginx](https://github.com/lide-reed/apache2nginx)
A command line tool to convert Apache config to Nginx config


# Usage

```shell
docker pull mansoor1/apache2nginx
docker run -it mansoor1/apache2nginx -h
```

## Converting a local file

```shell
docker run --rm -it -v $(pwd):/tmp mansoor1/apache2nginx:latest -f /tmp/apache.conf -o /tmp/nginx.conf
```
This will convert `apache.conf` in your current working directory and write to `nginx.conf`

> Note: the `/tmp` is added because we are mounting the `pwd` as a volume to the container
