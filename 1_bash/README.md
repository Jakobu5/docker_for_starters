# BASH

A simple bash container can be spawned with:

```
sudo docker run -it --rm bash:4.4
```

Scripts can be imported by using a `Dockerfile`:

```
FROM bash:4.4

RUN echo $BASH_VERSION

COPY script.sh /

CMD ["bash", "/script.sh"]
```
This container can be built with:

```
sudo docker build -t bash-container .
```
And run with:
```
sudo docker run --rm bash-container
```

With a `docker-compose` file:

```
sudo docker-compose up
```
and
```
sudo docker-compose down
```